# User Interfaces

This document provides a comprehensive overview of all user-facing interfaces in the RMW End and Material Tracking Application. Each section corresponds to a functional screen tailored to a specific user role or shop.

---

## 1. Picklist Screen

**Role:** Picklist Maker  
**Purpose:** Create picklists based on kanban requests received from the production floor.

### Features:
- Auto-generated `Picklist ID`
- Input fields for PO, SO, creation date
- Add materials (Thread, Polybag, etc.)
- Save & modify existing picklists



---

## 2. Poly Bag Shop Screen

**Role:** Operator – Poly Bag  
**Purpose:** View picklists that require polybags and update picking status.

### Features:
- Filter by date/module
- Show only relevant items
- Mark quantity picked
- Submit completion



---

## 3. Elastic Shop Screen

**Role:** Operator – Elastic  
**Purpose:** Similar to Poly Bag, dedicated to elastic material updates.



---

## 4. Thread Shop Screen

**Role:** Operator – Thread  
**Purpose:** Real-time picking interface for thread materials.



---

## 5. System 261 Screen

**Role:** Station 261 Operator  
**Purpose:** Final confirmation of picklist before SAP deduction.

### Features:
- Scan and confirm materials
- Update final picklist status
- Log delivery timestamp



---

## 6. Group Leader Screen

**Role:** Group Leader  
**Purpose:** Monitor daily progress, view operator status, approve exceptions.

### Features:
- View materials picked per operator
- See delays or pending items
- Override/mark picklist manually if needed



---

## 7. Admin Screen

**Role:** Admin  
**Purpose:** Manage users, assign stations, reset passwords.

### Features:
- Add/remove users
- Set shop/station per user
- View full logs



---

## 8. Loading Screen

**Role:** Loading Station Operator  
**Purpose:** Mark materials as "loaded to AGV" after shop pickup.

### Features:
- View shop completion
- Confirm material loaded



---

## 9. Unloading Screen

**Role:** Unloading Operator  
**Purpose:** Confirm AGV delivery to System 261 or production modules.



---

## 10. Power BI Dashboard

**Role:** Management / Engineers  
**Purpose:** Visual analytics based on picklists, time delays, picker performance.

### Features:
- Daily/weekly picklist volume
- Shop performance and delays
- Material completion rates by module



---

## Notes

- Screens are role-based and hidden if user permissions do not apply.
- Screens refresh dynamically based on picklist and station filters.
- Picking data auto-syncs to the `Materials` table in Dataverse.

---

> 🔜 See: [Power BI Dashboard](./powerbi-dashboard.md) for a deeper dive into analytical reports and KPIs.
