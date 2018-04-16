.. image:: https://img.shields.io/badge/License-Apache%202.0-yellow.svg
   :target: https://opensource.org/licenses/Apache-2.0
   
.. image:: https://travis-ci.org/StatisKit/FDDPLNG18.svg?branch=master
   :target: https://travis-ci.org/StatisKit/FDDPLNG18
  
.. image:: https://ci.appveyor.com/api/projects/status/bwc7elajp21arif0/branch/master?svg=true
   :target: https://ci.appveyor.com/project/pfernique/FDDPLNG18/branch/master

Computational studies for the article entitled "A spatio-temporal and multiscale characterization of tree development based on patchiness"
==========================================================================================================================================

This repository contains supplementary material for the reproducibiliy of computational studies performed in the article A spatio-temporal and multiscale characterization of tree development based on patchiness" written by:

* Pierre Fernique,
* Anaëlle Dambreville,
* Jean-Baptiste Durand,
* Christophe Pradal,
* Pierre-Éric Lauri,
* Frédéric Normand,
* Yann Guédon.

This article has been presented in the "Functional-Structural Plant Growth Modeling, Simulation, Visualization and Applications (FSPMA)" conference.
Here is the the citation formated as the bibtex standart.

.. code-block:: bibtex

   @inproceedings{
      FDDPLNG18,
      title={Characterization of mango tree patchiness using a tree-segmentation/clustering approach},
      author={Fernique, Pierre and Dambreville, Ana{\"e}ile and Durand, Jean-Baptiste and Pradal, Christophe and Lauri, Pierre-{\'E}ric and Normand, Fr{\'e}d{\'e}ric and Gu{\'e}don, Yann},
      booktitle={Functional-Structural Plant Growth Modeling, Simulation, Visualization and Applications (FSPMA), International Conference on},
      pages={68--74},
      year={2016},
      organization={IEEE}
    }

These studies are formatted as pre-executed **Jupyter** `notebooks <https://jupyter.readthedocs.io/en/latest/index.html>`_.
Refers to the `index.ipynb <share/jupyter/index.ipynb>`_ notebook which presents and references each study.

Test it !
=========

To reproduce the studies with **Docker** use these `images <https://hub.docker.com/r/statiskit/fddplng18/tags>`_.
After `installing <https://docs.docker.com/engine/installation/>`_ **Docker**, you can type the following command in a shell:

.. code-block:: console

   docker run -i -t -p 8888:8888 statiskit/fddplng18:v1.0.0-py3k
  
Then, follow the given instructions.
  
.. note::

    These images correspond to the ones used for the article.
    Most recent images can be runned using the following command in a shell:

    * For the *Python 3* version 

      .. code-block:: console

        docker run -i -t -p 8888:8888 statiskit/fddplng18:latest-py3k
    
Install it !
============
  
You can also install required packages on your computer to reproduce these studies.
In order to ease the installation of these packages on multiple operating systems, the **Conda** `package and environment management system <https://conda.io/docs/>`_ is used.
For more information refers to the **StatisKit** software suite documentation concerning prerequisites to the `installation <http://statiskit.readthedocs.io/en/latest/user/install_it.html>`_ step.
Then, to install the required packages, proceed as as follows:

1. Clone this repository,

   .. code:: console
   
     git clone --recursive https://github.com/StatisKit/FDDPLNG18
     
2. Create a **Conda** environment containing the meta-package :code:`fddplng18`,
       
   .. code:: console

      conda create -n fddplng18 fddplng18=1.0.0 -c statiskit -c defaults --override-channels

   .. note::

     This meta-package corresponds to the one used for the article.
     Most recent meta-package can be installed by replacing :code:`fddplng18=1.0.0` by :code:`fddplng18` in previous command lines.
     Moreover, if you replace the :code:`statiskit` channel by the :code:`statiskit/label/unstable` channel, you will benefit from the latest meta-package available that has not yet been released.
     
3. Activate the **Conda** environment as advised in your terminal.

4. Enter the directory containing **Jupyter** notebooks,

   .. code:: console
   
     cd FDDPLNG18
     cd share
     cd jupyter
     
5. Launch the **Jupyter** the `index.ipynb <jupyter/index.ipynb>`_ notebook,

   .. code:: console

     jupyter notebook index.ipynb
     
6. Execute the `index.ipynb <share/jupyter/index.ipynb>`_ notebook to execute all examples or navigate among referenced notebooks to execute them separatly.