# Machine-Learning-on-UV-plasmonic-engineered-Auto-Fluorescence-Time-Decay-Series-AFTDS-

Based on the two code files you provided (`rf_knn_time_independent.py`, `lstm_rf_knn_time_dependent.py`) and the content of your paper, here's a clean, professional `README.md` you can use for your GitHub repository:

---

### 📘 `README.md`

````markdown
# Machine Learning on UV Plasmonic-Engineered Auto Fluorescence Time Decay Series (AFTDS)

This repository contains the full pipeline for classifying monoamine neurotransmitters—dopamine (DA), norepinephrine (NE), and DOPAC—using UV plasmonic-enhanced fluorescence time-series data and machine learning models including LSTM, KNN, and Random Forest.

---

## 🧪 Project Summary

We propose a label-free, probe-free methodology that combines:

- **Aluminum Concave Nanocubes (AlCNCs)**: used to amplify autofluorescence (AF) signals.
- **AFTDS (Auto Fluorescence Time Decay Series)**: time-resolved fluorescence profiles under UV exposure.
- **ML Algorithms**:
  - 🧠 Long Short-Term Memory (LSTM) – for time-series modeling
  - 🌲 Random Forest – ensemble decision trees for static data
  - 👥 K-Nearest Neighbors (KNN) – simple baseline classifier

---

## 📁 Repository Structure

```bash
.
├── rf_knn_time_independent.py       # ML models using static fluorescence spectra
├── lstm_rf_knn_time_dependent.py    # Full pipeline for time-series data using AFTDS
├── Data_Sima.zip                    # ZIP containing .txt files with AFTDS signals (add via GitHub Release)
├── LSTM_prepared_df.pkl             # Preprocessed dataset for LSTM training
├── README.md                        # This file
````

---

## 🧬 Data Format

### For Time-Dependent (`Data_Sima.zip`)

Each `.txt` file contains two columns:

```
TimeStep_1_Intensity1   Intensity2
TimeStep_2_Intensity1   Intensity2
...
```

* Filename encodes class label: e.g. `sample_NE_001_01_0.txt`
* These are parsed and padded into fixed-length series.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/AFTDS-ML.git
cd AFTDS-ML
```

### 2. Install Requirements (Colab or Local)

```bash
pip install numpy pandas scikit-learn matplotlib seaborn tensorflow
```

### 3. Upload ZIP Data

Due to GitHub file size limits, download `Data_Sima.zip` from the [Releases page](https://github.com/yourusername/AFTDS-ML/releases) and place it in the root folder.

---

## 📊 Models Included

| Model Type       | File                            | Description                                              |
| ---------------- | ------------------------------- | -------------------------------------------------------- |
| Time-Independent | `rf_knn_time_independent.py`    | Uses static features from UV-AF spectra                  |
| Time-Dependent   | `lstm_rf_knn_time_dependent.py` | Full pipeline with data parsing, padding, and LSTM model |

---

## 🧠 Results

* **LSTM on AFTDS (AlCNCs)**:
  Accuracy: **\~89%**
  Best at modeling time-dependence of fluorescent decay.

* **KNN / RF on AFTDS**:
  Accuracy: **\~85–87%**
  Suitable for fast, explainable baselines.

* **KNN / RF on AF-in-solution**:
  Lower accuracy (\~60–70%) due to reduced signal quality and no temporal data.

---

## 📄 Citation / Paper

If using this code or dataset, please cite the paper:

> **A novel approach for classifying Monoamine Neurotransmitters by applying Machine Learning on UV plasmonic-engineered Auto Fluorescence Time Decay Series (AFTDS)**
> Mohammad Mohammadi, Sima Najafzadehkhoei, George Vega Yon, Yunshan Wang (2025)

---

## 🙏 Acknowledgments

* University of Utah Technology Licensing Office (TLO)
* Utah Nanofab Cleanroom
* NSF and Micron Foundation through EMSAL

---

## 🔒 License

MIT License (or adapt to your preference)

```

---

Would you like me to:
- Save this `README.md` as a downloadable file?
- Or copy it into your repo directly?

Let me know how you'd like to use it!
```

