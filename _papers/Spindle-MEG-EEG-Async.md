---
layout: paper
title: "Emergence of synchronous EEG spindles from asynchronous MEG spindles"
subtitle: ""
authors: "Nima Dehghani"
date: 2026-05-11
venue: "Paper"
year: 2011
image: /assets/img/papers/depth-cg-teaser.png
tags: [Spindle, Thalamocortical, Oscillation, Synchrony, Sleep, MEG, EEG]
arxiv: ""
doi: ""
pdf: "https://onlinelibrary.wiley.com/doi/epdf/10.1002/hbm.21183"
repo: "https://github.com/neurovium/depth-coarse-graining"
mirrors:
  - name: "Article page"
    url: "https://onlinelibrary.wiley.com/doi/ftr/10.1002/hbm.21183"
bibtex: |
  @article{Dehghani2011spindleAsync,
  author = {Dehghani, Nima and Cash, Sydney S. and Halgren, Eric},
  title = {Emergence of synchronous EEG spindles from asynchronous MEG spindles},
  journal = {Human Brain Mapping},
  volume = {32},
  number = {12},
  pages = {2217-2227},
  keywords = {synchrony, cortex, thalamus, inverse solution, oscillation, human, sleep, matrix, core, thalamic reticular nucleus, alpha},
  doi = {https://doi.org/10.1002/hbm.21183},
  url = {https://onlinelibrary.wiley.com/doi/abs/10.1002/hbm.21183},
  eprint = {https://onlinelibrary.wiley.com/doi/pdf/10.1002/hbm.21183},
  abstract = {Abstract Sleep spindles are bursts of rhythmic 10–15 Hz activity, lasting ∼0.5–2 s, that occur during Stage 2 sleep. They are coherent across multiple cortical and thalamic locations in animals, and across scalp EEG sites in humans, suggesting simultaneous generation across the cortical mantle. However, reports of MEG spindles occurring without EEG spindles, and vice versa, are inconsistent with synchronous distributed generation. We objectively determined the frequency of MEG-only, EEG-only, and combined MEG-EEG spindles in high density recordings of natural sleep in humans. About 50\% of MEG spindles occur without EEG spindles, but the converse is rare (∼15\%). Compared to spindles that occur in MEG only, those that occur in both MEG and EEG have ∼1\% more MEG coherence and ∼15\% more MEG power, insufficient to account for the ∼55\% increase in EEG power. However, these combined spindles involve ∼66\% more MEG channels, especially over frontocentral cortex. Furthermore, when both MEG and EEG are involved in a given spindle, the MEG spindle begins ∼150 ms before the EEG spindle and ends ∼250 ms after. Our findings suggest that spindles begin in focal cortical locations which are better recorded with MEG gradiometers than referential EEG due to the biophysics of their propagation. For some spindles, only these regions remain active. For other spindles, these locations may recruit other areas over the next 200 ms, until a critical mass is achieved, including especially frontal cortex, resulting in activation of a diffuse and/or multifocal generator that is best recorded by referential EEG derivations due to their larger leadfields. Hum Brain Mapp, 2011. © 2011 Wiley Periodicals, Inc.},
  year = {2011}
  }
description: "While sleep spindles are traditionally viewed as synchronous brain-wide events, this research demonstrates they actually emerge from a much more dynamic, focal process. Most spindles begin as localized, asynchronous oscillations—detectable only by MEG—before recruiting a "critical mass" of cortical surface area to finally appear as a synchronous wave on the EEG. Essentially, MEG captures the private, early "spark" of a spindle in specific brain regions, whereas EEG records the eventual "forest fire" of global synchronization that follows about 200 milliseconds later."
math: true
---

# The Hidden Topography of Sleep Spindles: From Asynchronous MEG Generators to Synchronous EEG Events

Sleep spindles occupy a special place in systems neuroscience. They are among the most recognizable oscillatory signatures of non-REM sleep, appearing as transient bursts of approximately \(10\)--\(15\,\mathrm{Hz}\) activity, typically lasting \(0.5\)--\(2\,\mathrm{s}\), and most prominently associated with Stage 2 sleep. They have been studied as markers of thalamocortical physiology, sleep architecture, memory consolidation, and large-scale neural synchrony. But they also pose a more basic question: when we observe a spindle at the scalp, what exactly is the spatial and dynamical organization of the neural activity that produced it?

For a long time, the dominant picture was that sleep spindles reflect a broadly synchronous thalamocortical event. Classical animal physiology, intracellular studies, computational models, and scalp EEG observations all contributed to this view. In scalp EEG, spindles often appear nearly simultaneous across many electrodes, suggesting a large-scale coordinated oscillation distributed across the cortical mantle. This has made the spindle a natural model for studying how the thalamus and cortex generate coherent rhythms over large spatial scales.

In our paper, **“Emergence of Synchronous EEG Spindles From Asynchronous MEG Spindles,”** we asked whether this apparent macroscopic synchrony is the whole story. The central idea was simple but powerful: if spindles are truly globally synchronous events, then simultaneous high-density EEG and MEG should largely reveal the same spindle events, modulo the known differences in sensitivity between the two modalities. Instead, we found a striking dissociation. Many spindles that are clearly visible in MEG gradiometers are absent from referential EEG, whereas the reverse case is rare. This asymmetry suggests that the “global” EEG spindle may not be the primitive event. Rather, it may emerge from a more local, spatially structured, and partially asynchronous process that is better captured by MEG.

This paper is therefore not only about sleep spindles. It is also about the physics of observation in human neurophysiology. EEG and MEG are often treated as complementary windows onto the same underlying brain activity. That is true at one level: both ultimately reflect currents generated by organized postsynaptic activity, especially in cortical pyramidal neurons. But the two modalities do not see the same sources with the same spatial weighting, and they do not respond equally to focal versus distributed generators. In this study, those differences become a tool. The dissociation between EEG and MEG spindles reveals hidden structure in the spindle-generating system itself.

## The classical problem: are spindles globally synchronous?

Sleep spindles are generated through thalamocortical interactions involving the thalamic reticular nucleus, thalamocortical relay cells, corticothalamic feedback, and cortical populations. The standard physiological picture emphasizes reciprocal interactions between inhibitory thalamic reticular neurons and bursting thalamocortical neurons. These interactions can generate rhythmic activity in the spindle frequency range, and corticothalamic loops help coordinate and sustain the oscillation.

A key question is whether this rhythm is generated as a single, coherent, large-scale event or as a set of local events that can sometimes become synchronized. Animal studies have supported both views. Some experiments suggested propagation from focal onset zones, whereas others emphasized widespread synchrony across thalamic and cortical sites. In human scalp EEG, spindles frequently appear as broadly coherent events, reinforcing the impression of a large-scale synchronous generator.

But scalp EEG is not a neutral observer of spatial synchrony. A referential EEG channel has a large leadfield. It integrates activity over broad cortical regions, and its signal is strongly shaped by the volume conduction properties of the head. Thus, high apparent synchrony in EEG can arise not only from perfect physiological synchrony, but also from spatial integration by the measurement system. If a distributed source is even moderately coherent over a large region, EEG may emphasize its common component. Conversely, focal or partially asynchronous generators may be difficult to isolate in referential EEG because they are mixed with other sources within the same large leadfield.

MEG planar gradiometers have a different sensitivity profile. They are more focal. They are less affected by skull and scalp conductivity. They are sensitive primarily to tangential intracellular currents, and they strongly attenuate spatially broad or distant sources. This makes MEG gradiometers less suited to detecting a perfectly diffuse synchronous field, but better suited to detecting local sources with favorable geometry.

The question, then, is not simply whether EEG and MEG detect spindles. The deeper question is:

\[
\text{Which spatial scales of spindle generation are made visible by each modality?}
\]

Our study used simultaneous high-density EEG and MEG to examine this question directly.

## Simultaneous EEG and MEG as a biophysical perturbation of the measurement problem

We recorded natural sleep from healthy adults using simultaneous 60-channel EEG and 306-channel MEG. The MEG system included magnetometers and two orthogonal planar gradiometers at each sensor location, but the main analyses focused on the gradiometers because of their focal sensitivity. Sleep staging identified Stage 2 non-REM periods, and spindle-rich epochs were analyzed.

The essential methodological point was that spindle detection was performed objectively and separately in EEG and MEG. We did not begin by assuming that an EEG spindle and an MEG spindle were the same event. Instead, we computed sequential power spectral density in the spindle band and asked when each modality independently showed spindle-frequency power peaks.

For each channel, spindle-band power was estimated in the \(7\)--\(15\,\mathrm{Hz}\) range using sliding \(500\,\mathrm{ms}\) windows advanced in \(100\,\mathrm{ms}\) steps. In schematic form, if \(x_i(t)\) is the signal recorded at channel \(i\), then for a window centered at time \(\tau\), the spindle-band power can be written as

\[
P_i(\tau)
=
\int_{7\,\mathrm{Hz}}^{15\,\mathrm{Hz}}
\left|
\mathcal{F}\{x_i(t)w(t-\tau)\}(f)
\right|^2
\,df,
\]

where \(w(t-\tau)\) is the analysis window. The resulting time series \(P_i(\tau)\) gives a channel-wise measure of spindle-frequency power over time.

The detection algorithm then identified periods where spindle-band power rose above baseline across a sufficient number of channels. Importantly, EEG and MEG detections were performed independently. Once peaks were detected in each modality, we classified events according to whether a MEG spindle had a corresponding EEG spindle within a specified temporal tolerance.

This led to three conceptual categories:

- **ME spindles**: spindles detected in both MEG and EEG.
- **Mo spindles**: spindles detected in MEG only.
- **EEG-only spindles**: spindles detected in EEG without corresponding MEG involvement.

The last category was rare. The important contrast was between MEG-only spindles and combined MEG+EEG spindles.

## The main empirical dissociation

The result was striking. About half of the MEG spindles did not have a corresponding EEG spindle. In contrast, most EEG spindles did have a corresponding MEG spindle. Quantitatively, when allowing a \(500\,\mathrm{ms}\) temporal window for co-occurrence, the probability that an MEG spindle occurred given an EEG spindle was high, approximately

\[
P(\mathrm{MEG}\mid \mathrm{EEG}) \approx 0.85,
\]

whereas the probability that an EEG spindle occurred given a MEG spindle was much lower,

\[
P(\mathrm{EEG}\mid \mathrm{MEG}) \approx 0.47.
\]

Thus, EEG spindles were usually accompanied by MEG spindles, but MEG spindles were often not accompanied by EEG spindles.

This asymmetry is crucial. If EEG and MEG were simply noisy measurements of the same globally synchronous generator, one would expect a more symmetric relationship. Instead, the results suggest a hierarchical or recruitment-like process: the neural substrate visible to MEG can be active without producing a detectable referential EEG spindle, but when a referential EEG spindle appears, the MEG-visible substrate is usually already involved.

The temporal structure reinforced this interpretation. During spindles detected in both modalities, MEG spindle-band power began earlier than EEG spindle-band power and persisted longer. Depending on the amplitude threshold used to define onset and offset, MEG led EEG by roughly \(100\)--\(190\,\mathrm{ms}\) on the rising phase and outlasted EEG by roughly \(140\)--\(310\,\mathrm{ms}\) on the falling phase. Since a spindle cycle at \(12\,\mathrm{Hz}\) lasts about \(83\,\mathrm{ms}\), these delays correspond to approximately one to several oscillatory cycles.

This timing argues against the idea that EEG and MEG are merely detecting the same event with slightly different noise levels. Instead, the MEG-visible activity appears first. In some cases, it remains local or fragmented and never becomes visible in referential EEG. In other cases, it recruits a broader cortical or thalamocortical substrate, eventually producing the large-scale synchronous event recorded by EEG.

## Why amplitude alone cannot explain the EEG spindle

A simple explanation would be that MEG-only spindles are just weaker versions of MEG+EEG spindles. Perhaps the same generator becomes larger, and once its amplitude crosses a threshold, it becomes visible in EEG. This explanation is plausible, but the data argue against it.

When we compared MEG-only spindles to MEG+EEG spindles, MEG amplitude increased only modestly. Depending on the exact measure and channel subset, the increase was on the order of roughly \(10\)--\(20\%\). By contrast, EEG amplitude increased by approximately \(55\%\). The MEG amplitude change was therefore too small to explain the much larger increase in EEG power.

A second possibility is that the MEG sources become more coherent. If many local generators oscillate with better phase alignment, then even without large amplitude increases at individual sites, their combined field might become visible in EEG. To test this, we estimated coherence between MEG gradiometer channels using Capon’s nonparametric spectral estimation, also known as the minimum variance distortionless response (MVDR). In broad terms, coherence between two channels \(i\) and \(j\) at frequency \(f\) can be expressed as

\[
C_{ij}(f)
=
\frac{|S_{ij}(f)|^2}{S_{ii}(f)S_{jj}(f)},
\]

where \(S_{ij}(f)\) is the cross-spectral density and \(S_{ii}(f)\), \(S_{jj}(f)\) are autospectral densities. MVDR provides a spectral estimate that can be useful when distinguishing contributions from nearby frequencies.

Again, the result was not consistent with a simple coherence-threshold explanation. MEG coherence increased only slightly from MEG-only to MEG+EEG spindles, on the order of about \(1\%\) in the relevant comparisons. Such a small change cannot plausibly explain the much larger EEG amplitude increase.

The more informative difference was spatial recruitment.

## Spatial recruitment and the emergence of the EEG spindle

The strongest distinction between MEG-only and MEG+EEG spindles was not local amplitude or pairwise coherence, but the number and distribution of MEG channels involved. During MEG+EEG spindles, the fraction of active MEG gradiometer channels increased substantially relative to MEG-only spindles. In the paper, the average fraction of participating gradiometer channels was approximately \(20.9\%\) for MEG+EEG spindles compared with \(12.6\%\) for MEG-only spindles, corresponding to an increase of about \(66\%\).

This suggests that a referential EEG spindle emerges when the spindle-generating activity spreads over a sufficiently large spatial extent. The EEG spindle is not simply the same focal generator becoming louder. It is the macroscopic signature of broader cortical recruitment.

The topography of this recruitment was also meaningful. MEG+EEG spindles showed relatively greater power over anterior and midline/frontocentral regions compared with MEG-only spindles. This does not mean that spindles are exclusively frontal. Rather, it suggests that recruitment of frontal or frontocentral cortical territories may play a special role in the transition from a focal or fragmented MEG-visible event to a distributed EEG-visible event.

This is important because prefrontal regions have strong anatomical relationships with thalamic circuitry involved in synchronizing thalamocortical activity. The thalamic reticular nucleus and thalamocortical projection systems provide plausible routes through which local spindle activity could recruit broader domains. Thus, the topography is not merely a measurement detail. It points toward a physiological mechanism.

The picture that emerges is one of spatial growth. A spindle may begin as a local oscillatory event, visible to MEG because the gradiometer leadfield is small and focal. If that event remains local, it appears as a MEG-only spindle. If it recruits additional cortical and thalamocortical domains, especially frontocentral regions, it may reach a critical spatial extent and become visible as a referential EEG spindle.

## The physics of why MEG can see what EEG misses

At first glance, the existence of MEG-only spindles may seem counterintuitive. EEG has large leadfields and integrates over broad regions. Should it not detect any source that MEG detects?

The answer lies in signal-to-noise ratio and spatial mixing. A large leadfield is not always an advantage. If a focal spindle generator lies within the compact leadfield of a MEG gradiometer, that gradiometer may record it with high signal-to-noise ratio. But the same focal generator contributes only a small fraction of the signal at a referential EEG electrode, whose leadfield includes many other cortical sources. In EEG, the focal spindle can be diluted by unrelated activity. It is not necessarily absent from the EEG forward model; rather, it may be invisible relative to the background mixture.

This is a general lesson for neuroimaging and source modeling. Visibility is not identical to existence. A source can be physically present but effectively undetectable in a modality if its contribution is small relative to the modality’s spatial integration and noise structure.

The leadfield relation can be written schematically as

\[
\mathbf{y}(t) = \mathbf{L}\mathbf{j}(t) + \boldsymbol{\varepsilon}(t),
\]

where \(\mathbf{y}(t)\) is the sensor measurement, \(\mathbf{j}(t)\) is the distribution of neural current sources, \(\mathbf{L}\) is the leadfield operator, and \(\boldsymbol{\varepsilon}(t)\) captures noise and unmodeled activity. EEG and MEG differ in \(\mathbf{L}\). Their leadfields weight source orientation, spatial extent, conductivity structure, and distance differently.

For referential EEG, \(\mathbf{L}_{\mathrm{EEG}}\) is broad and strongly shaped by volume conduction through CSF, skull, and scalp. For MEG planar gradiometers, \(\mathbf{L}_{\mathrm{MEG}}\) is more focal and primarily sensitive to tangential currents. A focal source may therefore yield a large component in a local MEG gradiometer but only a weak component in referential EEG. Conversely, a spatially distributed synchronous source may sum effectively in EEG but partially cancel in MEG, especially if currents on opposing sulcal banks have opposite orientations.

This is why the MEG-only spindle is not paradoxical. It is a natural consequence of source geometry, leadfield size, and spatial integration.

## EEG synchrony is not necessarily microscopic synchrony

One of the deeper implications of the study concerns the interpretation of synchrony. In scalp EEG, spindles often appear highly synchronous across electrodes. In our data, the average pairwise correlation across EEG channels during the analyzed epochs was much higher than the corresponding pairwise correlation across MEG gradiometer channels. EEG channels were strongly correlated; MEG gradiometer channels were much less so.

This does not mean that EEG is wrong. It means that EEG emphasizes a different component of the underlying activity. Referential EEG is well suited to detecting distributed coherent fields. When a spindle becomes sufficiently widespread, EEG captures the common large-scale component. MEG gradiometers, by contrast, can reveal local heterogeneity within what appears from the scalp as a unified event.

Thus, the scalp EEG spindle may be a macroscopic order parameter for a distributed thalamocortical process. It captures the emergence of large-scale coherence, but it does not necessarily reveal the local route by which that coherence emerged.

A useful analogy comes from statistical physics. A macroscopic order parameter can indicate that a system has entered an organized phase, but it does not by itself specify the microscopic path to that phase. The EEG spindle may function similarly. It reports the presence of a large-scale coherent oscillatory state, while MEG reveals that this state can arise from initially local and asynchronous components.

This perspective changes how one might model spindle generation. Instead of treating the spindle as a single globally synchronized oscillator, one can think of it as a spatially extended dynamical process in which local oscillatory domains interact, recruit one another, and sometimes cross a threshold into macroscopic coherence.

## Core and matrix thalamocortical systems

The paper proposed a physiological interpretation based on the distinction between core and matrix thalamocortical systems. The core system consists of more specific thalamocortical projections, often associated with focal or topographically organized cortical targets. The matrix system consists of more diffuse thalamocortical projections, capable of influencing broad cortical territories.

Under this framework, MEG gradiometers may be especially sensitive to focal, asynchronous spindles generated within core-like thalamocortical modules. Referential EEG, by contrast, may be especially sensitive to diffuse, synchronous activity generated through matrix-like thalamocortical recruitment.

This gives a natural interpretation of the MEG-only and MEG+EEG distinction:

\[
\text{MEG-only spindle}
\quad \rightarrow \quad
\text{local/focal thalamocortical event}
\]

\[
\text{MEG+EEG spindle}
\quad \rightarrow \quad
\text{local event plus distributed recruitment}
\]

The model does not require that EEG and MEG arise from completely separate biological rhythms. Rather, it suggests that they emphasize different regimes of the same spindle-generating system. A focal event can remain local and be visible only to MEG. Or it can recruit additional thalamocortical domains, become spatially extended, and appear in EEG.

This is also consistent with the temporal finding that MEG begins before EEG in combined spindles. The focal event precedes the distributed event. The macroscopic EEG spindle emerges later, once the recruited network reaches sufficient spatial extent and coherence.

## Toward a source-modeling view of spindle emergence

The findings also have implications for source modeling. A common temptation in source analysis is to seek a single “generator” of an observed rhythm. But for spindles, this study suggests that the word generator may be misleading if it implies a single stable source. The source structure appears to be dynamic, spatially heterogeneous, and modality-dependent.

A more appropriate source-modeling framework would treat the spindle as a time-evolving source distribution:

\[
\mathbf{j}(t)
=
\sum_{k=1}^{K(t)}
a_k(t)\,\phi_k(\mathbf{r})\,e^{i\theta_k(t)},
\]

where \(\phi_k(\mathbf{r})\) represents the spatial pattern of a local generator or domain, \(a_k(t)\) its amplitude, \(\theta_k(t)\) its phase, and \(K(t)\) the number of participating domains at time \(t\). In a MEG-only spindle, \(K(t)\) may remain small, and the phases \(\theta_k(t)\) may not align sufficiently across space to generate a strong referential EEG signal. In a MEG+EEG spindle, more domains become active, their spatial distribution changes, and a sufficiently coherent distributed component emerges.

This formulation makes clear why amplitude, coherence, and number of channels are not interchangeable. A large EEG spindle may require not merely stronger local sources, but a reconfiguration of the source distribution: more domains, different locations, and a stronger common component.

It also suggests why inverse solutions are difficult. If EEG and MEG weight different components of the same evolving source field, then combining them requires careful attention to leadfield geometry, source extent, and the distinction between focal and distributed activity. A source model that explains MEG-only spindles may not automatically explain EEG spindles, and a model fit only to EEG may miss the asynchronous local structure that precedes the global event.

## Statistical controls and the interpretation of coincidence

The paper also addressed a basic statistical issue: if EEG and MEG spindles sometimes co-occur, how do we know that this co-occurrence is meaningful rather than a consequence of high spindle density during Stage 2 sleep?

To address this, the study compared observed coincidence rates with rates obtained after randomizing inter-spindle intervals. The observed co-occurrence exceeded the randomized expectation, showing that EEG and MEG spindle timing is not independent. However, the relationship was far from deterministic. MEG and EEG spindles were statistically related, but MEG spindles often occurred without EEG expression.

This matters because the result is not a simple dissociation. It is not that EEG and MEG detect unrelated phenomena. Rather, the relationship is asymmetric and probabilistic. MEG activity is often present when EEG spindles occur, but MEG activity does not guarantee EEG expression. This is precisely the structure one would expect from a recruitment process: local activity increases the probability of global expression, but global expression requires additional spatial and dynamical conditions.

In this sense, the spindle is not best thought of as a binary event. It is a dynamical process with degrees of spatial recruitment, coherence, and modality visibility.

## Implications for sleep neurophysiology

For sleep neurophysiology, the study suggests that the canonical EEG spindle is only one manifestation of a richer thalamocortical process. The EEG spindle may represent the subset of spindle events that successfully recruit enough cortex, with sufficient coherence and appropriate geometry, to become visible at the scalp.

This has several implications.

First, spindle counts based only on referential EEG may underestimate the number of focal spindle-like thalamocortical events. Many local events may be invisible to scalp EEG but detectable with MEG or intracranial recordings.

Second, spindle synchrony should not be assumed from EEG coherence alone. High EEG coherence may reflect true large-scale synchrony, but it is also shaped by the large leadfields of referential EEG. MEG and intracranial data can reveal local asynchrony within the broader event.

Third, different spindle subtypes may not merely differ in frequency, duration, or frontal/parietal dominance. They may differ in their degree of spatial recruitment and in the balance between focal and diffuse thalamocortical systems.

Finally, the transition from MEG-only to MEG+EEG spindles may provide a useful experimental handle on the mechanisms by which local oscillations become global brain states. This transition is where the physics of measurement and the physiology of recruitment meet.

## Implications for oscillations and synchrony more broadly

Although this paper focuses on sleep spindles, the conceptual issue extends to many neural oscillations. Oscillatory synchrony is often inferred from sensor-level coherence, phase-locking, or amplitude correlation. But sensor-level synchrony is always filtered through the measurement apparatus. The spatial scale and orientation of the source, the conductivity structure of the head, and the leadfield properties of the modality all shape what appears synchronous.

This is especially important when interpreting large-scale rhythms such as alpha, beta, gamma, slow oscillations, and pathological rhythms. A rhythm that appears global in EEG may have local structure that is not visible without MEG or intracranial recordings. Conversely, focal activity visible in MEG or ECoG may fail to produce a scalp signature unless it recruits a sufficiently large or appropriately oriented source distribution.

The broader lesson is that synchrony is not a single-level concept. There is microscopic synchrony among neurons and local circuits; mesoscopic synchrony among cortical columns or areas; macroscopic synchrony visible in scalp fields; and measurement-induced synchrony arising from spatial mixing. These levels are related, but they are not identical.

For this reason, the study of neural synchrony requires both physiology and physics. One needs models of thalamocortical dynamics, but also models of how those dynamics project to sensors.

## Conclusion: the EEG spindle as an emergent macroscopic event

The main message of the paper is that the familiar synchronous EEG spindle may emerge from a more local and asynchronous MEG-visible process. MEG gradiometers often detect focal spindle activity that does not appear in referential EEG. When EEG spindles do appear, they are usually accompanied by MEG activity, and that MEG activity begins earlier and ends later. The transition from MEG-only to MEG+EEG spindles is associated not primarily with a large increase in MEG amplitude or coherence, but with recruitment of more MEG channels and a shift toward frontocentral regions.

This leads to a revised view of spindle generation. Rather than a single monolithic synchronous generator, the spindle-generating system may consist of local thalamocortical domains that can remain focal or recruit broader networks. MEG is sensitive to the focal components. EEG is sensitive to the distributed coherent state that sometimes emerges from them.

In this view, the EEG spindle is not the beginning of the event. It is the macroscopic expression of a process already underway.

That distinction matters. It changes how we interpret scalp synchrony, how we model thalamocortical oscillations, and how we think about the relationship between local circuit dynamics and global brain states during sleep. It also illustrates a general principle for neurophysiology: what we observe as a coherent brain rhythm is always the result of both neural dynamics and measurement physics. Understanding one without the other is incomplete.

## Citing

If you use this code or build on these ideas, please cite the paper using the
BibTeX entry above.
