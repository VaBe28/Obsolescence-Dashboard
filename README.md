#  Obsolescence Inventory Dashboard

A Power BI dashboard that analyzes inventory obsolescence using operational SAP MM logic, categorizing stock by movement age and estimating financial impact via yield cost.

> ⚠️ This is a sanitized version of a real project — the `.pbix` file is not included due to company confidentiality. Only the dashboard preview is shared.

---


## Preview

![Obsolescence Dashboard](Obsolescence%20Dashboard.png)

##  Overview

This dashboard delivers a strategic view of inventory health across plants and material types. It highlights:
- Aging of stock based on last movement
- Obsolete inventory value
- Estimated financial impact (5% yield cost)
- Evolution of obsolescence over time

---

##  Obsolescence Logic

Obsolescence is classified based on **months since last movement**:

| Category        | Condition               | Label         |
|----------------|--------------------------|----------------|
| No Movement     | No stock movement ever    | `No Movement`  |
| Obsolete        | >16 months               | `>16m`         |
| At Risk         | 12–16 months             | `12–16m`       |
| Monitor         | 6–12 months              | `6–12m`        |
| Active          | ≤6 months                | Not shown      |

These thresholds are implemented with DAX calculated columns and flags.

---

## 📈 Visual Highlights

- **Inventory KPIs:** Total value, obsolete value, % obsolete, financial cost
- **Gauge:** Visual cue of % inventory obsolescence
- **Bar Charts:** Breakdown by Material Type and Plant
- **Stacked Column:** Evolution over the last 12 months

---

##  Tech Stack

- **Power BI Desktop**
- **DAX** for business logic
- **Power Query** for preprocessing
- **SAP MB51 / MM Extracts** as base data (sanitized)

---

## 👨‍💼 Author

**Vasco Bento**  
Analytics & Supply Chain Optimization  
[LinkedIn →](https://www.linkedin.com/in/vasco--bento)

---

## ⚖️ License

This project is shared for educational and demonstration purposes.  
**No production data is included.**

License: `MIT`
