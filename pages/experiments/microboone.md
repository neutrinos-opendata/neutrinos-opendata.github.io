---
permalink: /experiments/microboone.html
layout: experiment
title: MicroBooNE
short_description: "Short-baseline liquid argon TPC neutrino experiment at Fermilab"
experiment_photo: /assets/images/experiments/microboone.jpg
photo_credit: "U.S. Department of Energy (public domain)"
energy_range: "0.1–2 GeV"
status: completed
open_data_links:
  - label: "Public Datasets (Fermilab)"
    url: https://microboone.fnal.gov/documents-publications/public-datasets/
  - label: "Dataset paper (arXiv:2309.15362)"
    url: https://arxiv.org/pdf/2309.15362
  - label: "Inclusive BNB sample — HDF5 (Zenodo 10.5281/zenodo.8370883)"
    url: https://zenodo.org/records/8370883
  - label: "Inclusive BNB sample with wire waveforms (Zenodo 10.5281/zenodo.7262009)"
    url: https://zenodo.org/records/7262009
  - label: "Electron neutrino sample — HDF5 (Zenodo 10.5281/zenodo.7261921)"
    url: https://zenodo.org/records/7261921
  - label: "Electron neutrino sample with wire waveforms (Zenodo 10.5281/zenodo.7262140)"
    url: https://zenodo.org/records/7262140
---

MicroBooNE (Micro Booster Neutrino Experiment) was a short-baseline neutrino experiment
at Fermilab that operated from 2015 to 2021. It used a liquid argon time projection
chamber (LArTPC) containing 170 tonnes of liquid argon (85 tonnes active mass), making
it one of the largest LArTPC detectors of its time.

The experiment studied neutrino interactions in the ~0.1–2 GeV range using the Booster
Neutrino Beam (BNB) and aimed to address the anomalous excess of electron-like events
observed by the MiniBooNE experiment, as well as to measure neutrino cross sections and
develop LArTPC technology for future experiments such as DUNE.

The MicroBooNE detector recorded ionization charge signals on three planes of sense wires
(U, V, Y) and detected scintillation light via photomultiplier tubes. The resulting data
are naturally represented as 2D wire-time images, making the experiment well-suited to
image-based deep learning techniques.

MicroBooNE released public LArTPC overlay samples to support collaborative software
development beyond the collaboration. The samples combine simulated neutrino interactions
with real off-beam data, providing realistic cosmic-ray backgrounds and detector noise.
Two data formats are provided: full art/ROOT for LArTPC experts and simplified HDF5 for
broader AI/ML users. Releases include inclusive BNB samples and intrinsic electron
neutrino samples, with optional wire-waveform content.
