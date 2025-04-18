
## 🔄 Power Query Transformations

This project analyzes the merchandise sales of influencer **Lee Chatmen**, focusing on key business questions such as product performance, customer demographics, and purchasing behavior. Data preparation was conducted in Power Query to ensure clean and analysis-ready tables.

### 🧾 Fact Table: `Data`
This is the primary transactional table containing individual sales records.

#### ✅ Transformations Applied:
- **Imported from Excel** using `Excel.Workbook` and selected the relevant sheet.
- **Promoted Headers** for proper column naming.
- **Changed Data Types** for appropriate formatting (e.g., dates, numbers, text).
- **Renamed "Order Date" ➝ "Date"** for simplicity.
- **Replaced Values** in `International Shipping`:
  - `"No"` ➝ `"International"`
  - `"Yes"` ➝ `"Domestic"`
- **Renamed Column**:
  - `"International Shipping"` ➝ `"Shipping Method"`

---

### 🌍 Dimension Table: `Countries_Table`
Maps order locations to country names and flag icons for visualization purposes.

#### ✅ Transformations Applied:
- **Imported from CSV** with proper encoding and delimiter setup.
- **Promoted Headers** for meaningful column names.
- **Changed Data Types** for all columns.
  - `Order Location`, `Country`, and `Flag` set as text types.

---

### 💬 Dimension Table: `Sentiment_Table`
Assigns sentiment categories (e.g., Positive, Neutral, Negative) to customer review texts.

#### ✅ Transformations Applied:
- **Imported from CSV** with 2 columns: `Review` and `Sentiment`.
- **Promoted Headers**.
- **Changed Data Types**:
  - `Review`: Text
  - `Sentiment`: Text

---

### 🛍️ Dimension Table: `Product_Table`
Provides product-level metadata including product names and image URLs.

#### ✅ Transformations Applied:
- **Imported from CSV** with 3 columns.
- **Promoted Headers**.
- **Changed Data Types**:
  - `Product ID`, `Product Name`, and `Image` set as text.

---

### 📌 Supporting Table: `Icon_Table`
Contains color-coded KPI indicators used for report visuals.

#### ✅ Transformations Applied:
- **Created using JSON + Binary decode logic** for embedded custom visuals(Created in Power BI using `Enter Data`).
- **Converted to table** with columns: `KPI`, `Grey`, and `Blue`.

---

### 📊 Supporting Table: `KPI_Table`
Used for organizing KPIs on the dashboard with display order.

#### ✅ Transformations Applied:
- **Created via embedded JSON decompression**(Created in Power BI using `Enter Data`).
- **Changed Data Types**:
  - `KPI`: Text
  - `Index`: Whole Number
- **Replaced Text**:
  - `"Avg Order Value (AOV)"` ➝ `"Avg Order Value"` in the `KPI` column.

---
