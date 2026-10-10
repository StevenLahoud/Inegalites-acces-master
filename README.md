# Access to Master's Programs in France — A Data Exploration

Exploratory analysis of **admission data for every Master's program in France** (MonMaster platform, 2024 and 2025 sessions), looking for geographical, gender and academic-background disparities.

## Questions explored

1. **Metropolitan France vs overseas territories:** how many students are admitted in each academy, and how much do universities recruit from their own students (internal recruitment)?
2. **Gender distribution:** are women under-represented in every scientific field, or only in some?
3. **Academic background:** what did admitted students do the year before (Licence, professional Licence, BUT, Master, not enrolled…), and how does Île-de-France differ from the rest of the country?

## Key findings

- Paris is by far the largest academic center, with **twice as many admitted students** as the second-largest academy (Lille). Martinique and Mayotte have no Master's program on the platform.
- Universities in **overseas territories recruit much more internally**, showing low student mobility from metropolitan France toward them.
- Women are the majority of applicants and admitted students in almost every broad field. Within sciences, however, **mathematics, computer science and physics remain male-dominated**, while biology and medicine are mostly female.
- The **Licence** is the main pathway to a Master's degree everywhere, but Île-de-France has a much more diverse intake, including many students coming from abroad or returning to study after working.

## Methods & visualizations

- Data cleaning and aggregation by academy, field and gender
- Bar charts and boxplots (student counts, internal recruitment rate)
- **Mosaic plots** of gender distribution by field, for applications and admissions
- **Maps with proportional pie charts** showing the previous enrollment of admitted students in each academy

## Tech stack

**R** · tidyverse (dplyr, ggplot2, forcats, stringr) · sf · scatterpie · gt · **Quarto**

## Data

- MonMaster admission results (Ministry of Higher Education): [data.enseignementsup-recherche.gouv.fr](https://data.enseignementsup-recherche.gouv.fr/explore/dataset/fr-esr-mon_master)
- Academy boundaries (Ministry of Education): [data.education.gouv.fr](https://data.education.gouv.fr/explore/assets/fr-en-contour-academies-2020/)

Raw data is not included in this repository.

## How to run

Install the required R packages:

```r
install.packages(c("tidyverse", "sf", "scatterpie", "gt"))
```

Then render the report:

```bash
quarto render report.qmd
```

## Authors

Group project — Master in Mathematics & Computer Science for Data Science, Université Paris Cité.

Steven Lahoud, Anthony Fernandez
