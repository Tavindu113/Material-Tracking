# Overview

MAS Intimates Linea Clothing, Pallekale, Sri-Lanka. operate as 2 facilities. Since Row Material Warehouse (RMW) at one facility, the other facility having  Production Lines. This is a huge barrior to The **RMW End and Material Tracking Application** is a confidential internal system developed to streamline the tracking of materials and finished products across multiple production units in a manufacturing facility. It ensures accountability, traceability, and real-time visibility into material movement throughout the value stream. 

## Purpose

- Eliminate manual data entry and tracking processes
- Enable digital, real-time updates of material flow
- Improve traceability across production stages
- Provide analytics for decision-making using Power BI

## Problem Statement

Previously, material tracking was done through paper logs or Excel files, leading to:
- Delayed updates and manual errors
- Lack of visibility for team leads and managers
- Inconsistent reporting and analysis

## Solution Summary

This application offers a modular web-based interface for each production area (e.g., Poly Bag Shop, Thread Shop, System 261), allowing operators and supervisors to interact with live data using QR/barcode scanning and automated logging.

## Key Features

- Role-based dashboards (Admin, Group Leader, Operator)
- QR/Barcode-based material scanning and validation
- Live status of loading and unloading events
- Power BI dashboard for historical and real-time analytics

## Tech Stack

| Layer        | Technology           |
|--------------|----------------------|
| Frontend     | Power Apps             |
| Backend      | Power Apps    |
| Database     | Dataverse             |
| Analytics    | Microsoft Power BI   |
| Auth & Admin | Dataverse  |
| Deployment   | Microsoft Powerplatform |

## System Architecture
<img width="1536" height="1024" alt="LOading   Unloading" src="https://github.com/user-attachments/assets/4aa44109-f1ff-4865-a385-b542c293dfd6" />



> _Diagram shows how each shop floor interface communicates with the backend server and central database. Power BI connects via a secured data pipeline._

## Stakeholders

- **Production Operators** – Daily interaction for material status
- **Group Leaders** – Monitoring and escalation
- **Admin** – User management and filtering requirements configuration
- **Process Engineers / Management** – Visual insights via Power BI dashboard

## Development Timeline

| Phase                | Description                                  |
|----------------------|----------------------------------------------|
| Phase 1              | Requirements analysis and VSM mapping        |
| Phase 2              | Database design and backend development      |
| Phase 3              | Screen-by-screen UI/UX and functionality     |
| Phase 4              | Testing with limited users                   |
| Phase 5              | Final deployment + Power BI integration      |

---

> _For detailed documentation on each screen or module, refer to the respective markdown files in the `docs/` directory._

<img width="1785" height="2526" alt="Reccomendation from MAS_Page_1" src="https://github.com/user-attachments/assets/35152b87-9ac3-4c94-9a32-b3162277d18e" />
<img width="1785" height="2526" alt="Reccomendation from MAS_Page_2" src="https://github.com/user-attachments/assets/32615932-871a-45ea-b15a-3550cd94b99c" />

