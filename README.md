# OTIF & Backorder Risk – Mini Supply-Chain Analytics Project  

**Goal:** Show how a business-minded analyst turns raw operations data into decisions.  
We simulate orders, lead times, and inventory, then build:
- a **Backorder Risk Score** for open orders  
- **OTIF (On-Time In-Full)** KPIs  
- a short **storytelling summary** for stakeholders  

> This project is intentionally simple and transparent — perfect for interview prep and portfolio work.  

---

## 💼 Why it matters  
- **Stockouts** hurt revenue and customer trust.  
- Leaders don’t want complex models; they want clear signals: “Where are we at risk and what should we do?”

---

## 🗂️ Repo structure  
```
supply-chain-otif-risk/
├─ data/                  # synthetic CSVs (you can add later)
├─ notebooks/
│  └─ 01_eda_risk.ipynb   # EDA + risk scoring
├─ src/
│  └─ utils.py            # helper functions
├─ reports/figures/       # exported plots
├─ requirements.txt
└─ README.md
```

---

## ⚙️ Quick start
```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_eda_risk.ipynb
```

---

## 📊 Data dictionary (synthetic)
**orders.csv**
| Column | Description |
|:-------|:-------------|
| order_id | unique id |
| order_date | date placed |
| promise_date | promised ship date |
| ship_date | actual ship date |
| customer | anonymized |
| mpn | part number |
| qty | ordered quantity |
| priority | Low/Med/High |
| plant | DC / warehouse |
| lead_time_days | quoted lead time |

**inventory.csv**
| Column | Description |
|:-------|:-------------|
| date | snapshot date |
| mpn | part number |
| on_hand | inventory available |
| in_transit | goods on the way |
| safety_stock | minimum threshold |

---

## 💬 Interview story  
- “I built a lightweight risk score that flags 12–18 % of orders at risk before they miss promise.”  
- “It’s fully explainable and helps CS / Supply teams prioritize expedites.”  

---

**Author:** Sharvee Shrotriya  
**License:** MIT
