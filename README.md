

# Machine Learning on UV Plasmonic-Engineered Auto Fluorescence Time Decay Series (AFTDS)

This repository contains the full ML pipeline for classifying monoamine neurotransmitters—dopamine (DA), norepinephrine (NE), and DOPAC—using UV plasmonic-enhanced fluorescence and time-series decay data.


## 🧪 Project Summary

We propose a **label-free, probe-free** classification method by combining:

- **Plasmonic Aluminum Nanocubes (AlCNCs)** to amplify UV-induced autofluorescence (AF)
- **AFTDS (Auto Fluorescence Time Decay Series)** and static spectra
- **Machine Learning models** including:
  - 🧠 LSTM (for sequence modeling)
  - 🌲 Random Forest
  - 👥 KNN


## 📁 Files & Structure
```bash
.
├── RF-KNN/time_independent.py       # Static spectral ML pipeline (DA, NE, DOPAC)
├── LSTM-RF-KNN/time_dependent.py    # Full time-series model pipeline (AFTDS)
├── FLI_vs_Wv.xlsx                   # Static dataset (AF vs. Wavelength)
├── DATA_ML.zip                      # Time-series .txt files (AFTDS signals)
├── README.md                        # Project overview
```

## 📊 Datasets

### 🔹 `FLI_vs_Wv.xlsx`

* Static fluorescence intensity vs. wavelength
* Columns: `Wavelength`, `DA_*`, `DOPAC_*`, `NE_*`
* Used for classical ML (KNN, RF) with 2D vectors

### 🔹 `DATA_ML.zip`

* Contains `.txt` time-series files for each neurotransmitter
* File naming format: `*_DA_*.txt`, `*_NE_*.txt`, `*_DOPAC_*.txt`
* Each file contains 2 columns of signal readings across timesteps



## 🚀 How to Run

### 1. Clone and Install

```bash
git clone https://github.com/yourusername/AFTDS-ML.git
cd AFTDS-ML
pip install -r requirements.txt
```

### 2. Place Your Data

* Put `FLI_vs_Wv.xlsx` and `DATA_ML.zip` in the root of the repo
* If too large for Git, use [GitHub Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) or [Google Drive + gdown](https://github.com/wkentaro/gdown)

---

## 🧠 Models Included

| Model Type                    | File                            | Description                               |
| ----------------------------- | ------------------------------- | ----------------------------------------- |
| KNN + RF (Static)             | `rf_knn_time_independent.py`    | Uses data from `FLI_vs_Wv.xlsx`           |
| LSTM + RF + KNN (Time-Series) | `lstm_rf_knn_time_dependent.py` | Uses `DATA_ML.zip` or preprocessed `.pkl` |

---

## 📈 Results

| Model               | Accuracy | Notes                               |
| ------------------- | -------- | ----------------------------------- |
| **LSTM (AFTDS)**    | \~89%    | Best for sequence prediction        |
| **KNN/RF (AFTDS)**  | \~85–87% | Efficient for structured decay data |
| **KNN/RF (Static)** | \~60–70% | Lower due to spectral overlap       |

---

## 📄 Citation

> **A novel approach for classifying Monoamine Neurotransmitters using Machine Learning on UV plasmonic-engineered Auto Fluorescence Time Decay Series (AFTDS)**
> Mohammad Mohammadi, Sima Najafzadehkhoei, George Vega Yon, Yunshan Wang (2025)

---

## 🙌 Acknowledgments

* University of Utah TLO
* Utah Nanofab Cleanroom
* NSF + Micron Foundation via EMSAL

---

## 📜 License

MIT License (or as specified)

---




