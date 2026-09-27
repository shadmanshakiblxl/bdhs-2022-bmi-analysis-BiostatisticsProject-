


# Socio-Demographic Determinants of BMI in Bangladesh (BDHS 2022)


[![BRAC University](https://img.shields.io/badge/BRAC%20University-BTE317-0B132B)](https://www.bracu.ac.bd/)
[![Dataset](https://img.shields.io/badge/Dataset-BDHS%202022-48CAE4)](https://dhsprogram.com/pubs/pdf/FR386/FR386.pdf)

An interactive statistical visualizer and quantitative investigation examining how macro-level socio-demographic drivers systematically shape body mass profiles in Bangladesh. Based on secondary data from the **Bangladesh Demographic and Health Survey (BDHS) 2022** ($N = 9,946$).

---

## Executive Overview

Understanding population-level nutritional transitions is crucial for targeted public health policy. This study evaluates the dual burden of nutritional risk in Bangladesh—where undernutrition and overnutrition coexist—by testing the association between socio-demographic factors and Body Mass Index (BMI).

### Core Findings
- **Nutritional Risk Cohort**: **46.8%** of the sampled population falls into an at-risk BMI classification (underweight or overweight/obese), while **53.2%** maintain a normal BMI ($18.5 \le \text{BMI} < 25.0$).
- **Primary Macro Drivers**: Wealth quintile ($\chi^2 = 168.1$), type of residence ($\chi^2 = 67.7$), administrative division ($\chi^2 = 26.3$), and education level ($\chi^2 = 24.9$) exert the strongest, statistically significant ($p < 0.001$) structural influence on nutritional status.
- **Invariant Household Controls**: Household headship sex ($p = 0.403$) and current working status ($p = 0.056$) show negligible impact compared to economic and geographic factors.

---

## Key Statistical Results

### Bivariate Chi-Square ($\chi^2$) Analysis

| Predictor Variable | Pearson $\chi^2$ | Degrees of Freedom ($df$) | $p$-value | Significance Threshold ($\alpha = 0.05$) |
| :--- | :---: | :---: | :---: | :---: |
| **Wealth Index Quintile** | $168.099$ | $4$ | $< 0.001$ | Statistically Significant |
| **Type of Residence** (Urban/Rural) | $67.738$ | $1$ | $< 0.001$ | Statistically Significant |
| **Administrative Division** | $26.325$ | $7$ | $< 0.001$ | Statistically Significant |
| **Highest Education Level** | $24.949$ | $3$ | $< 0.001$ | Statistically Significant |
| **Current Working Status** | $3.662$ | $1$ | $0.056$ | Not Significant |
| **Sex of Household Head** | $0.699$ | $1$ | $0.403$ | Not Significant |

### Predictive Linear Regression (Age vs. Continuous BMI)

Pearson correlation reveals a weak but statistically significant positive linear relationship between age and continuous BMI ($r = 0.200, p < 0.001$).

$$\text{BMI} = 20.724 + 0.097 \times (\text{Age})$$

* **Sample Baseline**: At age 15, the predicted baseline BMI is $\sim 22.18\ \text{kg/m}^2$.
* **Annual Gradient**: Each additional year of age increases an individual's BMI by an average of $0.097\ \text{kg/m}^2$ ($F = 414.231, p < 0.001, t = 20.353$).

---

## Interactive Features

The included `index.html` dashboard provides an interactive presentation of the research paper:

1. **Chi-Square Profile Explorer**: Dynamically toggle between socio-demographic indicators to view comparative stacked bar charts and statistical parameters.
2. **Predictive BMI Trajectory Simulator**: Adjust respondent age (15–49) and socio-demographic status to calculate real-time estimated BMI and plot trajectory points against the linear model.
3. **Scroll Reveal & Responsive UI**: Built with a dark obsidian typography theme, animated section entrances, and clean tabular visualizers.

---

## Project Structure

```text
bdhs-2022-bmi-analysis/
├── index.html        # Interactive Web Dashboard & Visualizer
├── README.md         # Repository Documentation & Research Summary
└── LICENSE           # MIT License

```

---

## Tech Stack

* **Frontend Framework**: HTML5, Vanilla JavaScript (ES6+)
* **Styling**: [Tailwind CSS](https://tailwindcss.com/?utm_source=gemini)
* **Data Visualization**: [Chart.js](https://www.chartjs.org/?utm_source=gemini)
* **Math Rendering**: [MathJax v3](https://www.mathjax.org/?utm_source=gemini)
* **Iconography**: [Lucide Icons](https://lucide.dev/?utm_source=gemini)

---

## Getting Started

No server-side setup or dynamic build steps are required.



```


 **Run locally**:
Open `index.html` directly in any standard browser or serve it using a simple local HTTP server:
```bash
npx serve .

```



---

## Policy & Research Recommendations

* **Dual-Target Public Health Strategies**: Shift from "one-size-fits-all" programs toward targeted rural food security (combating undernutrition) and urban lifestyle awareness campaigns (addressing affluent overnutrition).
* **WHO Category Disaggregation**: Future research should disaggregate binary BMI groupings into standard 4-category WHO thresholds ($\text{Underweight}$, $\text{Normal}$, $\text{Overweight}$, $\text{Obese}$).
* **Multivariable Controls**: Implement multivariable logistic regression frameworks to control for co-dependent confounders, such as income-education collinearity.

---

## Author & Citation

* **Author**: Shadman Shakib
* **Course**: BTE317 - Biostatistics Project
* **Institution**: Department of Biotechnology, BRAC University
* **Data Source**: [Bangladesh Demographic and Health Survey (BDHS) 2022](https://dhsprogram.com/pubs/pdf/FR386/FR386.pdf)

### Citation

```bibtex
@misc{shakib2024bdhs,
  author = {Shakib, Shadman},
  title = {Nutritional Status and Socio-Demographic Determinants of Body Mass Index in Bangladesh: Statistical Analysis of BDHS 2022},
  institution = {BRAC University},
  year = {2024}
}

```

---

## License

This project is open-source and available for educational purpose 

```

<ElicitationsGroup message="Would you like help setting this up in Git?">
  <Elicitation label="Show terminal commands to push README to GitHub" query="Show me the step-by-step Git terminal commands to add this README file and push it to my GitHub repository."/>
  <Elicitation label="Generate a MIT LICENSE file" query="Generate a standard MIT License text file for this project."/>
</ElicitationsGroup>

```
