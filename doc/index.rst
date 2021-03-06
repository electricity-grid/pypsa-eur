PyPSA-Eur: An Open Optimisation Model of the European Transmission System
=========================================================================

.. image:: https://img.shields.io/github/v/release/pypsa/pypsa-eur?include_prereleases
    :alt: GitHub release (latest by date including pre-releases)
    
.. image:: https://travis-ci.org/PyPSA/pypsa-eur.svg?branch=master
    :target: https://travis-ci.org/PyPSA/pypsa-eur

.. image:: https://readthedocs.org/projects/pypsa-eur/badge/?version=latest
    :target: https://pypsa-eur.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status

.. image:: https://img.shields.io/github/license/pypsa/pypsa-eur
    :alt: GitHub

.. image:: https://img.shields.io/github/repo-size/pypsa/pypsa-eur
    :alt: GitHub repo size

.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.3520875.svg
    :target: https://doi.org/10.5281/zenodo.3520875

.. image:: https://badges.gitter.im/PyPSA/community.svg
    :target: https://gitter.im/PyPSA/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge
    :alt: Chat on Gitter

PyPSA-Eur is an open model dataset of the European power system at the
transmission network level that covers the full ENTSO-E area.

It contains alternating current lines at and above 220 kV voltage level and all high voltage direct current lines, substations, an open database of conventional power plants, time series for electrical demand and variable renewable generator availability, and geographic potentials for the expansion of wind and solar power.

The model is suitable both for operational studies and generation and transmission expansion planning studies. The continental scope and highly resolved spatial scale enables a proper description of the long-range smoothing effects for renewable power generation and their varying resource availability.

.. image:: img/base.png

The restriction to freely available and open data encourages the open exchange of model data developments and eases the comparison of model results. It provides a full, automated software pipeline to assemble the load-flow-ready model from the original datasets, which enables easy replacement and improvement of the individual parts.

PyPSA-Eur is designed to be imported into the open toolbox `PyPSA <https://www.pypsa.org>`_ for which `documentation <https://pypsa.org/doc>`_ is available as well.

This project is maintained by the `Energy System Modelling group <https://www.iai.kit.edu/english/2338.php>`_ at the `Institute for Automation and Applied Informatics <https://www.iai.kit.edu/english/index.php>`_ at the `Karlsruhe Institute of Technology <http://www.kit.edu/english/index.php>`_. The group is funded by the `Helmholtz Association <https://www.helmholtz.de/en/>`_ until 2024. Previous versions were developed by the `Renewable Energy Group <https://fias.uni-frankfurt.de/physics/schramm/renewable-energy-system-and-network-analysis/>`_ at `FIAS <https://fias.uni-frankfurt.de/>`_ to carry out simulations for the `CoNDyNet project <http://condynet.de/>`_, financed by the `German Federal Ministry for Education and Research (BMBF) <https://www.bmbf.de/en/index.html>`_ as part of the `Stromnetze Research Initiative <http://forschung-stromnetze.info/projekte/grundlagen-und-konzepte-fuer-effiziente-dezentrale-stromnetze/>`_.

Documentation
=============

**Getting Started**

* :doc:`introduction`
* :doc:`installation`
* :doc:`tutorial`

.. toctree::
   :hidden:
   :maxdepth: 1
   :caption: Getting Started

   introduction
   installation
   tutorial

**Configuration**

* :doc:`wildcards`
* :doc:`configuration`
* :doc:`costs`

.. toctree::
   :hidden:
   :maxdepth: 1
   :caption: Configuration

   wildcards
   configuration
   costs

**Rules Overview**

* :doc:`preparation`
* :doc:`simplification`
* :doc:`solving`
* :doc:`plotting`

.. toctree::
   :hidden:
   :maxdepth: 1
   :caption: Rules Overview

   preparation
   simplification
   solving
   plotting
   
**References**
   
* :doc:`release_notes`
* :doc:`limitations`
* :doc:`contributing`

.. toctree::
   :hidden:
   :maxdepth: 1
   :caption: References

   release_notes
   limitations
   contributing

Learning Energy System Modelling
================================

If you are (relatively) new to energy system modelling and optimisation
and plan to use PyPSA-Eur, the following resources are *one way* to get started
in addition to reading this documentation.

- Documentation of `PyPSA <https://pypsa.readthedocs.io>`_, the package for
  simulating and optimising modern power systems which PyPSA-Eur uses under the hood.
- Course on `Energy System Modelling <https://nworbmot.org/courses/esm-2019/>`_,
  Karlsruhe Institute of Technology (KIT), `Dr. Tom Brown <https://nworbmot.org>`_

Citing PyPSA-Eur
================

If you use PyPSA-Eur for your research, we would appreciate it if you would cite the following paper:

- Jonas Hörsch, Fabian Hofmann, David Schlachtberger, and Tom Brown. `PyPSA-Eur: An open optimisation model of the European transmission system <https://arxiv.org/abs/1806.01613>`_. Energy Strategy Reviews, 22:207-215, 2018. `arXiv:1806.01613 <https://arxiv.org/abs/1806.01613>`_, `doi:10.1016/j.esr.2018.08.012 <https://doi.org/10.1016/j.esr.2018.08.012>`_.

Please use the following BibTeX: ::

    @article{PyPSAEur,
        author = "Jonas Hoersch and Fabian Hofmann and David Schlachtberger and Tom Brown",
        title = "PyPSA-Eur: An open optimisation model of the European transmission system",
        journal = "Energy Strategy Reviews",
        volume = "22",
        pages = "207 - 215",
        year = "2018",
        issn = "2211-467X",
        doi = "10.1016/j.esr.2018.08.012",
        eprint = "1806.01613"
    }


If you want to cite a specific PyPSA-Eur version, each release of PyPSA-Eur is stored on Zenodo with a release-specific DOI.
This can be found linked from the overall PyPSA-Eur Zenodo DOI:

.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.3520875.svg
   :target: https://doi.org/10.5281/zenodo.3520875

Pre-Built Networks as a Dataset
===============================

There are pre-built networks available as a dataset on Zenodo as well for every release of PyPSA-Eur.

.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.3601882.svg
   :target: https://doi.org/10.5281/zenodo.3601882

The included ``.nc`` files are PyPSA network files which can be imported with PyPSA via:

.. code:: python
    
    import pypsa

    filename = "elec_s_1024_ec.nc" # example
    n = pypsa.Network(filename)

Licence
=======

The code in PyPSA-Eur is released as free software under the `GPLv3
<http://www.gnu.org/licenses/gpl-3.0.en.html>`_, see
`LICENSE <https://github.com/PyPSA/pypsa-eur/blob/master/LICENSE.txt>`_.
However, different licenses and terms of use apply to the various input data, which are summarised below.
More details are included in 
`the description of the data bundles on zenodo <https://zenodo.org/record/3517935#.XbGeXvzRZGo>`_.

.. csv-table::
   :header-rows: 1
   :file: configtables/licenses.csv

* *BY: Attribute Source*
* *NC: Non-Commercial Use Only*
* *SA: Share Alike*
