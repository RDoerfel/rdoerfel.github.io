---
layout: project
title: "Multimodal Brain Age Prediction Using Machine Learning"
description: "Combining structural MRI and 5-HT2AR PET derived features for accurate brain age prediction"
category: research

---

# Multimodal Brain Age Prediction Using Machine Learning

## Overview

This project focuses on developing advanced biomarkers for assessing age-related biological changes in the human brain. We combine structural MRI and 5-HT2AR PET data to improve brain age prediction, which is crucial for understanding neurodegenerative disorders and evaluating neuroprotective interventions. Please visit the [GitHub repository](https://github.com/RDoerfel/bap2a-public.git) for code and documentation: 

## Key Objectives

1. Predict brain age using 5-HT2AR binding outcomes
2. Compare 5-HT2AR-based predictions to gray matter (GM) volume predictions
3. Investigate the synergy of combining 5-HT2AR and GM volume data for improved prediction accuracy

## Methodology

- **Data**: PET and MR images from 209 healthy individuals (age range: 18-85 years)
- **Measures**: 5-HT2AR binding and GM volume for 14 cortical and subcortical regions
- **Analysis**: Applied various machine learning algorithms for age prediction
- **Evaluation**: Used Mean Absolute Error (MAE) and cross-validation for model comparison

## Key Findings

- 5-HT2AR binding predicts chronological age accurately (mean MAE = 6.63 years, std = 0.74 years)
- GM volume also provides accurate predictions (mean MAE = 6.95 years, std = 0.83 years)
- Combining both measures significantly improves prediction accuracy (mean MAE = 5.54 years, std = 0.68)

## Publication

- **Preprint**: [bioRxiv](https://www.biorxiv.org/content/10.1101/2024.02.05.578968v2)
- **Journal Article**: [GeroScience](https://doi.org/10.1007/s11357-024-01148-6)

## Citation

```bibtex
@article{Doerfel2024,
  title = {Multimodal Brain Age Prediction Using Machine Learning: Combining Structural {{MRI}} and 5-{{HT2AR PET-derived}} Features},
  shorttitle = {Multimodal Brain Age Prediction Using Machine Learning},
  author = {D{\"o}rfel, Ruben P. and {Arenas-Gomez}, Joan M. and Svarer, Claus and Ganz, Melanie and Knudsen, Gitte M. and Svensson, Jonas E. and {Plav{\'e}n-Sigray}, Pontus},
  year = {2024},
  journal = {GeroScience},
  doi = {10.1007/s11357-024-01148-6},
  urldate = {2024-05-01},
  copyright = {All rights reserved},
  langid = {english},
  keywords = {5HT2A,brain age,MRI,multimodal,PET}
}
```

## Code Repository

The code and documentation for this project are available on GitHub. To use the code:

1. Clone the repository:
   ```
   git clone https://github.com/RDoerfel/bap2a-public.git
   ```

2. Set up the environment:
   ```
   conda env create -f environment.yml
   conda activate bap2a-public
   ```

3. Install the package:
   ```
   pip install -e .
   ```
