# Codebook - Regan et al. Data Supplement (public release)

**Source file:** `regan_et_al_data_supplement_public.dta`  
**Dataset label:** S&P 500 panel (time-varying): Compustat + Orbis, 2000-2025  
**Observations:** 10,527  
**Variables:** 98  

> **Anonymisation note:** The internal identifiers `gvkey` (Compustat) and `bvd_id_number` (Orbis) have been removed for external release and replaced by `firm_id`, a pseudonymous firm-level id (`id00001`-`id00798`) that is constant across each firm's yearly observations, preserving the panel structure.

> Fill in the **Description** field for any variable that lacks one. Labels read automatically from the `.dta` file are marked _(from file)_.

---

## Variable overview

| # | Variable | Type | Label / Description |
|---|----------|------|---------------------|
| 1 | `firm_id` | string | Anonymised firm identifier (replaces gvkey/bvd_id_number) |
| 2 | `fyear` | numeric (int) | Fiscal Year |
| 3 | `tic` | string | Ticker Symbol |
| 4 | `merge_status` | categorical | Matching result from merge |
| 5 | `matched` | numeric (int) | =1 if firm-year matched in both Compustat and Orbis |
| 6 | `sp500_member` | numeric (int) | =1 if firm was in S&P 500 in this year |
| 7 | `sector` | categorical | Sector (6-category classification) |
| 8 | `knowledge_sector` | numeric (float) | Dummy: Knowledge sector |
| 9 | `comp_pi` | numeric (float) | Pretax Income - Total |
| 10 | `orb_pi` | numeric (float) | Profit before tax (nominal USD) |
| 11 | `comp_revt` | numeric (float) | Revenue - Total |
| 12 | `orb_revt` | numeric (float) | Operating revenue / turnover (nominal USD) |
| 13 | `comp_txfed` | numeric (float) | Income Taxes - Current - Federal |
| 14 | `comp_txfo` | numeric (float) | Income Taxes - Current - Foreign |
| 15 | `comp_txc` | numeric (float) | Income Taxes - Current (Total) |
| 16 | `comp_txt` | numeric (float) | Income Taxes - Total |
| 17 | `etr_current` | numeric (float) | Current ETR (txc / pi) |
| 18 | `etr_federal` | numeric (float) | Federal ETR (txfed / pi) |
| 19 | `etr_foreign` | numeric (float) | Foreign ETR (txfo / pi) |
| 20 | `etr_total` | numeric (float) | Total ETR (txt / pi) |
| 21 | `post2022` | numeric (int) | =1 if year >= 2022 (Section 174 capitalisation) |
| 22 | `post_tcja` | numeric (int) | =1 if year >= 2018 (post-TCJA) |
| 23 | `knowledge_post2022` | numeric (float) | Knowledge × Post-2022 (DiD interaction) |
| 24 | `knowledge_post_tcja` | numeric (float) | Knowledge × Post-TCJA (DiD interaction) |
| 25 | `costat` | string | Company Status (A=Active, I=Inactive) |
| 26 | `curcd` | string | ISO Currency Code |
| 27 | `datafmt` | string | Data Format (STD=Standardized, SUMM=Summary) |
| 28 | `indfmt` | string | Industry Format (INDL=Industrial, FS=Financial) |
| 29 | `consol` | string | Consolidation Level (C=Consolidated) |
| 30 | `cik` | numeric (float) | SEC Central Index Key |
| 31 | `state` | string | State/Province Code |
| 32 | `comp_gdwl` | numeric (float) | Goodwill |
| 33 | `comp_intan` | numeric (float) | Intangible Assets - Total |
| 34 | `intano` | numeric (float) | Intangible Assets - Other |
| 35 | `tlcf` | numeric (float) | Tax Loss Carry Forward |
| 36 | `txdb` | numeric (float) | Deferred Taxes (Balance Sheet) |
| 37 | `txdba` | numeric (float) | Deferred Tax Asset - Long-Term |
| 38 | `txdbca` | numeric (float) | Deferred Tax Asset - Current |
| 39 | `txdbcl` | numeric (float) | Deferred Tax Liability - Current |
| 40 | `txditc` | numeric (float) | Deferred Taxes and Investment Tax Credit |
| 41 | `txndb` | numeric (float) | Net Deferred Tax Asset (Liability) - Total |
| 42 | `txndba` | numeric (float) | Net Deferred Tax Asset - Current |
| 43 | `txndbl` | numeric (float) | Net Deferred Tax Liability - Current |
| 44 | `txndbr` | numeric (float) | Net Deferred Tax Asset (Liability) - Noncurrent |
| 45 | `txp` | numeric (float) | Income Taxes Payable |
| 46 | `txr` | numeric (float) | Income Tax Refund |
| 47 | `comp_gp` | numeric (float) | Gross Profit (Loss) |
| 48 | `comp_pidom` | numeric (float) | Pretax Income - Domestic |
| 49 | `comp_pifo` | numeric (float) | Pretax Income - Foreign |
| 50 | `comp_txdfed` | numeric (float) | Income Taxes - Deferred - Federal |
| 51 | `comp_txdfo` | numeric (float) | Income Taxes - Deferred - Foreign |
| 52 | `comp_txdi` | numeric (float) | Income Taxes - Deferred (Total) |
| 53 | `txds` | numeric (float) | Income Taxes - Deferred - State |
| 54 | `txo` | numeric (float) | Income Taxes - Current - Other |
| 55 | `txs` | numeric (float) | Income Taxes - Current - State |
| 56 | `utxfed` | numeric (float) | Unrecognized Tax Benefits - Federal |
| 57 | `tdc` | numeric (float) | Deferred Charges |
| 58 | `txach` | numeric (float) | Tax Benefit from Stock Options |
| 59 | `txdc` | numeric (float) | Deferred Taxes (Cash Flow Statement) |
| 60 | `comp_txpd` | numeric (float) | Income Taxes Paid (Cash Flow) |
| 61 | `acqgdwl` | numeric (float) | Goodwill from Acquisitions |
| 62 | `acqintan` | numeric (float) | Intangible Assets from Acquisitions |
| 63 | `comp_emp` | numeric (float) | Number of Employees (thousands) |
| 64 | `nace4_prim` | numeric (int) | _(add description)_ |
| 65 | `sic` | numeric (float) | _(add description)_ |
| 66 | `sic_name` | string | _(add description)_ |
| 67 | `orb_ni` | numeric (float) | Profit after tax (net income, nominal USD) |
| 68 | `orb_cf` | numeric (float) | _(add description)_ |
| 69 | `orb_at` | numeric (float) | Total assets (nominal USD) |
| 70 | `orb_profmarg` | numeric (float) | _(add description)_ |
| 71 | `orb_mktcap` | numeric (float) | _(add description)_ |
| 72 | `orb_name2` | string | Firm name (consolidated parent) |
| 73 | `orb_intan` | numeric (float) | Total intangible assets (nominal USD) |
| 74 | `orb_cash` | numeric (float) | _(add description)_ |
| 75 | `orb_rd` | numeric (float) | _(add description)_ |
| 76 | `orb_emp` | numeric (float) | Number of employees |
| 77 | `orb_tax` | numeric (float) | Effective tax (nominal USD) |
| 78 | `orb_taxrate` | numeric (float) | Effective tax rate |
| 79 | `nace4_sec` | numeric (float) | NACE secondary code (cleaned to 4-digit integer) |
| 80 | `nace_4d` | numeric (float) | NACE main code (4-digit) |
| 81 | `nace_2d` | numeric (float) | NACE division (2-digit) |
| 82 | `CPI` | numeric (float) | Consumer Price Index (CPI) |
| 83 | `big_sectors` | numeric (float) | Broad sector (Knowledge vs Traditional) |
| 84 | `tech` | numeric (float) | Dummy: Tech |
| 85 | `pharma` | numeric (float) | Dummy: Pharma |
| 86 | `other_knowledge` | numeric (float) | Dummy: Other knowledge-intensive |
| 87 | `commodities_retail` | numeric (float) | Dummy: Commodities, retail and sales |
| 88 | `industry` | numeric (float) | Dummy: Industry and manufacturing |
| 89 | `other_services` | numeric (float) | Dummy: Other services |
| 90 | `traditional_sector` | numeric (float) | Dummy: Traditional sector |
| 91 | `log_revenue` | numeric (float) | Log(Total revenue) |
| 92 | `rev_per_emp` | numeric (float) | Revenue per employee ( / thousands) |
| 93 | `etr_total_pct` | numeric (float) | _(add description)_ |
| 94 | `etr_current_pct` | numeric (float) | _(add description)_ |
| 95 | `etr_federal_pct` | numeric (float) | _(add description)_ |
| 96 | `etr_foreign_pct` | numeric (float) | _(add description)_ |
| 97 | `sp500_pre` | numeric (int) | =1 if firm was in S&P 500 in 2017 (pre-TCJA) |
| 98 | `sp500_x_post` | numeric (int) | S&P 500 (pre) x Post-TCJA |

---

## Variable details

### 1. `firm_id`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Anonymised firm identifier (replaces gvkey/bvd_id_number)
- **Unique values:** 798

### 2. `fyear`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Fiscal Year
- **Range:** 2000 to 2025   |   **Unique values:** 26

### 3. `tic`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Ticker Symbol
- **Unique values:** 589

### 4. `merge_status`

- **Type:** categorical
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Matching result from merge
- **Value labels** (`merge_status`):
    - `0` = Compustat only
    - `1` = Orbis only
    - `2` = Matched

### 5. `matched`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** =1 if firm-year matched in both Compustat and Orbis
- **Range:** 0 to 1   |   **Unique values:** 2

### 6. `sp500_member`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** =1 if firm was in S&P 500 in this year
- **Range:** 1 to 1   |   **Unique values:** 1

### 7. `sector`

- **Type:** categorical
- **Non-missing:** 9,982 / 10,527  (missing: 545)
- **Label (from file):** Sector (6-category classification)
- **Value labels** (`sector`):
    - `0` = Tech
    - `1` = Pharma / Life Sciences
    - `2` = Other Knowledge-Intensive
    - `3` = Commodities / Retail
    - `4` = Industry / Manufacturing
    - `5` = Other Services
    - `6` = Financial Sector

### 8. `knowledge_sector`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Knowledge sector
- **Range:** 0 to 1   |   **Unique values:** 2

### 9. `comp_pi`

- **Type:** numeric (float)
- **Non-missing:** 9,192 / 10,527  (missing: 1,335)
- **Label (from file):** Pretax Income - Total
- **Range:** -108761 to 158826   |   **Unique values:** 8,086

### 10. `orb_pi`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Profit before tax (nominal USD)
- **Range:** -5.64938e+10 to 1.23485e+11   |   **Unique values:** 8,242

### 11. `comp_revt`

- **Type:** numeric (float)
- **Non-missing:** 9,192 / 10,527  (missing: 1,335)
- **Label (from file):** Revenue - Total
- **Range:** -1527.81 to 716924   |   **Unique values:** 8,960

### 12. `orb_revt`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Operating revenue / turnover (nominal USD)
- **Range:** 752000 to 6.48125e+11   |   **Unique values:** 9,083

### 13. `comp_txfed`

- **Type:** numeric (float)
- **Non-missing:** 7,981 / 10,527  (missing: 2,546)
- **Label (from file):** Income Taxes - Current - Federal
- **Range:** -23427 to 41425   |   **Unique values:** 5,160

### 14. `comp_txfo`

- **Type:** numeric (float)
- **Non-missing:** 7,682 / 10,527  (missing: 2,845)
- **Label (from file):** Income Taxes - Current - Foreign
- **Range:** -734 to 31377   |   **Unique values:** 4,095

### 15. `comp_txc`

- **Type:** numeric (float)
- **Non-missing:** 7,981 / 10,527  (missing: 2,546)
- **Label (from file):** Income Taxes - Current (Total)
- **Range:** -21515 to 45962   |   **Unique values:** 5,685

### 16. `comp_txt`

- **Type:** numeric (float)
- **Non-missing:** 9,192 / 10,527  (missing: 1,335)
- **Label (from file):** Income Taxes - Total
- **Range:** -34831 to 37162   |   **Unique values:** 6,590

### 17. `etr_current`

- **Type:** numeric (float)
- **Non-missing:** 7,453 / 10,527  (missing: 3,074)
- **Label (from file):** Current ETR (txc / pi)
- **Range:** 0 to 1   |   **Unique values:** 6,808

### 18. `etr_federal`

- **Type:** numeric (float)
- **Non-missing:** 7,453 / 10,527  (missing: 3,074)
- **Label (from file):** Federal ETR (txfed / pi)
- **Range:** 0 to 1   |   **Unique values:** 6,328

### 19. `etr_foreign`

- **Type:** numeric (float)
- **Non-missing:** 7,172 / 10,527  (missing: 3,355)
- **Label (from file):** Foreign ETR (txfo / pi)
- **Range:** 0 to 1   |   **Unique values:** 6,077

### 20. `etr_total`

- **Type:** numeric (float)
- **Non-missing:** 8,588 / 10,527  (missing: 1,939)
- **Label (from file):** Total ETR (txt / pi)
- **Range:** 0 to 1   |   **Unique values:** 7,926

### 21. `post2022`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** =1 if year >= 2022 (Section 174 capitalisation)
- **Range:** 0 to 1   |   **Unique values:** 2

### 22. `post_tcja`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** =1 if year >= 2018 (post-TCJA)
- **Range:** 0 to 1   |   **Unique values:** 2

### 23. `knowledge_post2022`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Knowledge × Post-2022 (DiD interaction)
- **Range:** 0 to 1   |   **Unique values:** 2

### 24. `knowledge_post_tcja`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Knowledge × Post-TCJA (DiD interaction)
- **Range:** 0 to 1   |   **Unique values:** 2

### 25. `costat`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Company Status (A=Active, I=Inactive)
- **Unique values:** 2

### 26. `curcd`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** ISO Currency Code
- **Unique values:** 3

### 27. `datafmt`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Data Format (STD=Standardized, SUMM=Summary)
- **Unique values:** 2

### 28. `indfmt`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Industry Format (INDL=Industrial, FS=Financial)
- **Unique values:** 2

### 29. `consol`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Consolidation Level (C=Consolidated)
- **Unique values:** 2

### 30. `cik`

- **Type:** numeric (float)
- **Non-missing:** 9,201 / 10,527  (missing: 1,326)
- **Label (from file):** SEC Central Index Key
- **Range:** 1800 to 2.01238e+06   |   **Unique values:** 588

### 31. `state`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** State/Province Code
- **Unique values:** 43

### 32. `comp_gdwl`

- **Type:** numeric (float)
- **Non-missing:** 8,601 / 10,527  (missing: 1,926)
- **Label (from file):** Goodwill
- **Range:** 0 to 146370   |   **Unique values:** 6,394

### 33. `comp_intan`

- **Type:** numeric (float)
- **Non-missing:** 8,895 / 10,527  (missing: 1,632)
- **Label (from file):** Intangible Assets - Total
- **Range:** 0 to 310197   |   **Unique values:** 7,528

### 34. `intano`

- **Type:** numeric (float)
- **Non-missing:** 8,213 / 10,527  (missing: 2,314)
- **Label (from file):** Intangible Assets - Other
- **Range:** 0 to 167742   |   **Unique values:** 5,846

### 35. `tlcf`

- **Type:** numeric (float)
- **Non-missing:** 5,783 / 10,527  (missing: 4,744)
- **Label (from file):** Tax Loss Carry Forward
- **Range:** 0 to 780800   |   **Unique values:** 3,362

### 36. `txdb`

- **Type:** numeric (float)
- **Non-missing:** 8,278 / 10,527  (missing: 2,249)
- **Label (from file):** Deferred Taxes (Balance Sheet)
- **Range:** -269 to 92344   |   **Unique values:** 5,398

### 37. `txdba`

- **Type:** numeric (float)
- **Non-missing:** 7,746 / 10,527  (missing: 2,781)
- **Label (from file):** Deferred Tax Asset - Long-Term
- **Range:** -78.185 to 35092   |   **Unique values:** 3,714

### 38. `txdbca`

- **Type:** numeric (float)
- **Non-missing:** 7,478 / 10,527  (missing: 3,049)
- **Label (from file):** Deferred Tax Asset - Current
- **Range:** 0 to 10349   |   **Unique values:** 2,179

### 39. `txdbcl`

- **Type:** numeric (float)
- **Non-missing:** 7,122 / 10,527  (missing: 3,405)
- **Label (from file):** Deferred Tax Liability - Current
- **Range:** 0 to 8484   |   **Unique values:** 706

### 40. `txditc`

- **Type:** numeric (float)
- **Non-missing:** 7,941 / 10,527  (missing: 2,586)
- **Label (from file):** Deferred Taxes and Investment Tax Credit
- **Range:** -269 to 92344   |   **Unique values:** 5,312

### 41. `txndb`

- **Type:** numeric (float)
- **Non-missing:** 8,861 / 10,527  (missing: 1,666)
- **Label (from file):** Net Deferred Tax Asset (Liability) - Total
- **Range:** -131000 to 55322   |   **Unique values:** 7,472

### 42. `txndba`

- **Type:** numeric (float)
- **Non-missing:** 8,391 / 10,527  (missing: 2,136)
- **Label (from file):** Net Deferred Tax Asset - Current
- **Range:** 0 to 830000   |   **Unique values:** 6,588

### 43. `txndbl`

- **Type:** numeric (float)
- **Non-missing:** 8,393 / 10,527  (missing: 2,134)
- **Label (from file):** Net Deferred Tax Liability - Current
- **Range:** -0.604 to 961000   |   **Unique values:** 6,955

### 44. `txndbr`

- **Type:** numeric (float)
- **Non-missing:** 8,470 / 10,527  (missing: 2,057)
- **Label (from file):** Net Deferred Tax Asset (Liability) - Noncurrent
- **Range:** -986 to 449   |   **Unique values:** 26

### 45. `txp`

- **Type:** numeric (float)
- **Non-missing:** 8,275 / 10,527  (missing: 2,252)
- **Label (from file):** Income Taxes Payable
- **Range:** -1346 to 26601   |   **Unique values:** 3,540

### 46. `txr`

- **Type:** numeric (float)
- **Non-missing:** 7,787 / 10,527  (missing: 2,740)
- **Label (from file):** Income Tax Refund
- **Range:** 0 to 7600   |   **Unique values:** 905

### 47. `comp_gp`

- **Type:** numeric (float)
- **Non-missing:** 9,192 / 10,527  (missing: 1,335)
- **Label (from file):** Gross Profit (Loss)
- **Range:** -76735 to 402370   |   **Unique values:** 8,638

### 48. `comp_pidom`

- **Type:** numeric (float)
- **Non-missing:** 6,272 / 10,527  (missing: 4,255)
- **Label (from file):** Pretax Income - Domestic
- **Range:** -105179 to 143591   |   **Unique values:** 5,548

### 49. `comp_pifo`

- **Type:** numeric (float)
- **Non-missing:** 6,246 / 10,527  (missing: 4,281)
- **Label (from file):** Pretax Income - Foreign
- **Range:** -11194 to 82000   |   **Unique values:** 5,079

### 50. `comp_txdfed`

- **Type:** numeric (float)
- **Non-missing:** 6,764 / 10,527  (missing: 3,763)
- **Label (from file):** Income Taxes - Deferred - Federal
- **Range:** -33819 to 32357   |   **Unique values:** 4,222

### 51. `comp_txdfo`

- **Type:** numeric (float)
- **Non-missing:** 7,142 / 10,527  (missing: 3,385)
- **Label (from file):** Income Taxes - Deferred - Foreign
- **Range:** -10979 to 5064   |   **Unique values:** 2,974

### 52. `comp_txdi`

- **Type:** numeric (float)
- **Non-missing:** 8,565 / 10,527  (missing: 1,962)
- **Label (from file):** Income Taxes - Deferred (Total)
- **Range:** -35561 to 36977   |   **Unique values:** 5,342

### 53. `txds`

- **Type:** numeric (float)
- **Non-missing:** 6,681 / 10,527  (missing: 3,846)
- **Label (from file):** Income Taxes - Deferred - State
- **Range:** -3415 to 1041   |   **Unique values:** 2,595

### 54. `txo`

- **Type:** numeric (float)
- **Non-missing:** 8,569 / 10,527  (missing: 1,958)
- **Label (from file):** Income Taxes - Current - Other
- **Range:** -623 to 1374   |   **Unique values:** 267

### 55. `txs`

- **Type:** numeric (float)
- **Non-missing:** 7,898 / 10,527  (missing: 2,629)
- **Label (from file):** Income Taxes - Current - State
- **Range:** -763 to 3342   |   **Unique values:** 3,474

### 56. `utxfed`

- **Type:** numeric (float)
- **Non-missing:** 691 / 10,527  (missing: 9,836)
- **Label (from file):** Unrecognized Tax Benefits - Federal
- **Range:** -1378.97 to 2875   |   **Unique values:** 505

### 57. `tdc`

- **Type:** numeric (float)
- **Non-missing:** 679 / 10,527  (missing: 9,848)
- **Label (from file):** Deferred Charges
- **Range:** -3055 to 2607   |   **Unique values:** 595

### 58. `txach`

- **Type:** numeric (float)
- **Non-missing:** 4,651 / 10,527  (missing: 5,876)
- **Label (from file):** Tax Benefit from Stock Options
- **Range:** -8028 to 18183   |   **Unique values:** 1,999

### 59. `txdc`

- **Type:** numeric (float)
- **Non-missing:** 8,389 / 10,527  (missing: 2,138)
- **Label (from file):** Deferred Taxes (Cash Flow Statement)
- **Range:** -35561 to 24877   |   **Unique values:** 4,894

### 60. `comp_txpd`

- **Type:** numeric (float)
- **Non-missing:** 8,958 / 10,527  (missing: 1,569)
- **Label (from file):** Income Taxes Paid (Cash Flow)
- **Range:** -6318 to 43369   |   **Unique values:** 5,903

### 61. `acqgdwl`

- **Type:** numeric (float)
- **Non-missing:** 1,862 / 10,527  (missing: 8,665)
- **Label (from file):** Goodwill from Acquisitions
- **Range:** 0 to 54220   |   **Unique values:** 1,574

### 62. `acqintan`

- **Type:** numeric (float)
- **Non-missing:** 1,749 / 10,527  (missing: 8,778)
- **Label (from file):** Intangible Assets from Acquisitions
- **Range:** 0 to 76920   |   **Unique values:** 1,407

### 63. `comp_emp`

- **Type:** numeric (float)
- **Non-missing:** 9,152 / 10,527  (missing: 1,375)
- **Label (from file):** Number of Employees (thousands)
- **Range:** 0 to 2300   |   **Unique values:** 4,518

### 64. `nace4_prim`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** _(none)_
- **Range:** 111 to 9610   |   **Unique values:** 183

### 65. `sic`

- **Type:** numeric (float)
- **Non-missing:** 9,315 / 10,527  (missing: 1,212)
- **Label (from file):** _(none)_
- **Range:** 100 to 8742   |   **Unique values:** 216

### 66. `sic_name`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** _(none)_
- **Unique values:** 217

### 67. `orb_ni`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Profit after tax (net income, nominal USD)
- **Range:** -9.7323e+10 to 1.00118e+11   |   **Unique values:** 8,083

### 68. `orb_cf`

- **Type:** numeric (float)
- **Non-missing:** 8,364 / 10,527  (missing: 2,163)
- **Label (from file):** _(none)_
- **Range:** -5.2049e+10 to 1.15429e+11   |   **Unique values:** 7,514

### 69. `orb_at`

- **Type:** numeric (float)
- **Non-missing:** 9,286 / 10,527  (missing: 1,241)
- **Label (from file):** Total assets (nominal USD)
- **Range:** 9.499e+06 to 4.00281e+12   |   **Unique values:** 9,172

### 70. `orb_profmarg`

- **Type:** numeric (float)
- **Non-missing:** 9,232 / 10,527  (missing: 1,295)
- **Label (from file):** _(none)_
- **Range:** -99.76 to 98.94   |   **Unique values:** 4,150

### 71. `orb_mktcap`

- **Type:** numeric (float)
- **Non-missing:** 8,040 / 10,527  (missing: 2,487)
- **Label (from file):** _(none)_
- **Range:** 252.1 to 3.54256e+06   |   **Unique values:** 8,009

### 72. `orb_name2`

- **Type:** string
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** Firm name (consolidated parent)
- **Unique values:** 778

### 73. `orb_intan`

- **Type:** numeric (float)
- **Non-missing:** 8,369 / 10,527  (missing: 2,158)
- **Label (from file):** Total intangible assets (nominal USD)
- **Range:** 0 to 1.90583e+11   |   **Unique values:** 6,751

### 74. `orb_cash`

- **Type:** numeric (float)
- **Non-missing:** 8,368 / 10,527  (missing: 2,159)
- **Label (from file):** _(none)_
- **Range:** 51000 to 1.50864e+11   |   **Unique values:** 7,188

### 75. `orb_rd`

- **Type:** numeric (float)
- **Non-missing:** 4,438 / 10,527  (missing: 6,089)
- **Label (from file):** _(none)_
- **Range:** 0 to 8.8544e+10   |   **Unique values:** 3,420

### 76. `orb_emp`

- **Type:** numeric (float)
- **Non-missing:** 8,332 / 10,527  (missing: 2,195)
- **Label (from file):** Number of employees
- **Range:** 7 to 2.3e+06   |   **Unique values:** 3,897

### 77. `orb_tax`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Effective tax (nominal USD)
- **Range:** -3.3554e+10 to 5.556e+10   |   **Unique values:** 7,119

### 78. `orb_taxrate`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Effective tax rate
- **Range:** -297.714 to 492   |   **Unique values:** 9,244

### 79. `nace4_sec`

- **Type:** numeric (float)
- **Non-missing:** 8,714 / 10,527  (missing: 1,813)
- **Label (from file):** NACE secondary code (cleaned to 4-digit integer)
- **Range:** 111 to 9699   |   **Unique values:** 173

### 80. `nace_4d`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** NACE main code (4-digit)
- **Range:** 111 to 9610   |   **Unique values:** 181

### 81. `nace_2d`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** NACE division (2-digit)
- **Range:** 1 to 96   |   **Unique values:** 68

### 82. `CPI`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Consumer Price Index (CPI)
- **Range:** 172.2 to 314.4   |   **Unique values:** 25

### 83. `big_sectors`

- **Type:** numeric (float)
- **Non-missing:** 7,942 / 10,527  (missing: 2,585)
- **Label (from file):** Broad sector (Knowledge vs Traditional)
- **Range:** 1 to 2   |   **Unique values:** 2

### 84. `tech`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Tech
- **Range:** 0 to 1   |   **Unique values:** 2

### 85. `pharma`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Pharma
- **Range:** 0 to 1   |   **Unique values:** 2

### 86. `other_knowledge`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Other knowledge-intensive
- **Range:** 0 to 1   |   **Unique values:** 2

### 87. `commodities_retail`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Commodities, retail and sales
- **Range:** 0 to 1   |   **Unique values:** 2

### 88. `industry`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Industry and manufacturing
- **Range:** 0 to 1   |   **Unique values:** 2

### 89. `other_services`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Other services
- **Range:** 0 to 1   |   **Unique values:** 2

### 90. `traditional_sector`

- **Type:** numeric (float)
- **Non-missing:** 9,293 / 10,527  (missing: 1,234)
- **Label (from file):** Dummy: Traditional sector
- **Range:** 0 to 1   |   **Unique values:** 2

### 91. `log_revenue`

- **Type:** numeric (float)
- **Non-missing:** 9,187 / 10,527  (missing: 1,340)
- **Label (from file):** Log(Total revenue)
- **Range:** 3.23958 to 13.4827   |   **Unique values:** 8,955

### 92. `rev_per_emp`

- **Type:** numeric (float)
- **Non-missing:** 9,150 / 10,527  (missing: 1,377)
- **Label (from file):** Revenue per employee ( / thousands)
- **Range:** -3637.65 to 143589   |   **Unique values:** 9,140

### 93. `etr_total_pct`

- **Type:** numeric (float)
- **Non-missing:** 8,588 / 10,527  (missing: 1,939)
- **Label (from file):** _(none)_
- **Range:** 0 to 100   |   **Unique values:** 7,926

### 94. `etr_current_pct`

- **Type:** numeric (float)
- **Non-missing:** 7,453 / 10,527  (missing: 3,074)
- **Label (from file):** _(none)_
- **Range:** 0 to 100   |   **Unique values:** 6,808

### 95. `etr_federal_pct`

- **Type:** numeric (float)
- **Non-missing:** 7,453 / 10,527  (missing: 3,074)
- **Label (from file):** _(none)_
- **Range:** 0 to 100   |   **Unique values:** 6,328

### 96. `etr_foreign_pct`

- **Type:** numeric (float)
- **Non-missing:** 7,172 / 10,527  (missing: 3,355)
- **Label (from file):** _(none)_
- **Range:** 0 to 100   |   **Unique values:** 6,077

### 97. `sp500_pre`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** =1 if firm was in S&P 500 in 2017 (pre-TCJA)
- **Range:** 0 to 1   |   **Unique values:** 2

### 98. `sp500_x_post`

- **Type:** numeric (int)
- **Non-missing:** 10,527 / 10,527  (missing: 0)
- **Label (from file):** S&P 500 (pre) x Post-TCJA
- **Range:** 0 to 1   |   **Unique values:** 2
