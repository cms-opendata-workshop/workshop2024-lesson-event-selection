---
title: "The physics of our analysis"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is the signal we are searching for?
- What are the backgrounds we need to concern ourselves with?
- How will we select the data?
- What is a "boosted jet"?
- What trigger(s) will we be using?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand what makes the signal "look" different from our backgrounds?
- How does this translate into how we record and measure particle interactions in CMS?

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

We're going to reproduce parts of a 2019 CMS study for resonant production of 
top-antitop pairs. The paper can be found [here](https://arxiv.org/pdf/1810.05905) and
hypothesizes a particle with specific properties referred to as $Z'$ which is
produced in our proton-proton collisions and then decays to a top-antitop pair. 

$$p p \rightarrow Z' \rightarrow t\overline{t}$$

![Representation of the resolved (left) and boosted (right) regimes of a top-quark pair decay. From the [thesis](https://www.semanticscholar.org/paper/Searches-for-top-antitop-quark-resonances-in-final-Missiroli/15209cea4bda62b56ca4e8f3bf856b8470b168e4) of M. Missiroli "Searches for top-antitop quark resonances in semileptonic final states with the CMS detector"](fig/boosted_top_decay.png){alt='Two diagrams showing a top quark and antitop quark being produced where one decays through a leptonic process and the other decays through a hadronic process. The first image shows the hadronic decay in a non-boosted state and the second image shows the hadronic jets overlapping because of the boosted nature of the decay.'}

The original analysis searched for the $Z'$ assuming a range of masses. In the interests
of time, we will conduct our search assuming a mass of 2000 GeV/$c^2$ for the $Z'$. The
Monte Carlo for this process can be found [here](https://opendata.cern.ch/record/75156).
It might be helpful 
[to review how to find data and how to understand these records](https://cms-opendata-workshop.github.io/workshop2024-lesson-dataset-scouting/instructor/index.html), 
if you have not done so prior to the lesson. 

## Selection criteria

A top quark decays almost 100% of the time to a $b$-quark and a $W$ boson. The $W$ can decay *leptonically* (to a charged lepton and a neutrino)
or *hadronically* (to a quark and an antiquark). All the quarks hadronize to form *jets*.

We reconstruct the top quark pair such that one of the top quarks decays leptonically and the other decays hadronically. This is
referred to as the *semileptonic* final state, as opposed to the *hadronic* final state, when both top quarks decay hadronically, 
 or the *leptonic* final state, when both top quarks decay leptonically. 

We are assuming masses of the $Z'$ resonance in the TeV range and for this particular search, a mass of 2000 GeV/c$^2$ (2 TeV/c$^2$).
The mass of the top quark is 173 GeV/c$^2$, considerably less than the resonance for which we are searching. This means
that a significant amount of the mass-energy of the resonance goes into the momentum of the top quarks, referred to as a *boosted* final state.
In this boosted regime, the individual jets from the hadronically decaying top quark overlap and appear to merge together. 

We are going to attempt to calculate the invariant mass of the $Z'$ by reconstructing it's 4-momentum from the sum of the 
4-momenta of the top quark and antitop quark. Meaning we have four (4) physics "objects" in our final state. 

* The jet coming from the $b$-quark of the leptonically-decaying top quark.
* The muon coming from the $W$ of the leptonically-decaying top quark.
* The neutrino coming from the $W$ of the leptonically-decaying top quark.
* The fully-merged jets of the hadronically-decaying top quark.

### Physics requirements 

* For the jet from the $b$ quark, we are going to make use of the `Jet` physics objects and require
that the $b$-tagging algorithm is above some threshold and that the jet passes some other combined quality checks.
* We will use the `Muon` physics object and require that it is a relatively high momentum muon with $p_T > 55$ GeV/c and that is is
recorded in a fiducial region of $|\eta| < 2.4$. We will also require that it is isolated from the other jets and that it passes
some reconstruction quality thresholds. 
* For the merged jets, we make use of the `FatJet` object. We will require a $p_T>500$ GeV/c. While the original analysis tried to tag
top quarks by looking at the subjettiness, we now have access to a more sophisticated tagger and so we will use this field and set
a threshold to cleanly identify boosted top quark merged jets.
* The neutrino will be approximated using the missing energy in the transverse plane, MET, and we will use the 
`PuppiMET` object in our calculations. We'll approximate the mass as 0. 

### Trigger

We will require that events pass the `HLT_TkMu50` trigger: the high-level trigger that requires a track consistent with a
muon with $p_T > 50$ GeV/c.

### Luminosity masking

In a [previous lesson](https://cms-opendata-workshop.github.io/workshop2024-lesson-triggers-lumi/instructor/index.html), 
you learned that the luminosity is calculated for "good" runs and so we need to make sure we only use those runs when we process
collision data. 

We'll be downloading and using [this file](https://opendata.cern.ch/record/14220/files/Cert_271036-284044_13TeV_Legacy2016_Collisions16_JSON.txt)
to match and select these good runs. 


::::::::::::::::::::::::::::::::::::: keypoints 

- We reconstruct the final state in the semileptonic decay of the top-quark pair
- The high mass assumption of the $Z'$ resonance leads to boosted final states
- We can make use of specific reconstruction algorithms to identify these final states

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
