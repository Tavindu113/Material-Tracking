# Power BI Dashboard

The Power BI dashboard provides real-time visual insights into the RMW end and material tracking process. It is directly connected to the Microsoft Dataverse tables (`Pick`, `Materials`, `Users`) and refreshes automatically to reflect the current operational status across all production shops.

---

## 1. Purpose

The dashboard is designed to:

- 📊 Monitor daily picklist activity and fulfillment
- ⏱️ Identify material flow delays
- 📈 Track picker and shop-level performance
- 📍 Help supervisors and management make data-driven decisions

---

## 2. Connected Tables

- `Pick` – Header data for each picklist
- `Materials` – Material-level tracking including quantity, status, picker
- `Users` – Roles and stations for filtering picker performance

---

## 3. Key Metrics (KPIs)

| Metric                        | Description                                                  |
|-------------------------------|--------------------------------------------------------------|
| 📦 **Total Picklists**       | Number of picklists created in selected time period          |
| ✅ **Completed Picklists**   | Number and % of picklists fully completed                    |
| 🔄 **In-Progress Picklists** | Picklists with one or more materials still pending           |
| ⏳ **Avg. Picking Time**     | Average duration from picklist creation to material completion |
| 🧑‍🔧 **Top Pickers**         | Ranked list of pickers by quantity or speed                  |
| 🏭 **Shop Completion Rate**  | Status % by shop: Poly Bag, Thread, Elastic, etc.            |
| ⚠️ **Delayed Picklists**     | Picklists exceeding SLA (e.g., >2 hrs open)                  |

---

## 4. Visual Components

| Visual                       | Description                                                  |
|------------------------------|--------------------------------------------------------------|
| ⌛ Timeline Chart             | Picklist creation vs completion over time                    |
| 📍 Pie/Donut Chart           | Status distribution (Pending / Completed / In Progress)      |
| 📊 Bar Chart                 | Material picked per shop                                     |
| 🧑‍💼 Stacked Bar             | Performance by operator (EPF vs Qty vs Time)                 |
| 🏗️ Module Heatmap           | Module-wise picklist frequency                               |
| 📅 Date Filter Slicer        | Filter metrics by specific date range                        |
| 🧩 Shop Filter Slicer        | Select shop-specific views (e.g., Thread only)               |

---

## 5. Sample Screenshot



> _The image above shows real-time insights across picklists, materials, and operator-level performance._

---

## 6. Refresh Strategy

- Data refresh is scheduled **every 5–15 minutes**
- Dashboard supports **on-demand refresh** for team leads
- Connected directly to Dataverse using Power BI connector

---

## 7. Usage by Role

| Role             | Usage                                                                 |
|------------------|------------------------------------------------------------------------|
| **Admin**        | View all picklists, shops, and users                                   |
| **Group Leader** | Monitor pickers in their assigned shop                                 |
| **Management**   | Analyze performance trends and bottlenecks across all modules          |

---

## 8. Export & Sharing

- Reports can be exported as **PDF** or **Excel**
- Shared via Microsoft Teams and Email with scheduled snapshots
- Drill-through enabled to view picklist → materials → picker trace

---

> 🔚 End of dashboard documentation.  
> 🔙 Back to: [User Interfaces](./user-interfaces.md)
