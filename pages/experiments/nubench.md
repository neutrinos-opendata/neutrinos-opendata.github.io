---
permalink: /experiments/nubench.html
layout: experiment
title: NuBench
short_description: "Open benchmark simulation dataset for Cherenkov neutrino telescope reconstruction"
status: running
open_data_links:
  - label: "Dataset paper (arXiv:2511.13111)"
    url: https://arxiv.org/abs/2511.13111
  - label: "Benchmark tasks and model implementations (GitHub)"
    url: https://github.com/nubench
---

NuBench is an open benchmark dataset for the development and evaluation of reconstruction
algorithms for Cherenkov neutrino telescopes, analogous in spirit to PILArNet for LArTPC
detectors. It provides a common, well-documented simulation framework that allows the
community to train and compare machine learning models on a shared dataset without
requiring access to proprietary experimental data.

The dataset represents neutrino events in a large-volume Cherenkov detector through
detector hit records in multiple complementary representations: graph and point-cloud
formats suited to geometric deep learning (e.g. graph neural networks), and tabular
formats for classical methods. Data are stored in Parquet and SQLite formats and hosted
on ERDA (Electronic Research Data Archive).

NuBench is designed around a set of benchmark reconstruction tasks that map onto the
core challenges in Cherenkov neutrino telescope physics: event classification, energy
reconstruction, direction reconstruction, and particle identification. Reference model
implementations based on GraphNeT — a framework for graph neural network-based
reconstruction in neutrino telescopes — are provided on GitHub together with data
loaders and training scripts, enabling reproducible comparisons across methods.

Documentation is available via the dataset paper on arXiv and supplementary material
on GitHub.
