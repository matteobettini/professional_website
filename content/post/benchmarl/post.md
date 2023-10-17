[//]: <>


<!-- ![BenchMARL](https://github.com/matteobettini/vmas-media/blob/main/media/benchmarl.png?raw=true) -->

**TL;DR:**
- We introduce BenchMARL, a training library for benchmarking MARL algorithms, tasks, and models backed by TorchRL.
- BenchMARL already contains a variety of SOTA algorithms and tasks.
- BenchMARL is grounded by its core tenets: standardization and reproducibility

# What is BenchMARL 🧐?
BenchMARL is a Multi-Agent Reinforcement Learning (MARL) training library created to enable reproducibility
and benchmarking across different MARL algorithms and environments.
Its mission is to present a standardized interface that allows easy integration of new algorithms and environments to 
provide a fair comparison with existing solutions.
BenchMARL uses [TorchRL](https://github.com/pytorch/rl) as its backend, which grants it high performance 
and state-of-the-art implementations.
It also uses [hydra](https://hydra.cc/docs/intro/) for flexible and modular configuration,
and its data reporting is compatible with [marl-eval](https://sites.google.com/view/marl-standard-protocol/home) 
for standardised and statistically strong evaluations.

BenchMARL **core design tenets** are:
* _Reproducibility through systematical grounding and standardization of configuration_ 
* _Standardised and statistically-strong plotting and reporting_
* _Experiments that are independent of the algorithm, environment, and model choices_
* _Breadth over the MARL ecosystem_
* _Easy implementation of new algorithms, environments, and models_
* _Leveraging the know-how and infrastructure of [TorchRL](https://github.com/pytorch/rl), without reinventing the wheel_

# Why would I BenchMARL 🤔?
Why would you BenchMARL, I see you ask. 
Well, you can BenchMARL to compare different algorithms, environments, models, 
to check how your new research compares to existing ones, or if you just want to approach 
the domain and want to easily take a picture of the landscape.

# Why does it exist?

We created it because, compared to other ML domains, RL has always been more fragmented
in terms of shared community standards, tools, and interfaces. 
In MARL, this problem is even more evident, with new libraries being frequently 
introduced that focus on specific algorithms, environments, or models. Furthermore, 
these libraries often implement components from scratch, without leveraging the know-how of
the single-agent RL community. In fact, the great majority of components used in MARL is shared 
with single-agent RL (e.g., losses like MAPPO, models, probability distributions, replay buffers, and much more).

This fragmentation of the domain has led to a reproducibility crisis, recently highlighted in 
a NeurIPS paper [^1]. While authors in [^1] propose a set of tools for statistically-strong results' reporting, 
there is still the need for a standardized library to run such benchmarks. 
This is where BenchMARL comes in. Its mission is to provide a benchmarking tool for MARL, 
leveraging the components of TorchRL for a solid RL backend.

[^1]: _Gorsane, Rihab, et al. "Towards a standardised performance evaluation protocol 
for cooperative marl." Advances in Neural Information Processing Systems 35 (2022): 5510-5521._

# How do I use it?

### Command line

Simple, to run an experiment from the command line do:

```bash
python benchmarl/run.py algorithm=mappo task=vmas/balance
```

to run multiple experiments, a benchmark you can do:

```bash
python benchmarl/run.py -m algorithm=mappo,qmix,masac task=vmas/balance,vmas/sampling seed=0,1
```

Multirun has many launchers supported in the backend. 
The default implementation for hydra multirun is sequential, but [parallel](https://hydra.cc/docs/plugins/joblib_launcher/) and 
[slurm](https://hydra.cc/docs/plugins/submitit_launcher/) launchers are also available.


### Script

Run an experiment:

```python
experiment = Experiment(
    task=VmasTask.BALANCE.get_from_yaml(),
    algorithm_config=MappoConfig.get_from_yaml(),
    model_config=MlpConfig.get_from_yaml(),
    critic_model_config=MlpConfig.get_from_yaml(),
    seed=0,
    config=ExperimentConfig.get_from_yaml(),
)
experiment.run()
```

Run a benchmark:

```python
benchmark = Benchmark(
    algorithm_configs=[
        MappoConfig.get_from_yaml(),
        QmixConfig.get_from_yaml(),
        MasacConfig.get_from_yaml(),
    ],
    tasks=[
        VmasTask.BALANCE.get_from_yaml(),
        VmasTask.SAMPLING.get_from_yaml(),
    ],
    seeds={0, 1},
    experiment_config=ExperimentConfig.get_from_yaml(),
    model_config=MlpConfig.get_from_yaml(),
    critic_model_config=MlpConfig.get_from_yaml(),
)
benchmark.run_sequential()
```

# Components

The goal of BenchMARL is to bring different MARL environments and algorithms
under the same interfaces to enable fair and reproducible comparison and benchmarking.
BenchMARL is a full-pipline unified training library with the goal of enabling users to run
any comparison they want across our algorithms and tasks in just one line of code.
To achieve this, BenchMARL interconnects components from [TorchRL](https://github.com/pytorch/rl), 
which provides an efficient and reliable backend.

The library has a [default configuration](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf) for each of its components.
While parts of this configuration are supposed to be changed (for example experiment configurations),
other parts (such as tasks) should not be changed to allow for reproducibility.
To aid in this, each version of BenchMARL is paired to a default configuration.

Let's now introduce each component in the library.

**Experiment**. An experiment is a training run in which an algorithm, a task, and a model are fixed.
Experiments are configured by passing these values alongside a seed and the experiment hyperparameters.
The experiment [hyperparameters](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/experiment/base_experiment.yaml) cover both 
on-policy and off-policy algorithms, discrete and continuous actions, and probabilistic and deterministic policies
(as they are agnostic of the algorithm or task used).
An experiment can be launched from the command line or from a script.

**Benchmark**. In the library we call `benchmark` a collection of experiments that can vary in tasks, algorithm, or model.
A benchmark shares the same experiment configuration across all of its experiments.
Benchmarks allow to compare different MARL components in a standardized way.
A benchmark can be launched from the command line or from a script.

**Algorithms**. Algorithms are an ensemble of components (e.g., losss, replay buffer) which
determine the training strategy. Here is a table with the currently implemented algorithms in BenchMARL.

| Name                                                                                                                                        | On/Off policy | Actor-critic | Full-observability in critic | Action compatibility  | Probabilistic actor |   
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------|--------------|------------------------------|-----------------------|---------------------|
| [MAPPO](https://arxiv.org/abs/2103.01955)                                                                                                   | On            | Yes          | Yes                          | Continuous + Discrete | Yes                 |   
| [IPPO](https://arxiv.org/abs/2011.09533)                                                                                                    | On            | Yes          | No                           | Continuous + Discrete | Yes                 |  
| [MADDPG](https://arxiv.org/abs/1706.02275)                                                                                                  | Off           | Yes          | Yes                          | Continuous            | No                  | 
| [IDDPG](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/algorithms/iddpg.py)                                              | Off           | Yes          | No                           | Continuous            | No                  |   
| [MASAC](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/algorithms/masac.py)                                              | Off           | Yes          | Yes                          | Continuous + Discrete | Yes                 |   
| [ISAC](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/algorithms/isac.py)                                                | Off           | Yes          | No                           | Continuous + Discrete | Yes                 |   
| [QMIX](https://arxiv.org/abs/1803.11485)                                                                                                    | Off           | No           | NA                           | Discrete              | No                  | 
| [VDN](https://arxiv.org/abs/1706.05296)                                                                                                     | Off           | No           | NA                           | Discrete              | No                  |  
| [IQL](https://www.semanticscholar.org/paper/Multi-Agent-Reinforcement-Learning%3A-Independent-Tan/59de874c1e547399b695337bcff23070664fa66e) | Off           | No           | NA                           | Discrete              | No                  |  


**Tasks**. Tasks are scenarios from a specific environment which constitute the MARL
challenge to solve.
They differ based on many aspects, here is a table with the current environments in BenchMARL

| Environment                                                        | Tasks                                                                                       | Cooperation               | Global state | Reward function               | Action space          | Vectorized |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------|---------------------------|--------------|-------------------------------|-----------------------|:----------:|
| [VMAS](https://github.com/proroklab/VectorizedMultiAgentSimulator) | [5](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/task/vmas)       | Cooperative + Competitive | No           | Shared + Independent + Global | Continuous + Discrete |    Yes     |    
| [SMACv2](https://github.com/oxwhirl/smacv2)                        | [15](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/task/smacv2)    | Cooperative               | Yes          | Global                        | Discrete              |     No     |
| [MPE](https://github.com/openai/multiagent-particle-envs)          | [8](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/task/pettingzoo) | Cooperative + Competitive | Yes          | Shared + Independent          | Continuous + Discrete |     No     |
| [SISL](https://github.com/sisl/MADRL)                              | [2](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/task/pettingzoo) | Cooperative               | No           | Shared                        | Continuous            |     No     |

> BenchMARL uses the [TorchRL MARL API](https://github.com/pytorch/rl/issues/1463) for grouping agents.
> In competitive environments like MPE, for example, teams will be in different groups. Each group has its own loss,
> models, buffers, and so on. Parameter sharing options refer to sharing within the group. See the example on [creating
> a custom algorithm](https://github.com/facebookresearch/BenchMARL/tree/main/examples/extending/algorithm/custom_algorithm.py) for more info. 

**Models**. Models are neural networks used to process data. They can be used as actors (policies) or, 
when requested, as critics. We provide a set of base models (layers) and a SequenceModel to concatenate
different layers. All the models can be used with or without parameter sharing within an 
agent group. Here is a table of the models implemented in BenchMARL

| Name                           | Decentralized | Centralized with local inputs | Centralized with global input | 
|--------------------------------|:-------------:|:-----------------------------:|:-----------------------------:|
| [MLP](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/models/mlp.py) |      Yes      |              Yes              |              Yes              | 

And the ones that are _work in progress_

| Name | Decentralized | Centralized with local inputs | Centralized with global input | 
|------|:-------------:|:-----------------------------:|:-----------------------------:|
| GNN  |      Yes      |              Yes              |              No               | 
| CNN  |      Yes      |              Yes              |              Yes              | 


# Features
BenchMARL has many features. In this section we will dive deep
in the features that correspond to our core design tenets, but there are many more cool 
nuggets here and there, such as:

* **A test CI** with integration and training test routines that are run **for all simulators and algorithms**
* Integration in the **official TorchRL ecosystem** for dedicated support
* Experiment **checkpointing** and restoring using `torch`
* Experiment **logging** compatible with many loggers (wandb, csv, mflow, tensorboard). 
The wandb logger is fully compatible with experiment restoring and will automatically resume the run of the loaded experiment.

In the following we illustrate the features which are core to our tenets.

## Fine-tuned public benchmarks

In the [fine_tuned](https://github.com/facebookresearch/BenchMARL/blob/main/fine_tuned) folder 
we are collecting some tested hyperparameters for
specific environments to enable users to bootstrap their benchmarking.
You can just run the scripts in this folder to automatically use the proposed hyperparameters.

We will tune benchmarks for you and publish the config and benchmarking plots on
[Wandb](https://wandb.ai/benchmarl/public/reportlist) publicly

Currently available ones are:

<div class="row">
<b>VVMAS:</b>
<a href="https://github.com/facebookresearch/BenchMARL/blob/main/fine_tuned/vmas/conf/config.yaml">
<img src=https://img.shields.io/badge/Conf-purple.svg />
</a>
<a href="https://api.wandb.ai/links/benchmarl/xf5h3p3m">
<img src=https://img.shields.io/badge/Benchmarks-Wandb-yellow />
</a></div>

In the following, we report a table of the results:

| **<p align="center">Environment</p>** | **<p align="center">Sample efficiency curves (all tasks)</p>**                            | **<p align="center">Performance profile</p>**                                             | **<p align="center">Aggregate scores</p>**                                                |
|---------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| VMAS                                  | <img src="https://drive.google.com/uc?export=view&id=1fzfFn0q54gsALRAwmqD1hRTqQIadGPoE"/> | <img src="https://drive.google.com/uc?export=view&id=151pSR2sBluSpWiYxtq3jNX0tfE0vgAuR"/> | <img src="https://drive.google.com/uc?export=view&id=1q2So9V6sL8NHMtj6vL-S3KyzZi11Vfia"/> |


## Reporting and plotting

Reporting and plotting is compatible with [marl-eval](https://github.com/instadeepai/marl-eval). 
If `experiment.create_json=True` (this is the default in the [experiment config](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf/experiment/base_experiment.yaml))
a file named `{experiment_name}.json` will be created in the experiment output folder with the format of [marl-eval](https://github.com/instadeepai/marl-eval).
You can load and merge these files using the utils in [eval_results](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/eval_results.py) to create beautiful plots of 
your benchmarks.  No more struggling with matplotlib and latex!

![aggregate_scores](https://drive.google.com/uc?export=view&id=1q2So9V6sL8NHMtj6vL-S3KyzZi11Vfia)
![sample_efficiancy](https://drive.google.com/uc?export=view&id=1fzfFn0q54gsALRAwmqD1hRTqQIadGPoE)
![performace_profile](https://drive.google.com/uc?export=view&id=151pSR2sBluSpWiYxtq3jNX0tfE0vgAuR)

## Configuring
The project can be configured either the script itself or via [hydra](https://hydra.cc/docs/intro/). 
Each component in the project has a corresponding yaml configuration in the BenchMARL 
[conf](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/conf) tree. 
Components' configurations are loaded from these files into python dataclasses that act as schemas for 
validation of parameter names and types. That way we keep the best of both words: separation of all 
configuration from code and strong typing for validation! You can also directly load and validate 
configuration yaml files without using hydra from a script by calling `ComponentConfig.get_from_yaml()`.

Here are some examples on how you can override configurations:

#### Experiments

```bash
python benchmarl/run.py task=vmas/balance algorithm=mappo experiment.lr=0.03 experiment.evaluation=true experiment.train_device="cpu"
```

#### Algorithms

```bash
python benchmarl/run.py task=vmas/balance algorithm=masac algorithm.num_qvalue_nets=3 algorithm.target_entropy=auto algorithm.share_param_critic=true
```

#### Tasks 
Be careful, for benchmarking stability this is not suggested.

```bash
python benchmarl/run.py task=vmas/balance algorithm=mappo task.n_agents=4
```

#### Models

```bash
python benchmarl/run.py task=vmas/balance algorithm=mappo model=sequence "model.intermediate_sizes=[256]" "model/layers@model.layers.l1=mlp" "model/layers@model.layers.l2=mlp" "+model/layers@model.layers.l3=mlp" "model.layers.l3.num_cells=[3]"
```

Check out the [section on how to configure BenchMARL](https://github.com/facebookresearch/BenchMARL#configuring) and
our [examples](https://github.com/facebookresearch/BenchMARL/tree/main/examples/configuring).


## Extending
One of the core tenets of BenchMARL is allowing users to leverage the existing algorithm
and tasks implementations to benchmark their newly proposed solution.

For this reason we expose standard interfaces with simple abstract methods
for [algorithms](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/algorithms/common.py),
[tasks](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/environments/common.py) and
[models](https://github.com/facebookresearch/BenchMARL/tree/main/benchmarl/models/common.py).
To introduce your solution in the library, you just need to implement the abstract methods
exposed by these base classes which use objects from the [TorchRL](https://github.com/pytorch/rl) library.

Here is an [example on how you can create a custom algorithm](https://github.com/facebookresearch/BenchMARL/tree/main/examples/extending/algorithm).

Here is an [example on how you can create a custom task](https://github.com/facebookresearch/BenchMARL/tree/main/examples/extending/task).

Here is an [example on how you can create a custom model](https://github.com/facebookresearch/BenchMARL/tree/main/examples/extending/model).

# Next steps
BenchMARL is just born and is constantly looking for collaborators to extend and improve its capabilities.
**If you are interested in joining the project, please reach out!**

The next steps will include extending the library as well as fine-tuning sets of benchmark hyperparameters 
to make them available to the community.
