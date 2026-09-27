# Socio-Demographic Determinants of Body Mass Index in Bangladesh (BDHS 2022)

![Project Banner](https://img.shields.badge/BRAC%20University-BTE317%20Biostatistics-0B132B?style=for-the-badge&logo=education)
![Dataset](https://img.shields.badge/Dataset-BDHS%202022%20(N%3D9%2C946)-48CAE4?style=for-the-badge)
![License](https://img.shields.badge/License-MIT-emerald?style=for-the-badge)
![Status](https://img.shields.badge/Status-Complete-brightgreen?style=for-the-badge)

An empirical bio-statistical investigation and interactive web dashboard exploring how socio-demographic drivers systematically shape Body Mass Index ($\text{BMI}$) profiles among Bangladeshi adults aged 15–49. The study utilizes secondary weighted sample data ($N = 9,946$) from the **Bangladesh Demographic and Health Survey (BDHS) 2022**.

---

## 📋 Table of Contents
- [Executive Overview](#-executive-overview)
- [Key Empirical Findings](#-key-empirical-findings)
- [Interactive Features](#-interactive-features)
- [Statistical Methodology](#-statistical-methodology)
- [Tech Stack](#-tech-stack)
- [Quick Start & Usage](#-quick-start--usage)
- [Repository Structure](#-repository-structure)
- [Citation](#-citation)
- [License](#-license)

---

## 📊 Executive Overview

Body Mass Index ($\text{BMI}$) serves as a fundamental metric for assessing population-level nutritional transitions in developing economies. Bangladesh currently faces a complex dual burden of malnutrition—where urban affluence drives rising overweight/obesity prevalence while rural undernutrition persists.

### Core Metrics Summary
* **Sample Size ($N$):** $9,946$ weighted respondents (BDHS 2022)
* **Mean Population BMI:** $23.84 \text{ kg/m}^2$ ($\text{SD} = 4.32$)
* **Normal Weight Cohort ($18.5 \le \text{BMI} \le 24.9$):** $53.2\%$ ($n = 5,291$)
* **Nutritional Risk Cohort (Underweight / Overweight / Obese):** $46.8\%$ ($n = 4,655$)
* **Age Distribution:** $15–49 \text{ years}$ (Mean age: $32.06 \text{ years}$)

---

## 📈 Key Empirical Findings

### 1. Primary Socio-Demographic Drivers ($\alpha = 0.05$)
Bivariate Pearson Chi-Square ($\chi^2$) hypothesis testing revealed four macro-structural variables as statistically significant drivers of body mass outcome:

| Predictor Variable | $\chi^2$ Statistic | Degrees of Freedom ($\text{df}$) | $p$-value | Empirical Insight |
| :--- | :---: | :---: | :---: | :--- |
| **Wealth Index Quintile** | $168.099$ | $4$ | $< 0.001$ | Poorest quintile is $60.0\%$ normal weight; Richest quintile is $58.1\%$ at-risk (overweight driven). |
| **Type of Residence** | $67.738$ | $1$ | $< 0.001$ | Rural dwellers exhibit $56.2\%$ normal BMI; Urban dwellers show $52.4\%$ at-risk prevalence. |
| **Administrative Division** | $26.325$ | $7$ | $< 0.001$ | Urbanized divisions (Dhaka, Chattogram) carry elevated non-communicable health risks. |
| **Educational Attainment** | $24.949$ | $3$ | $< 0.001$ | Higher education correlates with elevated body mass shifts ($49.9\%$ at-risk). |

### 2. Invariant Household Controls ($p > 0.05$)
* **Working Status:** $\chi^2 = 3.662, \text{df} = 1, p = 0.056$ (Statistically non-significant at $\alpha = 0.05$).
* **Sex of Household Head:** $\chi^2 = 0.699, \text{df} = 1, p = 0.403$ (No distinct predictive difference between male- and female-headed households).

### 3. Biological Impact of Aging (Linear Regression Model)
Univariable linear regression analysis quantifies the trajectory of BMI growth across adult age brackets ($15–49 \text{ years}$):

$$\text{BMI} = 20.724 + 0.097 \times (\text{Age})$$

* **Model Fit:** $F(1, 9944) = 414.231, p < 0.001, R^2 = 0.040, r = 0.200$
* **Interpretation:** Each additional year of age increases predicted body mass index by an average of $0.097 \text{ kg/m}^2$ from an intercept baseline of $20.724 \text{ kg/m}^2$.

---

## 💻 Interactive Features

The included web interface (`index.html`) provides a responsive dashboard for exploring and dynamic interaction:

1. **Pearson $\chi^2$ Interactive Viewer:** Switch seamlessly between Wealth, Residence, and Educational predictors to inspect live cross-tabulation metrics and test statistics.
2. **Dynamic BMI Predictor Simulator:** Adjust age, wealth tier, residence type, and education level sliders/selectors to calculate predicted $\text{BMI}$ values and risk categorizations in real-time.
3. **Interactive Charting:** Powered by Chart.js with animated tooltips and live scale updates.
4. **LaTeX Mathematical Formulations:** Rendered using MathJax v3 for equations and statistical indicators.
5. **One-Click Citation System:** Copy formal academic citation strings or access external source links to the full study PDF and BDHS databank.

---

## 🛠️ Tech Stack

* **Markup & Structure:** HTML5 (Semantic Structure)
* **Styling & Layout:** [Tailwind CSS](https://tailwindcss.com/) (CDN)
* **Data Visualization:** [Chart.js](https://www.chartjs.org/)
* **Typography & UI Icons:** Google Fonts (Inter), [Lucide Icons](https://lucide.dev/)
* **Mathematical Notation:** [MathJax v3](https://www.mathjax.org/) (TeX syntax)

---

## 🚀 Quick Start & Usage

No build step or server setup is required. The web application runs natively in any modern web browser.

### Running Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/bdhs-2022-bmi-analysis.git
   ```
2. Navigate to the project folder:
   ```bash
   cd bdhs-2022-bmi-analysis
   ```
3. Open `index.html` in your web browser:
   * **Linux/macOS:** `open index.html` or `xdg-open index.html`
   * **Windows:** `start index.html`
   * Or simply double-click `index.html` in your file explorer.

---

## 📁 Repository Structure

```
bdhs-2022-bmi-analysis/
├── index.html         # Main standalone interactive single-page dashboard
├── README.md          # Comprehensive project documentation
└── LICENSE            # MIT License
```

---

## 🎓 Citation

If you reference this analysis or use the interactive visualization in your research or course projects, please cite as follows:

### Text Citation
> Shakib, S. (2024). *Nutritional Status and Socio-Demographic Determinants of Body Mass Index in Bangladesh: An Empirical Analysis of BDHS 2022* (Course Code: BTE317). Department of Biotechnology, BRAC University.

### BibTeX Entry
```bibtex
@article{Shakib2024BDHS,
  author    = {Shadman Shakib},
  title     = {Nutritional Status and Socio-Demographic Determinants of Body Mass Index in Bangladesh: An Empirical Analysis of BDHS 2022},
  institution = {BRAC University, Department of Biotechnology},
  year      = {2024},
  note      = {Biostatistics Project BTE317}
}
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) - feel free to use, modify, and distribute for educational and academic research purposes.