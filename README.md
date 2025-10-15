## 🛢️ Oil & NRs: Nepal's Macroeconomic Balance 🇳🇵

Welcome to the `Global_oilprice_forex_reserve` repository! This project contains the data, code, and findings from my recent research paper, "The Impact of Global Oil Price Shocks on Nepal's Foreign Exchange Reserves and Inflation."

This study dives into the dynamic, one-way street linking volatile global crude oil prices (WTI) and the critical buffer of Nepal's Foreign Exchange Reserves (FER). For an import-dependent, small open economy like Nepal, this relationship is a core vulnerability—one that determines the country's economic resilience in a turbulent global energy market.

### 💡 The Core Challenge: A Vulnerable Buffer

Nepal, which relies heavily on petroleum imports and maintains a pegged exchange rate, feels immediate and severe pressure when global oil prices surge. This study uses a **Vector Autoregression (VAR) model** on **annual time-series data from 1979 to 2021** to quantify this vulnerability.

---

### 🔬 Key Findings: Unidirectional Causality and Dynamic Impact

The econometric analysis reveals a significant, **unidirectional causal relationship**:

* **Oil Prices ➡️ Reserves:** Fluctuations in the **Global Oil Price significantly Granger-cause** changes in Nepal's Foreign Exchange Reserves (p-value: 0.007884). This confirms that past oil price movements are a useful predictor for future reserve changes.
* **Reserves 🚫 Oil Prices:** Conversely, Nepal's Foreign Exchange Reserves **do not Granger-cause** the Global Oil Price (p-value: 0.1663). This aligns with the expectation that a small economy has negligible influence on global oil markets.

#### Dynamic Impact (Impulse Response)

A shock to the Global Oil Price has a **significant and dynamic impact** on the Foreign Exchange Reserve, with the effect eventually dissipating after about 10 periods.This dynamic pressure is driven by increased import costs, which widen the trade deficit and force the use of reserves to maintain the currency peg.

*A single, one-standard-deviation shock to the Global Oil Price leads to a prolonged, volatile response in the Foreign Exchange Reserve.*

---

### 🛠️ Methodology and Model Specs

The research employs a **VAR(4)** model on the second differences of the inflation-adjusted time series (dd\_op and dd\_reserve) to ensure stationarity.

* **Model Type:** Vector Autoregression (VAR) 
* **Data Period:** 1979–2021 (Annual) 
* **Key Variables (Second Differences):** Global Oil Price (WTI) and Foreign Exchange Reserves (FER), both in real 2021 US.
* **Lag Order:** $p=4$ (based on AIC, HQ, and FPE criteria).
* **Identification:** Recursive (Cholesky), with oil price ordered first.

#### Diagnostic Checks Confirmed:

* **Stationarity:** Confirmed via Augmented Dickey-Fuller (ADF) test on second-differenced series (dd\_op p-value: 0.01; dd\_reserve p-value: 0.03711).
* **No Serial Correlation:** Portmanteau Test p-value: 0.4.
* **No Heteroskedasticity (ARCH Effect):** ARCH Test p-value: 0.9934.
* **Stability:** Confirmed by OLS-CUSUM test (coefficients are stable over time).

---

### 🎯 Policy Recommendations

The findings underscore the need for macro-level policy adjustments to insulate Nepal's economy:

1.  **Strategic Reserve Management:** Maintain reserve buffers above standard import coverage during volatile oil periods, proactively accumulating during low-price cycle.
2.  **Energy Diversification:** Reduce structural oil import dependence by investing in **hydropower and renewable energy**.
3.  **Flexible Fuel Pricing:** Adopt a **partial pass-through mechanism** to balance the effects on consumer inflation and reserve conservation, which is currently strained by price stabilization policies.

### 📂 Repository Structure 

This repository will soon contain:

* **`data/`**: Raw and processed time-series data.
* **`code/`**: R scripts used for VAR estimation, diagnostics, and IRF/Granger Causality analysis.
* **`paper/`**: The final research paper (`Shubham_Upreti_Final_Paper.pdf`).

### ✍️ Author

**Shubham Upreti** (Individual Lumiere Research Scholar)
