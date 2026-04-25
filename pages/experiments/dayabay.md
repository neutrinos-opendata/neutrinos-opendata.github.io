---
permalink: /experiments/dayabay.html
layout: experiment
title: Daya Bay
short_description: "Reactor antineutrino oscillation experiment in southern China"
experiment_photo: /assets/images/experiments/dayabay.jpg
photo_credit: "Roy Kaltschmidt / Lawrence Berkeley National Laboratory, U.S. DOE (public domain)"
energy_range: "2–8 MeV"
status: completed
open_data_links:
  - label: "Full dataset 2011–2020 (Zenodo)"
    url: https://zenodo.org/records/17587229
---

Daya Bay was a reactor antineutrino experiment located near the Daya Bay and Ling Ao
nuclear power plants in Guangdong, southern China. It operated from 2011 to 2020 and
made the world's most precise measurement of the neutrino mixing angle θ₁₃, announcing
its discovery in March 2012.

The experiment deployed eight functionally identical cylindrical antineutrino detectors —
each containing 20 tonnes of gadolinium-doped liquid scintillator surrounded by mineral
oil and a layer of undoped liquid scintillator — at three underground experimental halls:
two near halls close to the reactor cores and one far hall at ~1.6–1.9 km baseline.
Antineutrinos were detected via inverse beta decay (IBD): ν̄e + p → e⁺ + n, producing a
coincident signal of a prompt positron annihilation followed by neutron capture on
gadolinium. The gadolinium doping provided a distinctive ~8 MeV gamma cascade that
suppressed backgrounds.

Over its full data-taking period of 3158 days, Daya Bay recorded 5.55 million nGd IBD
events — the largest reactor neutrino dataset ever collected. The experiment measured
sin²(2θ₁₃) = 0.0851 ± 0.0024, resolving a long-standing ambiguity in the neutrino
mixing matrix and establishing the viability of reactor-based searches for the CP
violation phase δCP.

The complete Daya Bay open dataset (2011–2020) is released on Zenodo and includes
tabular event data in HDF5, NPZ, and ROOT formats, metadata, and an analysis dataset
containing IBD candidates together with all inputs needed for oscillation fits. A Python
analysis package (dayabay-model) and fit scripts are available on GitHub.
