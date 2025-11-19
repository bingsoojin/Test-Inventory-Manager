# TEST-Inventory-Manager
Inventory manager for personal use

A lightweight browser-based inventory manager designed for rapid data entry, barcode/SKU scanning, and smooth editing workflows. All data is stored locally in the browser using `localStorage`, meaning no backend or setup is required.

---

## Core Features

### 1. SKU Lookup & Smart Form Behaviour
- Enter or scan a SKU into the input field and press **Check**.
- If the SKU exists: an **Edit Product** form appears with values prefilled.
- If the SKU does not exist: an **Add Product** form is generated.
- Forms support **Enter-to-advance** between fields for fast scanning workflows.

### 2. Add New Products
Each new product contains:
- SKU  
- Name  
- Description  
- Reference  
- Producer  
- Quantity  
- Expiry (auto-formatted to `YYYY/MM/DD`)  
- Type  
- Status  

Press **Add Product** to save the new item to storage.

### 3. Edit Existing Products
Products can be modified through:
1. Scanning/entering a SKU and editing its details  
2. Clicking the **Edit** button in the table  

The edit form mirrors the Add form, maintaining consistency and speed.

### 4. Cancel Button (All Forms)
A **Cancel** button is included in all Add and Edit forms.  
It:
- Clears the form  
- Returns to the main table view  
- Refocuses the SKU input  

This keeps the interface clean and avoids unfinished entries.

---

## 5. Inventory Table
- Displays all stored inventory items.
- Most recent entries appear at the top.
- Columns show SKU, names, quantities, expiry, type, status + an Edit button.
- Edit button is enlarged for easier access.

---

## 6. Dark Mode (Default + Remembered)
- Dark mode is the default theme.
- When light/dark mode is toggled, the choice is saved into `localStorage`.
- On reload, the app restores the previous theme immediately.

Stored in:
  localStorage["theme"]
  
---

## 7. Import & Export

### Export Options
- **JSON Export:** Creates a JSON backup of the entire inventory.
- **Excel Export:** Generates an `.xlsx` file using the XLSX library.

### Import Options
- Import from **JSON** or **Excel (.xlsx)**.
- Replaces current inventory with imported data.
- JSON import validates structure before applying.

---

## 8. Local Storage
Inventory is stored persistently in:
  localStorage["inventory"]
  localStorage["theme"]
  
Nothing is uploaded or sent externally.

---

## 9. Dependencies
Only one external dependency:
- **XLSX.js** (via CDN) for Excel import/export

The rest of the system is fully self-contained.

---

## 10. Ideal Use Cases
- Medical consumables tracking  
- Warehouse or stockroom supply management  
- Clinic/office consumables  
- Any environment requiring offline, fast, reliable stock entry or barcode scanning  

---
