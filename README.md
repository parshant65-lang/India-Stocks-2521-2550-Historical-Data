# India-Stocks-2521-2550-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2521 to 2550)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2521-2550-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2521 to 2550)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2521 | `VESUVIUS` | Vesuvius India Limited | `VESUVIUS.NS` |
| 2522 | `VETO` | Veto Switchgears And Cables Limited | `VETO.NS` |
| 2523 | `VGCL` | Vibrant Global Capital Limited | `VGCL.NS` |
| 2524 | `VGL` | VARVEE GLOBAL LIMITED | `VGL.NS` |
| 2525 | `VGUARD` | V-Guard Industries Limited | `VGUARD.NS` |
| 2526 | `VHL` | Vardhman Holdings Limited | `VHL.NS` |
| 2527 | `VHLTD` | Viceroy Hotels Limited | `VHLTD.NS` |
| 2528 | `VIDHIING` | Vidhi Specialty Food Ingredients Limited | `VIDHIING.NS` |
| 2529 | `VIDYAWIRES` | Vidya Wires Limited | `VIDYAWIRES.NS` |
| 2530 | `VIJIFIN` | Viji Finance Limited | `VIJIFIN.NS` |
| 2531 | `VIJSOLX` | Vijay Solvex Limited | `VIJSOLX.NS` |
| 2532 | `VIKASECO` | Vikas EcoTech Limited | `VIKASECO.NS` |
| 2533 | `VIKASLIFE` | Vikas Lifecare Limited | `VIKASLIFE.NS` |
| 2534 | `VIKRAMSOLR` | Vikram Solar Limited | `VIKRAMSOLR.NS` |
| 2535 | `VIKRAN` | Vikran Engineering Limited | `VIKRAN.NS` |
| 2536 | `VIMTALABS` | Vimta Labs Limited | `VIMTALABS.NS` |
| 2537 | `VINATIORGA` | Vinati Organics Limited | `VINATIORGA.NS` |
| 2538 | `VINCOFE` | Vintage Coffee And Beverages Limited | `VINCOFE.NS` |
| 2539 | `VINDHYATEL` | Vindhya Telelinks Limited | `VINDHYATEL.NS` |
| 2540 | `VINEETLAB` | Vineet Laboratories Limited | `VINEETLAB.NS` |
| 2541 | `VINNY` | Vinny Overseas Limited | `VINNY.NS` |
| 2542 | `VINYLINDIA` | Vinyl Chemicals (India) Limited | `VINYLINDIA.NS` |
| 2543 | `VIPCLOTHNG` | VIP Clothing Limited | `VIPCLOTHNG.NS` |
| 2544 | `VIPIND` | VIP Industries Limited | `VIPIND.NS` |
| 2545 | `VIPULLTD` | Vipul Limited | `VIPULLTD.NS` |
| 2546 | `VIRAT` | Virat Industries Limited | `VIRAT.NS` |
| 2547 | `VIRINCHI` | Virinchi Limited | `VIRINCHI.NS` |
| 2548 | `VIRTUALG` | Virtual Global Education Limited | `VIRTUALG.NS` |
| 2549 | `VISACHROME` | VISA Chrome Limited | `VISACHROME.NS` |
| 2550 | `VISAKAIND` | Visaka Industries Limited | `VISAKAIND.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream VESUVIUS 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2521-2550-Historical-Data/main/VESUVIUS/1m/2026/10/VESUVIUS_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
