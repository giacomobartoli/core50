<img src="http://i.imgur.com/2UyfKHs.png?1" width="80" align="left">

# CORe50 

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![built with Python2.7](https://img.shields.io/badge/build%20with-python2.7-red.svg)](https://www.python.org/)
[![built with Caffe](https://img.shields.io/badge/build%20with-caffe-brightgreen.svg)](http://caffe.berkeleyvision.org/)
[![built with Sacred](https://img.shields.io/badge/build%20with-sacred-yellow.svg)](https://github.com/IDSIA/sacred)

## A new Dataset and Benchmark for Continuous Object Recognition

----------------------------------------------

#### *WARNING: This repository is still under construction!*

- [x] CORe50 core code-base
- [x] CORe50 benchmark configuration files
- [x] Easy-to-access results data and baches configurations
- [ ] **Easy-setup and getting started** (in progress...)
- [ ] Reproducibility tests

In this page we provide the code and all the materials related to the **CORe50** 
benchmark. If you plan to use this dataset or other resources you'll find in this page, please **cite our [latest paper](https://arxiv.org/abs/1705.03550)**: 

	@article{lomonaco2017core50,
       title={CORe50: a New Dataset and Benchmark for Continuous Object Recognition},
       author={Lomonaco, Vincenzo and Maltoni, Davide},
       journal={arXiv preprint arXiv:1705.03550},
       year={2017}
	}

You can find more information about the dataset and benchmark at as well as additional data to download at: 
[vlomonaco.github.io/core50](http://vlomonaco.github.io/core50).

----------------------------------------------

## Dependencies

In order to extecute the code in the repository you'll need to install the following dependencies in a [Python 2.7](https://www.python.org/) environment:

* [Numpy](https://pypi.python.org/pypi/numpy/1.6.1): _Matrices operations and stuff_

```bash
pip install numpy
```

* [Sacred](https://github.com/IDSIA/sacred): _Experiments Manager_

```bash
pip install sacred
```

* [Caffe](http://caffe.berkeleyvision.org/): _Actual DL back-end (easily interchangeable)_

Follow the step-by-step guide for installing caffe [here](http://caffe.berkeleyvision.org/installation.html). 

----------------------------------------------

## Project Structure
Up to now the projects is structured as follows:

- [`confs/`](confs): In this folder you can find all the experiments configurations and the caffe definition files. sI, sII and sIII stand for the NI, NC and NIC scenarios, respectively.
- [`core/`](core): The actual code of the benchmark.
- [`data/`](data): Void at first. After the setup it will be filled with data needed for the experiments. It will also be used for storing partial computations.
- [`extras/`](extras): Results and configuration files you can download without delving into the code.
- [`scripts/`](scripts): Currently void. It will contain useful scripts to help you downloading the necessary extra materials. Bash scripts will be updated soon for running the benchmark without much pain.
- [`LICENSE`](LICENSE): Standard Creative Commons Attribution 4.0 International License.
- [`README.md`](README.md): This instructions file.
- [`run_sI_exps.sh`](run_sI_exps.sh): Simple bash script for running the "New Instances (NI)" experiments with the different architectures and strategies
- [`run_sII_exps.sh`](run_sII_exps.sh): Simple bash script for running the "New Classes (NC)" experiments with the different architectures and strategies
- [`run_sIII_exps.sh`](run_sIII_exps.sh): Simple bash script for running the "New Instances and Classes (NIC)" experiments with the different architectures and strategies

----------------------------------------------

## Getting Started

In order to run the experiments and reproduce the benchmark first of all we need to download the pre-trained models and the CORe50 dataset. This can be automatically done using the script provided:

```bash
./scripts/fetch_data.sh
```

All the data will be downloaded in the [`data/`](data) directory. After this initial step you can directly run the experiments with the bash scripts [`run_sI_exps.sh`](run_sI_exps.sh), [`run_sII_exps.sh`](run_sII_expts.sh) and [`run_sIII_exps.sh`](run_sI_expts.sh) for the NI, NC and NIC scenarios respectively. 

For example, reproducing the first scenario experiments can be as easy as running:

```bash
./run_sI_exps.sh
```

Since this experiments can take a while (also more than 24h depending on the scenario) you can also disable some experiments just by commenting them in the bash script.

----------------------------------------------

## License

This work is licensed under a <a href="https://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. 

----------------------------------------------

## Author

* [Vincenzo Lomonaco](http://vincenzolomonaco.com) - email: *vincenzo.lomonaco@unibo.it*
