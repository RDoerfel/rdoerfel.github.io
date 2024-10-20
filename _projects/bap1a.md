---
layout: page
title: "Comparison of Brain Age Prediction Software Packages"
description: "Evaluating accuracy and test-retest reliability of publicly available software for brain age prediction using structural MRI"
category: research
date: 2023-09-01
---

# Prediction of Brain Age Using Structural Magnetic Resonance Imaging

## Abstract

Brain age prediction algorithms using structural magnetic resonance imaging (MRI) aim to assess the biological age of the human brain. The difference between a person's chronological age and the estimated brain age is thought to reflect deviations from a normal aging trajectory, indicating a slower or accelerated biological aging process. Several pre-trained software packages for predicting brain age are publicly available. In this study, we perform a comparison of such packages with respect to (1) predictive accuracy, (2) test–retest reliability, and (3) the ability to track age progression over time.

## Objectives

1. Evaluate the predictive accuracy of multiple publicly available software packages for brain age prediction
2. Assess the test-retest reliability of these software packages
3. Compare the ability of each package to track age progression over time
4. Provide a comprehensive comparison to guide researchers in choosing appropriate tools for their studies

## Methodology

- **Data**: 
  - T1-weighted MRI scans from 372 healthy individuals (age range: 18.4-86.2 years, mean 38.7 ± 17.5 years)
- **Software Packages**: 
  - brainageR
  - DeepBrainNet
  - brainage
  - ENIGMA
  - pyment
  - mccqrnn
- **Metrics**: 
  - Accuracy: Mean Absolute Error (MAE), Pearson's correlation coefficient (r)
  - Reliability: Intraclass Correlation Coefficient (ICC)
  - Age progression tracking: Analysis over a longer time span

## Implications

- Significant differences in accuracy, reliability, and age progression tracking across software packages
- pyment and brainageR consistently showed the highest accuracy and test-retest reliability
- some models are highly accurate and reliable

## Publications

Dörfel, R. P., Arenas-Gomez, J. M., Fisher, P. M., Ganz, M., Knudsen, G. M., Svensson, J. E., & Plavén-Sigray, P. (2023). Prediction of Brain Age Using Structural Magnetic Resonance Imaging: A Comparison of Accuracy and Test--Retest Reliability of Publicly Available Software Packages. Human Brain Mapping, 44(17), 6139-6148. [https://doi.org/10.1002/hbm.26502](https://doi.org/10.1002/hbm.26502)

## Citation

```bibtex
@article{Doerfel2023,
  title      = {Prediction of Brain Age Using Structural Magnetic Resonance Imaging: {{A}} Comparison of Accuracy and Test--Retest Reliability of Publicly Available Software Packages},
  shorttitle = {Prediction of Brain Age Using Structural Magnetic Resonance Imaging},
  author     = {D{\"o}rfel, Ruben P. and {Arenas-Gomez}, Joan M. and Fisher, Patrick M. and Ganz, Melanie and Knudsen, Gitte M. and Svensson, Jonas E. and {Plav{\'e}n-Sigray}, Pontus},
  year       = {2023},
  journal    = {Human Brain Mapping},
  volume     = {44},
  number     = {17},
  pages      = {6139--6148},
  issn       = {1097-0193},
  doi        = {10.1002/hbm.26502},
  urldate    = {2024-03-25},
  abstract   = {Brain age prediction algorithms using structural magnetic resonance imaging (MRI) aim to assess the biological age of the human brain. The difference between a person's chronological age and the estimated brain age is thought to reflect deviations from a normal aging trajectory, indicating a slower or accelerated biological aging process. Several pre-trained software packages for predicting brain age are publicly available. In this study, we perform a comparison of such packages with respect to (1) predictive accuracy, (2) test--retest reliability, and (3) the ability to track age progression over time. We evaluated the six brain age prediction packages: brainageR, DeepBrainNet, brainage, ENIGMA, pyment, and mccqrnn. The accuracy and test--retest reliability were assessed on MRI data from 372 healthy people aged between 18.4 and 86.2 years (mean 38.7 {\textpm} 17.5 years). All packages showed significant correlations between predicted brain age and chronological age (r = 0.66--0.97, p {$<$} 0.001), with pyment displaying the strongest correlation. The mean absolute error was between 3.56 (pyment) and 9.54 years (ENIGMA). brainageR, pyment, and mccqrnn were superior in terms of reliability (ICC values between 0.94--0.98), as well as predicting age progression over a longer time span. Of the six packages, pyment and brainageR consistently showed the highest accuracy and test--retest reliability.}
}
```
