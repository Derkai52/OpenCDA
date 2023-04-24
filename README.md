# OpenCDA
[![Build Status](https://travis-ci.com/ucla-mobility/OpenCDA.svg?branch=develop)](https://travis-ci.com/ucla-mobility/OpenCDA)
[![Coverage Status](https://coveralls.io/repos/github/ucla-mobility/OpenCDA/badge.svg?branch=feature/readme_revise)](https://coveralls.io/github/ucla-mobility/OpenCDA?branch=feature/readme_revise)
[![Documentation Status](https://readthedocs.org/projects/opencda-documentation/badge/?version=latest)](https://opencda-documentation.readthedocs.io/en/latest/?badge=latest)


OpenCDA is an open co-simulation-based **research/engineering framework** integrated with prototype cooperative driving automation (CDA; see [SAE J3216](https://www.sae.org/standards/content/j3216_202005/)) pipelines as well as regular automated driving components (e.g., perception, localization, planning, control).  It not only enables CDA evaluation in a CARLA + SUMO co-simulation environment but also provides a rich library of source codes of CDA research pipelines. 

The key features of OpenCDA are:
* <strong> Research Pipeline </strong>: OpenCDA provides rich research pipelines (i.e., open-source codes for basic and advanced CDA modules, such as platooning, cooperative perception).
* <strong>Integration</strong>: OpenCDA utilizes CARLA and SUMO separately, as well as integrates them together.
* <strong> Full-stack Simulation</strong>: OpenCDA provides a simple prototype automated driving and cooperative driving platform, <strong>all in Python</strong>, that contains perception, localization, planning, control, and V2X communication modules.
* <strong>Modularity</strong>: OpenCDA is highly modularized. 
* <strong>Benchmark</strong>: OpenCDA offers benchmark testing scenarios, benchmark baseline maps, state-of-the-art benchmark algorithms, and benchmark evaluation metrics.
* <strong>Connectivity and Cooperation</strong>: OpenCDA supports various levels and categories of cooperation between CAVs in simulation. This differentiates OpenCDA from other single vehicle simulation tools.


Users could refer to [OpenCDA documentation](https://opencda-documentation.readthedocs.io/en/latest/) for more details.




## Major Components
![teaser](docs/md_files/images/OpenCDA_new_diagrams.png)

OpenCDA  consists of four major component: <strong>Cooperative Driving System</strong>,  <strong>Co-Simulation Tools</strong>, <strong>Data Manager and Repository</strong>,
and  <strong>Scenario Manager</strong>.

Check the [OpenCDA Introduction](https://opencda-documentation.readthedocs.io/en/latest/md_files/introduction.html) for more details.


## Get Started

 ![teaser](docs/md_files/images/platoon_joining_2lanefree_complete.gif)


### Users Guide
* [Overview](https://opencda-documentation.readthedocs.io/en/latest/md_files/introduction.html)
* [Docker Deployment](Build.md)
* [Quick Start](https://opencda-documentation.readthedocs.io/en/latest/md_files/getstarted.html)
* [Logic Flow](https://opencda-documentation.readthedocs.io/en/latest/md_files/logic_flow.html)
* [Traffic Generation](https://opencda-documentation.readthedocs.io/en/latest/md_files/traffic_generation.html)


Note: We continuously improve the performance of OpenCDA. Currently, it is mainly tested in our customized maps and
 Carla town06 map; therefore, we <strong>DO NOT </strong> guarantee the same level of  robustness in other maps.

### Developer Guide

*  [Class Design](https://opencda-documentation.readthedocs.io/en/latest/md_files/developer_tutorial.html)
*  [Customize Your Algorithms](https://opencda-documentation.readthedocs.io/en/latest/md_files/customization.html)
*  [API Reference](https://opencda-documentation.readthedocs.io/en/latest/modules.html) <br>


### Contribution Rule
We welcome your contributions.
- Please report bugs and improvements by submitting issues.
- Submit your contributions using [pull requests](https://github.com/ucla-mobility/OpenCDA/pulls).
 Please use [this template](.github/PR_TEMPLATE.md) for your pull requests.
