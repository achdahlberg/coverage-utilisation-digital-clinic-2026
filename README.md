# Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic

Code for the study:
Dahlberg A., Kaartinen T., Jukarainen S. & Orre P. (2026). *Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic in Publicly Funded Healthcare: A Registry-Based Observational Study in Finland.* Preprint: https://doi.org/10.1101/2025.11.06.25339651

## Overview

A registry-based look at a 24/7 chat-based digital clinic at Harjun terveys (Päijät-Häme, Finland), 2019–2025. The extract holds 2,796,395 encounter records; 1,505,993 meet the primary care encounter definition (in-person appointments, digital clinic encounters, physician consultations), and a further 74,845 come from a separate digital system that could not be linked to the EHR, giving 1,580,838 analysed encounters.

`analysis.ipynb` reproduces all tables and figures:

- **Table 1** — Coverage and encounters per 1,000, 2019–2025, including the cross-system overlap correction (φ = 0.654, derived from the fully linked 2024–2025 data)
- **Supplementary Table S1** — Sensitivity of 2021–2023 coverage to φ across its full plausible range
- **Figure 1** — Encounters by modality over time
- **Figure 2** — Encounters per 1,000 by age group and contact type
- **Table 2** — Digital vs traditional users on a person-year basis: demographics, crude and directly age/sex-standardised CCI ≥1 prevalence, and adjusted ORs from logistic regression with a quadratic age term and cluster-robust standard errors at patient level
- **Figures 3–4** — Most common ICPC-2 and ICD-10 codes
- **Figure 5** — Cumulative follow-up over 30 days, split into follow-ups booked after the index encounter and those arranged during it
- **Figure 6** — Sankey of downstream care over 7 days

Modalities with fewer than three follow-up encounters are suppressed in Figure 5 and in the printed booking table.

## Running it

Python 3.12.10. Set `BASE` in the first cell to the directory holding the data, which the notebook expects to be laid out as:

```
{BASE}/data/df_primary.parquet                    encounter-level records
{BASE}/data/df_population.parquet                 patient characteristics + CCI
{BASE}/data/df_tilastokeskus.parquet              annual population denominators
{BASE}/data/df_tilastokeskus_detailed.parquet     denominators by age and sex
{BASE}/data/df_omameh.parquet                     separate digital system, 2021–2022
{BASE}/data/df_omameh2023.parquet                 separate digital system, 2023
{BASE}/raw_data/THL_ICD-10_codes_Simple.xlsx      ICD-10 code labels
{BASE}/raw_data/THL_ICPC-2_Simple.xlsx            ICPC-2 code labels
```

Figures are written to `{BASE}/results/figures/`. Cells run in order; `ENCOUNTER_TYPES_MAIN` in the Table 1 cell defines the encounter inclusion set and feeds everything downstream, so changing it changes all coverage, utilisation and person-year results.

## Data Availability

Patient-level data isn't shared (privacy / data protection). Analysis used pseudonymised data under the Finnish Act on Secondary Use of Health and Social Data (552/2019), approved by the Päijät-Häme Wellbeing Services County (HA/187/07.01.04.05/2025).

## References

- Harris CR, Millman KJ, van der Walt SJ, et al. Array programming with NumPy. *Nature* 585, 357–362 (2020). https://doi.org/10.1038/s41586-020-2649-2
- The pandas development team. pandas-dev/pandas: Pandas. Zenodo (2020). https://doi.org/10.5281/zenodo.3509134
- Virtanen P, Gommers R, Oliphant TE, et al. SciPy 1.0: fundamental algorithms for scientific computing in Python. *Nature Methods* 17, 261–272 (2020). https://doi.org/10.1038/s41592-019-0686-2
- Seabold S, Perktold J. statsmodels: Econometric and statistical modeling with Python. *Proceedings of the 9th Python in Science Conference* (2010).
- Hunter JD. Matplotlib: A 2D Graphics Environment. *Computing in Science & Engineering* 9, 90–95 (2007). https://doi.org/10.1109/MCSE.2007.55
- Waskom ML. seaborn: statistical data visualization. *Journal of Open Source Software* 6, 3021 (2021). https://doi.org/10.21105/joss.03021
- Plotly Technologies Inc. Collaborative data science. Montréal, QC (2015). https://plot.ly

## Citation

```
@article{dahlberg2026coverage,
  title   = {Coverage, Utilisation and Users of a Chat-Based Digital Primary Care Clinic in Publicly Funded Healthcare: A Registry-Based Observational Study in Finland},
  author  = {Dahlberg, Alexandra and Kaartinen, Taavi and Jukarainen, Sakari and Orre, Petja},
  year    = {2026},
  journal = {medRxiv},
  doi     = {10.1101/2025.11.06.25339651}
}
```