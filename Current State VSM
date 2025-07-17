# Current State Value Stream Map (VSM)

The current material flow process at the Raw Material Warehouse (RMW) supports 115 production lines and is primarily coordinated through SAP, Excel, and physical handling systems like AGVs. The following Value Stream Map (VSM) illustrates the end-to-end flow from supplier receipt to material unloading at production lines.

---

## 📌 Context & Role of RMW

The **Raw Material Warehouse (RMW)** is responsible for supplying production lines with essential materials such as thread, lace, polybags, stickers, and elastics. A **kanban-based pull system** is in place where production lines initiate a request through an e-kanban system. The key constraints and flow include:

- **Kanban Request Timing**: Must be sent at least **4 hours in advance**
- **RMW SLA**: Must deliver materials within **2 hours**
- **Material Limiting**: To prevent overstocking, only the requested quantity is issued
- **Data Tools**: SAP (for request/picklist creation), Excel (Trims Kanban), and AGVs

---

## 🔄 End-to-End Process Description

1. **e-Kanban Request**: Line team leader raises a request in advance.
2. **Picklist Creation**: An RMW officer generates a picklist via SAP.
3. **Trims Kanban Update**: Excel file is updated per shop.
4. **Shop Floor Picking**:
   - Each shop (Label, Polybag, Elastic, Lace, TRD) gathers items.
   - Materials are loaded onto the **AGV** by shop operators.
5. **AGV Delivery**:
   - AGV collects items from each shop.
   - Finishes route at **System 261 station**.
6. **System 261**:
   - Materials are scanned and deducted from SAP.
7. **Final Transfer**: Materials are sent to the production line.

---

## 📋 Key Roles

| Role             | Responsibility                            |
|------------------|--------------------------------------------|
| Production TL    | Send e-Kanban request                      |
| RMW Officer      | SAP Picklist creation                      |
| Shop Pickers     | Pick and load materials                    |
| AGV Driver       | Automated collection across shops          |
| 261 Operators    | SAP entry and final material issue         |

---

## 🔍 Pain Points

- ⏳ Delay due to manual SAP entries and Excel updates
- 📉 No real-time tracking of AGV or picklist status
- 🧾 Error-prone due to dependence on paper/GIS slips
- 🔄 Multiple software systems (SAP + Excel) = duplication

---

## 🧭 Current State VSM Diagram

![Current State VSM](../screenshots/current-vsm.png)

> _This visual maps the full process from material receipt to unloading at the production line. It includes key systems (SAP, Excel), stakeholders, delays, and data flows._

---

## 📉 Limitations Identified

| Problem Area        | Description                                             |
|---------------------|---------------------------------------------------------|
| **Process Delays**  | SAP entry takes time; pickers sometimes wait on updates |
| **Data Sync Gaps**  | Excel not auto-synced with SAP or shops                 |
| **AGV Efficiency**  | Cannot track live status or optimize its routes         |
| **Reporting**       | No centralized dashboard for status visibility          |

---

## 🧩 Why Digitization Was Needed

To reduce the friction between planning and execution, a centralized and modular tracking system was needed that:
- Unified data entry and retrieval (no duplication)
- Provided real-time material tracking (shop to shop, and AGV flow)
- Integrated with SAP while being user-friendly for shop-floor staff
- Automated dashboards for management (via Power BI)

---

> ✅ Next: [Filtering Requirements](./filtering-requirements.md) – How the system ensures only relevant and verified data is processed and displayed.
