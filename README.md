# 📊 Sentiment Analysis of COPOM Minutes

This project applies **Natural Language Processing (NLP)** to analyze the sentiment expressed in official minutes from Brazil’s Central Bank (COPOM meetings), with the goal of extracting signals about macroeconomic expectations.

---

## 🚀 Overview

Central banks use communication as a key policy tool. This project leverages NLP techniques to analyze the **tone and sentiment** of COPOM minutes and explore their relationship with macroeconomic indicators.

We classify each document into one of the following sentiment categories:

- Concern  
- Uncertainty  
- Caution  
- Alert  
- Confidence  
- Optimism  
- Accommodation  

The objective is to understand how institutional language evolves over time and whether it provides insights into future economic dynamics.

---

## 📂 Dataset

- 📄 **Source:** Central Bank of Brazil API  
- 🗓️ **Period:** 1998 – 2025  
- 📊 **Documents:** 270 COPOM meeting minutes  

## ⚙️ Methodology

### 1. Data Collection
- Automated extraction of COPOM minutes via API
- Integration with macroeconomic data

### 2. Preprocessing
- Text cleaning and structuring
- Temporal alignment with economic indicators

### 3. Sentiment Classification
- Model: **LLaMA 3.3 8B (local inference)**
- Prompt-based classification into predefined sentiment categories

### 4. Analysis
- Frequency and temporal evolution of sentiments  
- Correlation analysis with macroeconomic variables  
- Co-occurrence networks of key terms  
- Comparative analysis across presidential terms  

---

## 🧠 Key Results

### Sentiment Distribution
![Distribution](Images/sentiment_dist.png)

- **Overall distribution:**  
  The dominant sentiment is **caution (29.2%)**, followed by **confidence (23.6%)** and **concern (22.8%)**, indicating a consistently **prudent and risk-aware communication strategy** by the Central Bank. Lower frequencies of **uncertainty (8.4%)** and **alert (8.4%)** reflect periods of heightened risk, while **optimism (4.4%)** and **accommodation (3.2%)** remain rare, reinforcing a conservative stance focused on stability and inflation control.

- **FHC (1998–2002):**  
  Dominated by **caution and concern**, reflecting macroeconomic stabilization and the 1999 currency crisis, with communication focused on anchoring expectations during institutional transition.

- **Lula I (2003–2006):**  
  Shift toward **confidence**, signaling stabilization and restored credibility after initial market uncertainty. Presence of optimism reflects improved economic conditions.

- **Lula II (2007–2010):**  
  More **balanced distribution**, with alert and concern during the 2008 global crisis, but also signs of optimism and accommodation, reflecting economic resilience.

- **Dilma I (2011–2014):**  
  Dominated by **concern and caution**, indicating declining macroeconomic conditions and reduced credibility of monetary policy.

- **Dilma II (2015–2016):**  
  Increase in **uncertainty and concern**, associated with deep economic and political crisis, reflecting low predictability and institutional pressure.

- **Temer (2016–2018):**  
  Mixed sentiments (**caution, confidence, uncertainty, concern**) during a transition period marked by attempts to restore stability and credibility.

- **Bolsonaro (2019–2022):**  
  Strong dominance of **caution**, especially during COVID-19 and global shocks, reflecting a conservative and risk-averse communication strategy.

- **Lula III (2023–2025):**  
  Return of **confidence**, alongside caution, signaling efforts to reinforce credibility and stability amid institutional and fiscal debates.

---

### Evolution Over Time
![Time](Images/time_series.png)

## 📈 Temporal Evolution of Sentiments

- **Accommodation:** Shows a small peak around 2010, following the global financial crisis, suggesting a brief period of relative monetary stabilization. Overall, it remains a rare sentiment.

- **Alert:** Peaks in 2008 during the global financial crisis, reflecting a vigilant stance by the Central Bank in response to heightened uncertainty and external risks.

- **Caution:** Most prominent during the COVID-19 pandemic (2020–2022), highlighting a prudent response to unprecedented shocks. Also appears in periods of political and economic volatility, such as 2012–2014, 2018, and early 2000s crises.

- **Confidence:** Peaks in 2000, 2003, and 2004, associated with macroeconomic stabilization periods. Notably absent during crisis years (e.g., 2009, 2015–2016, 2020), indicating reduced institutional confidence.

- **Uncertainty:** Reaches its highest level in 2016, during Brazil’s political and economic crisis, reflecting increased instability and unpredictability.

- **Optimism:** Peaks in 2005, during a period of economic growth and consolidation of macroeconomic policies.

- **Concern:** Appears strongly during crisis periods (1999, 2001, 2008, 2011, 2016), showing a direct link between economic stress and more cautious institutional communication.

### Sentiment Repercussion
![Time](Images/time_series.png)

We analyze how different sentiment tones in COPOM minutes relate to short-term macroeconomic dynamics:

- **Accommodation:** Associated with rising inflation (+5.82% IPCA), stock market gains, currency appreciation, and lower unemployment, suggesting a stable environment with less interventionist communication.

- **Alert:** Linked to declining inflation (-7.1%) alongside positive market performance, indicating a **preventive stance** by policymakers despite improving conditions.

- **Caution:** Reflects a **balanced scenario**, with moderate inflation increase, lower unemployment, and slight currency depreciation, consistent with a prudent and watchful policy approach.

- **Confidence:** Occurs in periods of strong inflation growth (+9.09%) and market optimism, signaling positive expectations despite inflationary pressure.

- **Uncertainty:** Associated with sharp inflation drops (-13.97%), currency depreciation, and weaker stock performance, indicating increased risk aversion and underlying economic fragility.

- **Optimism:** Linked to falling inflation and interest rates, along with modest market gains, suggesting improving economic conditions and policy easing.

- **Concern:** Characterized by rising interest rates and mixed signals across markets, reflecting a tightening stance to control inflation amid uncertain conditions.


---

## TL;DR
- **Caution, confidence, and concern** are the most frequent sentiments  
- Central Bank communication is predominantly **prudent and risk-aware**  
- Sentiment varies across political and economic cycles  
- Some patterns suggest that **institutional tone may anticipate economic movements**, although not in a strictly linear way
