# 🌍 Global BIN Database Premium (2026 Edition)
### Professional Grade Card Issuing Data | 3,294,052 Records | 6 to 11-Digit Precision

This repository provides a high-performance, global BIN (Bank Identification Number) database. Engineered for payment processors, fintech platforms, and fraud prevention systems, our dataset offers surgical precision beyond the outdated 6-digit standard.

---

## 💎 Why Precision Matters (The 11-Digit Standard)
Modern card issuing uses extended ranges to differentiate products, currencies, and sub-brands. **Over 88% of our database consists of high-precision ranges (8-11 digits).** **Our Waterfall Lookup Logic:**
To ensure 100% routing accuracy, implement a descending search:
`11-digits` → `10-digits` → `9-digits` → `8-digits` → `6-digits`.

---

## 📊 Database Statistics & Market Highlights

### BIN Precision Distribution
| Range | Records | Percentage |
| :--- | :--- | :--- |
| **6-digit BINs** | 375,523 | 11.40% (Standard) |
| **8-digit BINs** | 510,565 | 15.50% (New ISO) |
| **9-digit BINs** | 1,439,224 | **43.69% (Ultra-High)** |
| **10-digit BINs** | 951,134 | 28.87% (Deep Product) |
| **11-digit BINs** | 17,605 | 0.53% (Specialized) |

### 🌐 Key Market Coverage
Our database is optimized for the world's most active card markets:
* **North America (USA & Canada):** 1,168,757 records (35.48%). Full support for Durbin Amendment (Regulated) flags.
* **Europe (UK, Nordics, EEA):** 418,964 records (12.72%). Interchange optimization for Personal vs Commercial.
* **Asia-Pacific (Japan, Korea, China, India):** 357,238 records (10.84%). Advanced support for CUP, JCB, and RuPay.
* **Latin America (Brazil & Mexico):** 88,770 records focused on fast-growing fintech issuers like NuBank.

### 💳 Supported Brands (Highlights)
`VISA` • `MASTERCARD` • `AMERICAN EXPRESS` • `CHINA UNION PAY` • `JCB` • `DISCOVER` • `DINERS CLUB` • `RUPAY` • `ELO` • `MIR` • `TROY` • `HIPERCARD` • `MAESTRO` • `FUEL CARDS` (Wex, Shell).

---

## 🛠 Extended Data Dictionary (29 Fields)

The database is delivered as a CSV file using `;` as a separator.

### 🟦 Phase 1: Core Card & Issuer Data
| # | Field Name | Detailed Description | Business Value |
| :--- | :--- | :--- | :--- |
| **1** | **BIN** | The prefix (6–11 digits). | Primary key for identification. |
| **2** | **Brand** | Card scheme (e.g., VISA, MASTERCARD). | Determines transaction rules. |
| **3** | **Issuer** | Issuing bank name. | KYC and white-listing. |
| **4** | **Type** | DEBIT, CREDIT, or CHARGE. | Risk profiling and fee calculation. |
| **5** | **Category** | Product tier (PLATINUM, WORLD, etc.). | Identify VIP/high-limit cards. |
| **6** | **Country** | Full name of issuing country. | Geo-fencing/Local compliance. |
| **7-9** | **ISO Codes** | A2, A3, and Numeric ISO codes. | API and legacy system compatibility. |
| **10-11**| **Contact** | Issuer Website & Phone. | Manual verification & support. |
| **12** | **PAN Len** | Total digits on card (12–19). | Front-end input validation. |
| **13** | **Usage** | PERSONAL vs. COMMERCIAL. | Impact on Interchange Fees (ICF). |
| **14** | **Regulated** | Y/N status (e.g., US Durbin status). | Critical for US fee optimization. |

### 🟩 Phase 2: Advanced Fintech & Payout Specs
| # | Field Name | Detailed Description | Business Value |
| :--- | :--- | :--- | :--- |
| **15-16**| **Net Info** | US Debit & ATM networks (STAR, NYCE). | Routing cost reduction in USA. |
| **17-18**| **Comm L2/L3**| Commercial Data support levels. | Required for B2B/Corporate reporting. |
| **19-20**| **Fast Funds**| FF Domestic & Cross-border support. | **Essential for instant payouts.** |
| **21** | **MS Ind** | Mastercard MoneySend indicator. | MC "Push-to-Card" protocol. |
| **24** | **MT Ind** | Visa Money Transfer indicator. | Visa Direct payout protocol. |
| **25-26**| **OG FF** | Online Gambling FF (Domestic/Cross). | **Critical for Betting/Gaming industry.** |
| **27** | **Pull Dom** | Support for Direct Debit / Pull-funds. | Subscription/Recurring billing. |
| **28** | **Token** | Tokenized Range (Apple/Google Pay). | Digital wallet identification. |
| **29** | **Currency** | Default ISO currency (USD, EUR, etc.). | Dynamic currency conversion (DCC). |

---

## ⌨️ Implementation for Developers
Ready-to-use code snippets for **Python, PHP, and SQL** to handle waterfall lookups.

👉 **[View Implementation Guide & Code Snippets](./examples/implementation_guide.md)**

---

## 💳 Get the Full Database
The full version (3.2M+ rows) is updated weekly.

| Edition | Records | Updates | Format |
| :--- | :--- | :--- | :--- |
| **Sample** | 50,000 | N/A | [Download Here](./bin_database_sample_2026.csv) |
| **Full Premium** | 3,294,052 | Weekly | CSV / SQL / JSON |

**Official Website:** [www.binbase.com](https://www.binbase.com)  
**Inquiries:** [sales@binbase.com]  
