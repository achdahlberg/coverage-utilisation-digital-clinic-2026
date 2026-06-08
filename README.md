# Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic

Code for the study:
Dahlberg A., Kaartinen T., Jukarainen S. & Orre P. (2026). *Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic in Publicly Funded Healthcare: A Registry-Based Observational Study in Finland.* Preprint: https://doi.org/10.1101/2025.11.06.25339651

## Overview

A registry-based look at a 24/7 chat-based digital clinic at Harjun terveys (Päijät-Häme, Finland), using ~2.8M primary care encounters from 2019–2025. The notebook (`analysis.ipynb`) reproduces all tables and figures:

- **Table 1** - Coverage and encounters per 1,000, 2019–2025 (incl. φ-correction + sensitivity analysis)
- **Figure 1** - Encounters by modality over time
- **Figure 2** - Encounters per 1,000 by age group and type
- **Table 2** - Digital vs traditional users (demographics, CCI, adjusted ORs)
- **Figures 3-4** - Most common ICPC-2 and ICD-10 codes
- **Figure 5** - Cumulative follow-up over 30 days
- **Figure 6** - Sankey of downstream care

## Data Availability

Patient-level data isn't shared (privacy / data protection). Analysis used pseudonymised data under the Finnish Act on Secondary Use of Health and Social Data (552/2019), approved by the Päijät-Häme Wellbeing Services County (HA/187/07.01.04.05/2025).

## References

- Harris CR, Millman KJ, van der Walt SJ, et al. Array programming with NumPy. *Nature* 585, 357–362 (2020). https://doi.org/10.1038/s41586-020-2649-2
- Virtanen P, Gommers R, Oliphant TE, et al. SciPy 1.0: fundamental algorithms for scientific computing in Python. *Nature Methods* 17, 261–272 (2020). https://doi.org/10.1038/s41592-019-0686-2
- Pedregosa F, Varoquaux G, Gramfort A, et al. Scikit-learn: Machine Learning in Python. *Journal of Machine Learning Research* 12, 2825–2830 (2011).
- Seabold S, Perktold J. statsmodels: Econometric and statistical modeling with Python. *Proceedings of the 9th Python in Science Conference* (2010).
- Hunter JD. Matplotlib: A 2D Graphics Environment. *Computing in Science & Engineering* 9, 90–95 (2007). https://doi.org/10.1109/MCSE.2007.55
- Waskom ML. seaborn: statistical data visualization. *Journal of Open Source Software* 6, 3021 (2021). https://doi.org/10.21105/joss.03021

## Citation

```
@article{dahlberg2026coverage,
  title   = {Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic in Publicly Funded Healthcare: A Registry-Based Observational Study in Finland},
  author  = {Dahlberg, Alexandra and Kaartinen, Taavi and Jukarainen, Sakari and Orre, Petja},
  year    = {2026},
  preprint= {https://doi.org/10.1101/2025.11.06.25339651}
}
```
