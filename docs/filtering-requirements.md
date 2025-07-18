# Filtering Requirements

To ensure that only accurate, relevant, and authorized data is processed and displayed in the RMW End and Material Tracking Application, several filtering rules and validation criteria were established across different modules.

---

## 1. Purpose of Filtering

The filtering system was designed to:

- ✅ Prevent invalid or outdated data from being used in material tracking
- ✅ Ensure that users only see what is relevant to their role/shop/module
- ✅ Improve response time by avoiding large, unfiltered datasets
- ✅ Align data handling with SAP and shop-floor practices

---

## 2. Key Filtering Dimensions

| Filter Category      | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Date & Time**      | Filter by current date, picklist issue time, or shift                       |
| **Shop Location**    | Only display materials relevant to the selected shop (Poly Bag, Thread, etc.) |
| **Material Type**    | Segregate by item type (Thread, Elastic, Sticker, etc.)                      |
| **Module ID**        | Filter data specific to the production module (e.g., Line 261, Line 302)     |
| **Picklist Status**  | Show only `Pending`, `In Progress`, or `Completed` picklists                 |
| **User Role**        | Group Leaders, Admins, and Operators see different filtered views            |

---

## 3. Frontend Filtering Rules

- Dropdown filters for:
  - Material category
  - Date range
  - Module/line
- Auto-refreshing tables based on filter selections
- Search by barcode or item code
- Table pagination for large datasets

```js
// Example: Client-side filter
const filteredData = data.filter(item =>
  item.shop === selectedShop &&
  item.status !== "Completed" &&
  item.date === today
);
