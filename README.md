# 🌍 Global BIN Database Premium (2026 Edition)
### Professional Grade Card Issuing Data | 6 to 11-Digit Precision

This repository provides a high-performance, global BIN (Bank Identification Number) database. While the provided **sample focuses on major markets (USA, Europe, Asia)**, the full database covers **all 249+ ISO countries and territories** and over **3.5 million unique ranges**.

---

## 💎 Why Precision Matters (6 vs 11 Digits)
Standard databases limited to 6 digits are obsolete. Modern card issuing uses 8, 9, 10, and 11-digit ranges to differentiate between products, currencies, and sub-brands within a single bank.

**Our Waterfall Lookup Logic:**
To ensure 100% routing accuracy, implement a descending search:
`11-digits` → `10-digits` → `9-digits` → `8-digits` → `6-digits`.

---

## 🛠 Detailed Field Specification

The database is provided in `.csv` format (Semicolon separated `;`).

### 🟦 Core Identification (Fields 1-14)
| # | Field Name | Description | Example |
|---|---|---|---|
| 1 | **BIN** | Card prefix (6, 8, 9, 10, or 11 digits) | `467122502` |
| 2 | **Brand** | Card scheme (VISA, MASTERCARD, AMEX, JCB, etc.) | `VISA` |
| 3 | **Issuer** | Name of the issuing organization/bank | `HANA CARD` |
| 4 | **Type** | Card type: `DEBIT`, `CREDIT`, or `CHARGE CARD` | `CREDIT` |
| 5 | **Category** | Product level: `CLASSIC`, `GOLD`, `PLATINUM`, `WORLD`, etc. | `CLASSIC` |
| 6 | **Country Name** | Full name of the issuing country | `KOREA, REPUBLIC OF` |
| 7 | **ISO A2** | 2-letter country code (ISO 3166-1) | `KR` |
| 8 | **ISO A3** | 3-letter country code (ISO 3166-1) | `KOR` |
| 9 | **ISO Number** | Numeric country code | `410` |
| 10 | **Website** | Official website of the issuer | `WWW.HANACARD.CO.KR` |
| 11 | **Phone** | Customer service phone of the issuer | `82-1544-3500` |
| 12 | **PAN Length** | Total digits on the card (Primary Account Number) | `16` |
| 13 | **Usage** | Segment: `PERSONAL` or `COMMERCIAL` | `PERSONAL` |
| 14 | **Regulated** | Interchange fee status: `Y` (Regulated) or `N` (Unregulated) | `N` |

### 🟩 Advanced Fintech & Payout Data (Fields 15-29)
*Crucial for Payment Service Providers (PSPs) and Neobanks.*

| # | Field Name | Technical Definition |
|---|---|---|
| 15 | **DebitNetwork** | US Debit networks (e.g., Star, Pulse, NYCE) - *USA only* |
| 16 | **ATMNetwork** | ATM regional networks - *USA only* |
| 17 | **CommL2 Support** | Commercial Level 2 data support (Y/N) |
| 18 | **CommL3 Support** | Commercial Level 3 data support (Y/N) |
| 19 | **FF_Dom** | **Fast Funds Domestic:** Supports instant payouts within the same country |
| 20 | **FF_Cross** | **Fast Funds Cross-border:** Supports instant international payouts |
| 21 | **MS_Ind** | **Mastercard MoneySend:** Specific indicator for MC push-payments |
| 22 | **Push_Dom** | Generic Push Funds support (Domestic) |
| 23 | **Push_Cross** | Generic Push Funds support (Cross-border) |
| 24 | **MT_Ind** | **Visa Money Transfer:** Specific indicator for Visa push-payments |
| 25 | **OG_FF_Dom** | **Online Gambling FF:** Supports payouts for gambling merchants (Domestic) |
| 26 | **OG_FF_Cross** | **Online Gambling FF:** Supports payouts for gambling merchants (Cross-border) |
| 27 | **Pull_Dom** | Support for Pull-funds (Direct Debit style transactions) |
| 28 | **Token** | **Token BIN Range:** Identifies Apple Pay, Google Pay, and other virtual tokens |
| 29 | **Currency** | ISO 3-digit currency code (e.g., `USD`, `EUR`, `GBP`) |

---

## 📈 Regional Coverage
- **North America:** Deep data for Durbin Amendment (Regulated) and US Debit Networks.
- **Europe (EEA):** Full interchange optimization data (Personal vs Commercial).
- **Asia-Pacific:** Advanced support for 11-digit BINs (UnionPay, JCB).
- **LATAM & MEA:** Growing coverage for local schemes and neobanks.

## 📥 Sample Data
The `bin_database_sample_2026.csv` file contains **50,000 records** specifically selected to demonstrate:
1. "Cluster" structures (how one prefix splits into many products).
2. Advanced fields (FF, MS, Currency) in action.
3. High-precision (8-11 digit) examples.

---

## 📬 Contact & Full Version
The full database (3.5M+ rows) is available via subscription or one-time purchase.

**Official Website:** [www.binbase.com](https://www.binbase.com)  
**Email:** [support@binbase.com]  
**Updates:** Data refreshed weekly.
