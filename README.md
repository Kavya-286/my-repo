# Dynamic Data Table Manager

A dynamic and customizable data table application built using **Next.js**, **Redux Toolkit**, and **Material UI (MUI)**.  
This project allows users to manage table data with features like sorting, searching, pagination, dynamic column visibility, and CSV import/export.

---

## 🚀 Features

### ✅ Core Features
- Display table with default fields: **Name, Email, Age, Role**
- **Sorting** on each column (ASC/DESC toggle)
- **Global search** across all fields
- **Client-side pagination** (10 rows per page)

### 🧩 Dynamic Columns
- “Manage Columns” modal to:
  - Add new fields dynamically (e.g., Department, Location)
  - Show / hide existing columns via checkboxes
- Column visibility is **persisted** using localStorage / Redux Persist

### 📥 CSV Import & 📤 Export
- Import CSV using **PapaParse**
- Validate format and show error feedback
- Export current table view as `.csv`
- Only visible columns are included in the export

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Next.js 14** | React framework & routing |
| **Redux Toolkit** | State management |
| **Material UI (MUI)** | UI components |
| **TypeScript** | Static typing |
| **React Hook Form** | Form handling |
| **PapaParse** | CSV import |
| **FileSaver.js / Blob** | CSV export |
| **localStorage / Redux Persist** | Saving preferences |

---

## 📦 Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/your-username/dynamic-data-table-manager.git
cd dynamic-data-table-manager
