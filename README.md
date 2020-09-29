# Fast Parameter Estimation of Binary Mergers for Multimessenger Followup

**Daniel Finstad<sup>1</sup>, Duncan A. Brown<sup>1</sup>**

**<sup>1</sup>Department of Physics, Syracuse University, Syracuse, NY 13244, USA**

## License

![Creative Commons License](https://i.creativecommons.org/l/by-sa/3.0/us/88x31.png "Creative Commons License")

This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 United States License](http://creativecommons.org/licenses/by-sa/3.0/us/).

## Introduction

This notebook is a companion to [] which is posted at [arxiv:](https://arxiv.org/abs/). It demonstrates how to read and use our posterior proability density files from the parameter estimation and shows how in principle to reconstruct Figure 3 in the paper from the raw data.

We encourage use of these data in derivative works.

The data provided contain the posterior samples from a selection of the simulated binary neutron star and neutron star--black hole signals recovered by our analysis. These data are stored in the files contained in [bns_posteriors](https://github.com/sugwg/rapid-relbin-pe/bns_posteriors) for binary neutron star signals, and [nsbh_posteriors](https://github.com/sugwg/rapid-relbin-pe/nsbh_posteriors) for neutron star--black hole signals. The notebook [data_release_companion.ipynb](https://github.com/sugwg/rapid-relbin-pe/blob/master/data_release_companion.ipynb) contains a demonstration of retrieving posterior samples from the data files and plotting the results shown in Figure 3 of the paper.

The results used in the paper were generated with the [PyCBC v1.16.9 release.](https://github.com/gwastro/pycbc/releases/tag/v1.16.9)

## Runing this notebook in a Docker container

This notebook can be run from a PyCBC Docker container, or a machine with PyCBC installed. Instructions for [downloading the docker container](http://gwastro.github.io/pycbc/latest/html/docker.html) are available from the [PyCBC home page.](https://pycbc.org/) To start a container with instance of Jupyter notebook, run the commands
```sh
docker pull pycbc/pycbc-el7:v1.16.9
docker run -p 8888:8888 --name pycbc_notebook -it pycbc/pycbc-el7:v1.16.9 /bin/bash -l
```
Once the container has started, this git repository can be downloaded with the command:
```sh
git clone https://github.com/sugwg/rapid-relbin-pe.git
```
The notebook server can be started inside the container with the command:
```sh
jupyter notebook --ip 0.0.0.0 --no-browser
```
You can then connect to the notebook server at the URL printed by ``jupyter``. Navigate to the directory `rapid-relbin-pe` in the cloned git repository and open [data_release_companion.ipynb](https://github.com/sugwg/rapid-relbin-pe/blob/master/data_release_companion.ipynb), the notebook that demonstrates use of these reults.

## Acknowledgements
We thank Brian Metzger, Ben Margalit, and Edo Berger for helpful discussions. DAB thanks the Kavli Institute for Theoretical Physics for their hospitality.

### Funding

This work was supported by U.S. National Science Foundation Grant No. PHY-1707954 and PHY-2011655. Computational work was supported by Syracuse University and National Science Foundation award OAC-1541396. DAB received partial support from the Kavli Institute for Theoretical Physics which is supported by the National Science Foundation award PHY-1748958.

### Authors contributions:
Conceptualization, DAB and DF; Methodology, DAB and DF; Software: DF; Formal Analysis: DF; Investigation: DF; Resources: DAB; Writing – Original Draft: DF; Writing – Review and Editing: DAB and DF; Visualization: DF; Supervision: DAB; Project Administration: DAB; Funding Acquisition: DAB.

