## 🛢️ Oil & NRs: Nepal's Macroeconomic Balance 🇳🇵

Welcome to the `Global_oilprice_forex_reserve` repository! This project contains the data, code, and findings from my recent research paper, "The Impact of Global Oil Price Shocks on Nepal's Foreign Exchange Reserves and Inflation."

This study dives into the dynamic, one-way street linking volatile global crude oil prices (WTI) and the critical buffer of Nepal's Foreign Exchange Reserves (FER). For an import-dependent, small open economy like Nepal, this relationship is a core vulnerability—one that determines the country's economic resilience in a turbulent global energy market.

### 💡 The Core Challenge: A Vulnerable Buffer

[cite_start]Nepal, which relies heavily on petroleum imports and maintains a pegged exchange rate, feels immediate and severe pressure when global oil prices surge[cite: 12, 14, 53]. [cite_start]This study uses a **Vector Autoregression (VAR) model** on **annual time-series data from 1979 to 2021** to quantify this vulnerability[cite: 75, 103, 108].

---

### 🔬 Key Findings: Unidirectional Causality and Dynamic Impact

The econometric analysis reveals a significant, **unidirectional causal relationship**:

* [cite_start]**Oil Prices ➡️ Reserves:** Fluctuations in the **Global Oil Price significantly Granger-cause** changes in Nepal's Foreign Exchange Reserves (p-value: 0.007884)[cite: 244, 422]. [cite_start]This confirms that past oil price movements are a useful predictor for future reserve changes[cite: 245].
* [cite_start]**Reserves 🚫 Oil Prices:** Conversely, Nepal's Foreign Exchange Reserves **do not Granger-cause** the Global Oil Price (p-value: 0.1663)[cite: 249, 427]. [cite_start]This aligns with the expectation that a small economy has negligible influence on global oil markets[cite: 132].

#### Dynamic Impact (Impulse Response)

[cite_start]A shock to the Global Oil Price has a **significant and dynamic impact** on the Foreign Exchange Reserve, with the effect eventually dissipating after about 10 periods[cite: 260, 261, 271]. [cite_start]This dynamic pressure is driven by increased import costs, which widen the trade deficit and force the use of reserves to maintain the currency peg[cite: 276, 306].

[cite_start]*A single, one-standard-deviation shock to the Global Oil Price leads to a prolonged, volatile response in the Foreign Exchange Reserve[cite: 260, 261, 271].*

---

### 🛠️ Methodology and Model Specs

[cite_start]The research employs a **VAR(4)** model on the second differences of the inflation-adjusted time series (dd\_op and dd\_reserve) to ensure stationarity[cite: 122, 198, 201].

* [cite_start]**Model Type:** Vector Autoregression (VAR) [cite: 103]
* [cite_start]**Data Period:** 1979–2021 (Annual) [cite: 75]
* [cite_start]**Key Variables (Second Differences):** Global Oil Price (WTI) and Foreign Exchange Reserves (FER), both in real 2021 USD[cite: 82, 84, 118].
* [cite_start]**Lag Order:** $p=4$ (based on AIC, HQ, and FPE criteria)[cite: 194, 198, 412].
* [cite_start]**Identification:** Recursive (Cholesky), with oil price ordered first[cite: 131].

#### Diagnostic Checks Confirmed:

* [cite_start]**Stationarity:** Confirmed via Augmented Dickey-Fuller (ADF) test on second-differenced series (dd\_op p-value: 0.01; dd\_reserve p-value: 0.03711)[cite: 181, 407].
* [cite_start]**No Serial Correlation:** Portmanteau Test p-value: 0.472[cite: 208].
* [cite_start]**No Heteroskedasticity (ARCH Effect):** ARCH Test p-value: 0.9934[cite: 213].
* [cite_start]**Stability:** Confirmed by OLS-CUSUM test (coefficients are stable over time)[cite: 233, 236].

---

### 🎯 Policy Recommendations

The findings underscore the need for macro-level policy adjustments to insulate Nepal's economy:

1.  [cite_start]**Strategic Reserve Management:** Maintain reserve buffers above standard import coverage during volatile oil periods, proactively accumulating during low-price cycles[cite: 288, 289].
2.  [cite_start]**Energy Diversification:** Reduce structural oil import dependence by investing in **hydropower and renewable energy**[cite: 290].
3.  [cite_start]**Flexible Fuel Pricing:** Adopt a **partial pass-through mechanism** to balance the effects on consumer inflation and reserve conservation, which is currently strained by price stabilization policies[cite: 291, 292, 306].

### 📂 Repository Structure (Coming Soon)

This repository will soon contain:

* **`data/`**: Raw and processed time-series data (`1979_2021_nepal_data.csv`).
* **`code/`**: R scripts used for VAR estimation, diagnostics, and IRF/Granger Causality analysis.
* **`paper/`**: The final research paper (`Shubham_Upreti_Final_Paper.pdf`).

### ✍️ Author

[cite_start]**Shubham Upreti** (Individual Lumiere Research Scholar) [cite: 3, 4]
