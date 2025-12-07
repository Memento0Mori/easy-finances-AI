## 📈 Easy Finances AI  
**Short-term Stock Movement Prediction System**

Easy Finances AI è un progetto sviluppato per analizzare e prevedere il comportamento a breve termine di un titolo azionario, applicando tecniche di Machine Learning e seguendo il processo CRISP-DM.  
L’obiettivo è studiare come modelli supervisionati reagiscono ai dati finanziari reali e confrontare approcci diversi alla previsione dei mercati.

---

## 🎯 Obiettivi del progetto

Il sistema affronta il problema da due prospettive complementari:

### **1️⃣ Pipeline A – Regressione**
Predizione del *ritorno percentuale* del prezzo del giorno successivo.  
Consente di stimare **di quanto** il titolo potrebbe salire o scendere.

- **Modelli utilizzati:**  
  - Linear Regression  
  - KNN Regressor  
- **Metriche:** MAE, MSE, RMSE  
- **Output:** grafici “predetto vs reale”, distribuzione degli errori

---

### **2️⃣ Pipeline B – Classificazione UP/DOWN**
Previsione della **direzione** del movimento (sale/scende).  
L’etichetta deriva sia dai dati originali sia dal valore predetto dalla regressione.

- **Modelli utilizzati:**  
  - Decision Tree  
  - Logistic Regression  
  - Naive Bayes  
- **Metriche:** Accuracy, Precision, Recall, F1-score  
- **Output:** confusion matrix, confronto tra modelli

---

## 📊 Dataset

Il dataset è composto da dati storici del mercato, contenenti:

- Prezzo di apertura (*Open*)
- Prezzo massimo (*High*)
- Prezzo minimo (*Low*)
- Prezzo di chiusura (*Close*)
- Volume degli scambi (*Volume*)

Le feature generate includono:

- Ritorni percentuali giornalieri
- Medie mobili (short-term / long-term)
- Indicatori sintetici basati sul prezzo
- Volumi normalizzati

Il dataset è suddiviso temporalmente in **train** e **test** per evitare data leakage.

---

## 🧹 Data Preparation

Le principali operazioni di preprocessing sono:

- Ordinamento temporale  
- Calcolo del target (ritorno e UP/DOWN)  
- Gestione dei valori mancanti  
- Feature engineering  
- Normalizzazione (dove necessario)  
- Creazione del train/test split basato sulle date  

---

## 🧠 Metodologia

Il progetto segue il modello **CRISP-DM**, che comprende:

1. *Business Understanding*  
2. *Data Understanding*  
3. *Data Preparation*  
4. *Modeling*  
5. *Evaluation*  
6. *Deployment / Interpretazione dei risultati*

Ogni passaggio è documentato nei notebook e nella relazione finale.

---
## 📂 Struttura del repository

  ```bash
  easy-finances-AI/
  │
  ├── data/
  │   ├── raw/            # dati originali
  │   └── processed/      # dati puliti e feature-ready
  │
  ├── notebooks/
  │   ├── EDA.ipynb       # analisi esplorativa
  │   ├── regression.ipynb    # pipeline A
  │   └── classification.ipynb  # pipeline B 
  │
  ├── src/
  │   ├── preprocessing.py
  │   ├── regression_models.py
  │   ├── classification_models.py
  │   └── utils.py
  │
  ├── report/
  │   └── main.tex        # relazione in LaTeX
  │
  │
  └── README.md
  ```
---
## 📦 Tecnologie utilizzate

- Python 3  
- NumPy, Pandas  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  
- LaTeX per la documentazione  

---

## 📘 Relazione finale

La documentazione in LaTeX include:

- PEAS del sistema
- Formalizzazione del problema
- Analisi del dataset
- Dettagli sulle due pipeline
- Metriche di valutazione
- Confronto tra i modelli
- Discussione dei limiti e possibili estensioni

---

## 🚀 Come eseguire il progetto

1. Installare le dipendenze:
   ```bash
   pip install -r requirements.txt
2. Aprire i notebook nella cartella notebooks/.

3. Eseguire prima la parte di preprocessing.

4. Lanciare le pipeline A e B.

4. Consultare grafici e metriche generati.

---

## 📄 Licenza

Questo progetto è distribuito sotto licenza MIT.

---

## ✨ Credits

Progetto sviluppato come esercitazione didattica per l'analisi predittiva dei mercati finanziari tramite tecniche di apprendimento automatico.
