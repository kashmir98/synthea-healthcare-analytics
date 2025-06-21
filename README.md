# Synthea Healthcare Analytics

This project explores synthetic electronic health record (EHR) data generated using [Synthea](https://github.com/synthetichealth/synthea). It simulates real-world healthcare analytics workflows, focusing on diagnosis trends, procedure patterns, and encounter-level clinical relationships across demographic groups.

---

## 📦 Dataset

Synthetic patient data was generated using Synthea’s open-source simulator.

Core CSV files used:
- `patients.csv`
- `conditions.csv`
- `procedures.csv`
- `encounters.csv`

These represent simulated patient demographics, diagnoses (ICD-10/11 codes), clinical procedures (CPT), and encounter metadata.

---

## 🛠 Tools & Environment

- **Python 3**
- **Jupyter Notebook**
- **pandas**
- **matplotlib** (optional for future visualizations)

---

## 🧹 Data Preparation

- Merged patient, condition, procedure, and encounter data using patient and encounter IDs
- Converted `BIRTHDATE` to age
- Created categorical bins:  
  `['0–18', '19–35', '36–50', '51–65', '66–80', '80+']`
- Replaced missing values with `"NULL"` for presentation
- Filtered and grouped conditions and procedures by age, gender, and temporal context

---

## 🔍 Key Analyses

- Top ICD-10 diagnoses by frequency
- Procedure frequencies and co-occurrences
- Diagnosis-to-procedure pairings at the encounter level
- Gender-based and age-based diagnostic trends
- High-volume clinical flows (e.g., `Medication review → Depression screening`)

---

## 📊 Sample Insights

- "Medication review due" was the most frequent diagnosis, co-occurring most with behavioral health procedures.
- Stress, gingivitis, and part-time employment were also common coded findings.
- Diagnoses like gingivitis and viral sinusitis showed strong age stratification.
- Male/female diagnostic counts were roughly balanced, with minor skews in behavioral and oral health patterns.

---

## ▶️ How to Run

1. **Clone this repo**
   ```bash
   git clone https://github.com/yourusername/synthea-healthcare-analytics.git
   cd synthea-healthcare-analytics
