# Database Design

The RMW End and Material Tracking Application uses **Microsoft Dataverse** to manage structured relational data. The schema is centered around three core tables: `Users`, `Pick`, and `Materials`, which are interlinked to ensure traceability, validation, and real-time performance monitoring.

---

## 1. Overview of Tables

| Table Name    | Purpose                                                             |
|---------------|---------------------------------------------------------------------|
| `Users`       | Stores login credentials, roles, and performance metrics            |
| `Pick`        | Contains picklist header information created by the picklist maker  |
| `Materials`   | Contains the list of materials assigned to each picklist            |

---

## 2. Table: `Users`

This table defines system users and their attributes.

| Column Name        | Description                             |
|--------------------|-----------------------------------------|
| `EPF` (PK)         | Unique identifier for the employee      |
| `Name`             | Full name of the user                   |
| `Password`         | Encrypted password                      |
| `Station`          | Shop or station name (e.g., Thread)     |
| `Role`             | User role (Admin, Operator, GL)         |
| `PerformanceMatrix`| Optional performance-related metrics     |

### 🔐 Usage
- Used for login authentication
- Drives role-based screen access
- Tracks material picked per operator via EPF linkage

---

## 3. Table: `Pick` (Picklist Header)

This table holds metadata about each picklist created.

| Column Name       | Description                                     |
|-------------------|-------------------------------------------------|
| `RandomKey` (PK)  | Unique auto-generated primary key               |
| `PicklistID`      | Business ID for tracking picklists              |
| `PO`              | Purchase Order number                           |
| `SO`              | Sales Order number                              |
| `DateCreation`    | Date and time of picklist creation              |
| `DateModified`    | Last updated timestamp                          |

### 🔗 Relationships
- Linked to the `Materials` table via `PicklistID`
- Created by a user in the `Users` table (via EPF mapping)

---

## 4. Table: `Materials` (Picklist Items)

This table stores individual material entries under each picklist.

| Column Name           | Description                                      |
|------------------------|--------------------------------------------------|
| `PicklistID` (FK)      | Foreign key linking to `Pick.PicklistID`         |
| `Material`             | Material type (Thread, Elastic, PolyBag, etc.)   |
| `Qty`                  | Quantity requested                               |
| `SendQty`              | Quantity sent                                    |
| `Balance`              | Remaining quantity (Qty - SendQty)               |
| `Status`               | `Pending` / `Completed`                          |
| `PickingCompletionTime`| Timestamp of when material was completed         |
| `PickerEPF`            | EPF of the operator who picked the material      |

### 🔁 Key Behaviors
- Status changes from "Pending" to "Completed" after picking
- `Balance` is auto-calculated or validated during picking
- Logs completion time and picker EPF for traceability

---

## 5. Data Relationships

