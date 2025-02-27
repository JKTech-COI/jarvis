<div align="center" style="text-align: center">

<p style="text-align: center">
  <img align="center" src="docs/JARVIS(J with Name).png" width="250px">
</p>

**[JARVIS](https://clear.ml) - Auto-Magical Suite of tools to streamline your ML workflow
</br>Experiment Manager, MLOps and Data-Management**

<!-- [![GitHub license](https://img.shields.io/github/license/allegroai/jarvis.svg)](https://img.shields.io/github/license/allegroai/jarvis.svg) [![PyPI pyversions](https://img.shields.io/pypi/pyversions/jarvis.svg)](https://img.shields.io/pypi/pyversions/jarvis.svg) [![PyPI version shields.io](https://img.shields.io/pypi/v/jarvis.svg)](https://pypi.org/project/jarvis/) [![Conda version shields.io](https://img.shields.io/conda/v/jarvis/jarvis)](https://anaconda.org/jarvis/jarvis) [![Optuna](https://img.shields.io/badge/Optuna-integrated-blue)](https://optuna.org)<br>
[![PyPI Downloads](https://pepy.tech/badge/jarvis/month)](https://pypi.org/project/jarvis/) [![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/allegroai)](https://artifacthub.io/packages/search?repo=allegroai) [![Youtube](https://img.shields.io/badge/JARVIS-DD0000?logo=youtube&logoColor=white)](https://www.youtube.com/c/jarvis) [![Slack Channel](https://img.shields.io/badge/slack-%23jarvis--community-blueviolet?logo=slack)](https://join.slack.com/t/jarvis/shared_invite/zt-1kvcxu5hf-SRH_rmmHdLL7l2WadRJTQg) [![Signup](https://img.shields.io/badge/Clear%7CML-Signup-brightgreen)](https://app.clear.ml) -->

</div>

---
### JARVIS

JARVIS is a ML/DL development and production suite, it contains FOUR main modules:

- [Experiment Manager](#jarvis-experiment-manager) - Automagical experiment tracking, environments and results
- [MLOps](https://github.com/allegroai/jarvis-agent) - Orchestration, Automation & Pipelines solution for ML/DL jobs (K8s / Cloud / bare-metal)  
- [Data-Management](https://github.com/allegroai/jarvis/blob/master/docs/datasets.md) - Fully differentiable data management & version control solution on top of object-storage 
  (S3 / GS / Azure / NAS)  
-  **NEW**  :fire: [Model-Serving](https://github.com/allegroai/jarvis-serving) :tada: - *cloud-ready* Scalable model serving solution! <br>:sparkles: **Deploy new model endpoints in under 5 minutes** :sparkles: <br> :muscle: includes optimized GPU serving support backed by Nvidia-Triton :mechanical_arm: <br> :bar_chart: **with out-of-the-box  Model Monitoring** :scream:

  

Instrumenting these components is the **JARVIS-server**, see [Self-Hosting](https://clear.ml/docs/latest/docs/deploying_jarvis/jarvis_server) & [Free tier Hosting](https://app.clear.ml)  


---
<!-- <div align="center">

**[Sign up](https://app.clear.ml)  &  [Start using](https://clear.ml/docs/) in under 2 minutes**  

</div>

---
<a href="https://app.clear.ml"><img src="https://github.com/allegroai/jarvis/blob/master/docs/webapp_screenshots.gif?raw=true" width="100%"></a> -->

## JARVIS Experiment Manager

**Adding only 2 lines to your code gets you the following**

* Complete experiment setup log
    * Full source control info including non-committed local changes
    * Execution environment (including specific packages & versions)
    * Hyper-parameters
        * ArgParser/[Click](https://github.com/pallets/click/) for command line parameters with currently used values
        * Explicit parameters dictionary
        * Tensorflow Defines (absl-py)
        * [Hydra](https://github.com/facebookresearch/hydra) configuration and overrides
    * Initial model weights file
* Full experiment output automatic capture
    * stdout and stderr
    * Resource Monitoring (CPU/GPU utilization, temperature, IO, network, etc.)
    * Model snapshots (With optional automatic upload to central storage: Shared folder, S3, GS, Azure, Http)
    * Artifacts log & store (Shared folder, S3, GS, Azure, Http)
    * Tensorboard/[TensorboardX](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/tensorboardx) scalars, metrics, histograms, **images, audio and video samples**
    * [Matplotlib & Seaborn](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/matplotlib)
    * [JARVIS Logger](https://clear.ml/docs/latest/docs/fundamentals/logger) interface for complete flexibility.
* Extensive platform support and integrations
    * Supported ML/DL frameworks: [PyTorch](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/pytorch) (incl' [ignite](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/ignite) / [lightning](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/pytorch-lightning)), [Tensorflow](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/tensorflow), [Keras](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/keras), [AutoKeras](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/autokeras), [FastAI](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/fastai), [XGBoost](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/xgboost), [LightGBM](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/lightgbm), [MegEngine](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/megengine) and [Scikit-Learn](https://github.com/allegroai/jarvis/tree/master/examples/frameworks/scikit-learn)
    * Seamless integration (including version control) with [**Jupyter Notebook**](https://jupyter.org/)
    and [*PyCharm* remote debugging](https://github.com/allegroai/trains-pycharm-plugin)
      
#### [Start using JARVIS](https://clear.ml/docs/latest/docs/getting_started/ds/ds_first_steps) 


1. Sign up for free to the [JARVIS Hosted Service](https://app.clear.ml) (alternatively, you can set up your own server, see [here](https://clear.ml/docs/latest/docs/deploying_jarvis/jarvis_server)).

    > **_jarvis Demo Server:_** JARVIS no longer uses the demo server by default. To enable the demo server, set the `jarvis_NO_DEFAULT_SERVER=0`
    > environment variable. Credentials aren't needed, but experiments launched to the demo server are public, so make sure not 
    > to launch sensitive experiments if using the demo server.

1. Install the `jarvis` python package:

    ```bash
    pip install jarvis
    ```

1. Connect the JARVIS SDK to the server by [creating credentials](https://app.clear.ml/settings/workspace-configuration), then execute the command
below and follow the instructions: 

    ```bash
    jarvis-init
    ```

1. Add two lines to your code:
    ```python
    from jarvis import Task
    task = Task.init(project_name='examples', task_name='hello world')
    ```

You are done, everything your process outputs is now automagically logged into JARVIS.

Next step, automation! **Learn more about JARVIS's two-click automation [here](https://clear.ml/docs/latest/docs/getting_started/mlops/mlops_first_steps)**. 

## JARVIS Architecture

The JARVIS run-time components:

* The JARVIS Python Package for integrating JARVIS into your existing scripts by adding just two lines of code, and optionally extending your experiments and other workflows with JARVIS powerful and versatile set of classes and methods.
* The JARVIS Server storing experiment, model, and workflow data, and supporting the Web UI experiment manager, and ML-Ops automation for reproducibility and tuning. It is available as a hosted service and open source for you to deploy your own JARVIS Server.
* The JARVIS Agent for ML-Ops orchestration, experiment and workflow reproducibility, and scalability.

<img src="https://raw.githubusercontent.com/allegroai/jarvis-docs/main/docs/img/jarvis_architecture.png" width="100%" alt="jarvis-architecture">

<!-- ## Additional Modules 

- [jarvis-session](https://github.com/allegroai/jarvis-session) - **Launch remote JupyterLab / VSCode-server inside any docker, on Cloud/On-Prem machines**
- [jarvis-task](https://github.com/allegroai/jarvis/blob/master/docs/jarvis-task.md) - Run any codebase on remote machines with full remote logging of Tensorboard, Matplotlib & Console outputs 
- [jarvis-data](https://github.com/allegroai/jarvis/blob/master/docs/datasets.md) - **CLI for managing and versioning your datasets, including creating / uploading / downloading of data from S3/GS/Azure/NAS** 
- [AWS Auto-Scaler](https://clear.ml/docs/latest/docs/guides/services/aws_autoscaler) - Automatically spin EC2 instances based on your workloads with preconfigured budget! No need for K8s!
- [Hyper-Parameter Optimization](https://clear.ml/docs/latest/docs/guides/optimization/hyper-parameter-optimization/examples_hyperparam_opt) - Optimize any code with black-box approach and state of the art Bayesian optimization algorithms 
- [Automation Pipeline](https://clear.ml/docs/latest/docs/guides/pipeline/pipeline_controller) - Build pipelines based on existing experiments / jobs, supports building pipelines of pipelines!  
- [Slack Integration](https://clear.ml/docs/latest/docs/guides/services/slack_alerts) - Report experiments progress / failure directly to Slack (fully customizable!)   -->

## Why JARVIS?

JARVIS is our solution to a problem we share with countless other researchers and developers in the machine
learning/deep learning universe: Training production-grade deep learning models is a glorious but messy process.
JARVIS tracks and controls the process by associating code version control, research projects,
performance metrics, and model provenance.

We designed JARVIS specifically to require effortless integration so that teams can preserve their existing methods
and practices. 

  - Use it on a daily basis to boost collaboration and visibility in your team 
  - Create a remote job from any experiment with a click of a button
  - Automate processes and create pipelines to collect your experimentation logs, outputs, and data
  - Store all you data on any object-storage solution, with the simplest interface possible
  - Make you data transparent by cataloging it all on the JARVIS platform    

We believe JARVIS is ground-breaking. We wish to establish new standards of true seamless integration between
experiment management,ML-Ops and data management. 

<!-- ## Who We Are

JARVIS is supported by the team behind [clear.ml](https://clear.ml),
where we build deep learning pipelines and infrastructure for enterprise companies.

We built JARVIS to track and control the glorious but messy process of training production-grade deep learning models.
We are committed to vigorously supporting and expanding the capabilities of JARVIS.

We promise to always be backwardly compatible, making sure all your logs, data and pipelines 
will always upgrade with you. -->

<!-- ## License

Apache License, Version 2.0 (see the [LICENSE](https://www.apache.org/licenses/LICENSE-2.0.html) for more information)

If JARVIS is part of your development process / project / publication, please cite us :heart: : 
```
@misc{jarvis,
title = {JARVIS - Your entire MLOps stack in one open-source tool},
year = {2019},
note = {Software available from http://github.com/allegroai/jarvis},
url={https://clear.ml/},
author = {JARVIS},
}
```

## Documentation, Community & Support

More information in the [official documentation](https://clear.ml/docs) and [on YouTube](https://www.youtube.com/c/JARVIS).

For examples and use cases, check the [examples folder](https://github.com/allegroai/jarvis/tree/master/examples) and [corresponding documentation](https://clear.ml/docs/latest/docs/guides).

If you have any questions: post on our [Slack Channel](https://join.slack.com/t/jarvis/shared_invite/zt-1kvcxu5hf-SRH_rmmHdLL7l2WadRJTQg
), or tag your questions on [stackoverflow](https://stackoverflow.com/questions/tagged/jarvis) with '**[jarvis](https://stackoverflow.com/questions/tagged/jarvis)**' tag (*previously [trains](https://stackoverflow.com/questions/tagged/trains) tag*).

For feature requests or bug reports, please use [GitHub issues](https://github.com/allegroai/jarvis/issues).

Additionally, you can always find us at *info@clear.ml*

## Contributing

**PRs are always welcome** :heart: See more details in the JARVIS [Guidelines for Contributing](https://github.com/allegroai/jarvis/blob/master/docs/contributing.md).


_May the force (and the goddess of learning rates) be with you!_ -->
