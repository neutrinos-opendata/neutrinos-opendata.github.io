---
permalink: /experiments/pilarnet.html
layout: experiment
title: PILArNet
short_description: "Open benchmark simulation dataset for LArTPC reconstruction and AI/ML development"
energy_range: "50–1000 MeV (kinetic energy)"
status: running
open_data_links:
  - label: "Dataset paper (arXiv:2006.01993)"
    url: https://arxiv.org/abs/2006.01993
  - label: "Labeled dataset (OSF)"
    url: https://osf.io/2dpv8/
---

PILArNet is an open benchmark simulation dataset designed to support machine learning
and reconstruction algorithm development for liquid argon time projection chambers
(LArTPCs). It is not associated with a single running experiment but rather provides a
clean, model-independent simulation environment usable across the LArTPC community.

The dataset contains 300,000 simulated particle gun events generated with
model-independent particle generators (MPV for single particles, MPR for multi-particle
events) and full Geant4 detector simulation. Three detector volumes are provided —
192³, 512³, and 768³ voxels — to support studies at different detector scales. Energy
depositions are stored in sparse 2D/3D voxel representations using the LArCV data format,
with two complementary data products: energy-3D (energy deposition per voxel) and
segment-3D (ground-truth particle category label per voxel). A simplified detector
response model is applied (no full electronics simulation; spatial smearing only), making
the dataset well-controlled for algorithm benchmarking.

Five particle categories are covered: protons, minimum-ionizing particles (MIPs: muons
and charged pions), electromagnetic particles (EM: electrons and photons), Michel
electrons, and delta rays. Particle multiplicities and kinetic energies are sampled
within configurable ranges (50–1000 MeV for most categories, 50–400 MeV for protons).

PILArNet supports a range of core reconstruction tasks: semantic segmentation (per-voxel
particle type classification), instance segmentation (grouping voxels into individual
particles), kinematic regression (particle energy and direction), vertex reconstruction,
and 2D-to-3D reconstruction. Its ground-truth labels and clean simulation make it
particularly useful for training and benchmarking supervised deep learning models before
applying them to real detector data.
