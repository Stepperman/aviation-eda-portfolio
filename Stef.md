# ✈️ Aviation Accidents EDA - Universal Data Engine

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-green.svg)](https://pandas.pydata.org)
[![Plotly](https://img.shields.io/badge/Plotly-5.0+-orange.svg)](https://plotly.com)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **A modular, OOP-based Exploratory Data Analysis toolkit designed for reusability across industries.**

[🇬🇧 English](#english) | [🇮🇹 Italiano](#italiano)

---

<a name="english"></a>
# 🇬🇧 English

## 📋 Project Overview

This project provides a comprehensive Exploratory Data Analysis (EDA) of aviation accidents (1919-2023) using a **reusable OOP architecture**. The core component, `UniversalDataEngine`, is designed to be **industry-agnostic** and can be easily adapted for sales, healthcare, finance, or any tabular dataset.

### Key Features

- 🧹 **Automated Data Cleaning** - Multi-format date parsing, string normalization, missing value handling
- 📈 **Temporal Analysis** - Time series trends, seasonality detection, decade comparisons
- 📊 **Categorical Analysis** - Distribution analysis, top-N rankings, cross-tabulations
- 🗺️ **Geospatial Analysis** - Interactive choropleth maps with Plotly
- 🔬 **Outlier Detection** - IQR-based statistical outlier identification
- 📦 **Modular Design** - Each analysis method is independent and chainable

---

## 🏗️ Architecture

### Class Diagram

```
┌─────────────────────────────────────────────────────────────┐
│                   UniversalDataEngine                        │
├─────────────────────────────────────────────────────────────┤
│ Attributes:                                                  │
│   - df_raw: pd.DataFrame      # Original data (immutable)   │
│   - df: pd.DataFrame          # Cleaned data                │
│   - cleaning_stats: CleaningStats  # Cleaning metrics       │
├─────────────────────────────────────────────────────────────┤
│ Private Methods:                                             │
│   - _parse_date(str) → Timestamp                            │
│   - _extract_fatalities(str) → Tuple[int, int, bool]        │
│   - _remove_outliers_iqr(Series) → Series[bool]             │
├─────────────────────────────────────────────────────────────┤
│ Public Methods:                                              │
│   - clean(remove_outliers=False) → self                     │
│   - eda_temporal(show_911=True) → Dict                      │
│   - eda_categorical() → Dict                                │
│   - eda_geospatial() → Dict                                 │
└─────────────────────────────────────────────────────────────┘
```

### Design Principles

| Principle | Implementation |
|-----------|----------------|
| **Immutability** | `df_raw` is never modified |
| **Method Chaining** | `clean()` returns `self` |
| **Separation of Concerns** | Each EDA method is independent |
| **Fail-Safe Parsing** | Multiple format attempts before NaN |

---

## 🔄 Adapting for Other Industries

### Column Mapping Example

| Aviation | Sales | Healthcare |
|----------|-------|------------|
| `date` | `order_date` | `admission_date` |
| `fatalities` | `revenue` | `patient_count` |
| `country` | `region` | `hospital_region` |
| `type` | `product_category` | `diagnosis_code` |
| `operator` | `sales_rep` | `physician` |

---

## 📁 Project Structure

```
aviation-eda-portfolio/
├── data/
│   └── aviation_accidents.csv
├── notebooks/
│   └── Aviation_EDA_Final.ipynb
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

## 🚀 Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/aviation-eda-portfolio.git
cd aviation-eda-portfolio
pip install -r requirements.txt
jupyter notebook notebooks/Aviation_EDA_Final.ipynb
```

---

<a name="italiano"></a>
# 🇮🇹 Italiano

## 📋 Panoramica

Analisi esplorativa completa degli incidenti aerei (1919-2023) con architettura OOP riutilizzabile.

### Caratteristiche

- 🧹 **Pulizia Automatica** - Parsing date multi-formato, normalizzazione stringhe
- 📈 **Analisi Temporale** - Trend, stagionalità, confronti decennali
- 📊 **Analisi Categorica** - Distribuzioni, ranking, cross-tabulazioni
- 🗺️ **Analisi Geospaziale** - Mappe interattive Plotly
- 🔬 **Rilevamento Outlier** - Metodo IQR

---

## 🚀 Avvio Rapido

```bash
git clone https://github.com/YOUR_USERNAME/aviation-eda-portfolio.git
cd aviation-eda-portfolio
pip install -r requirements.txt
jupyter notebook notebooks/Aviation_EDA_Final.ipynb
```

---

## 📜 License

MIT License - See [LICENSE](LICENSE)

---

**Built with ❤️ and Python**
