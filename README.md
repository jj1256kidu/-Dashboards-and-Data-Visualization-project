# 🧾 Sales Dashboard

An interactive dashboard built with **Streamlit** to visualize and analyze sales data with a clean, corporate-themed UI.

## ✨ Features

- 📥 Upload data via Excel file or connect to Google Sheets  
- 🧩 Select **Current Week** and **Previous Week** sheets from dropdowns  
- 🔍 Interactive filters for `Practice`, `Quarter`, and `Hunting/Farming`  
- 📊 Key Performance Indicators (KPIs) and trend visualizations  
- 🧠 Practice-wise sales summary with clean, corporate visuals  
- 📋 Detailed deals table with search and export functionality  
- 💰 All monetary values are standardized in **Lakhs (₹10⁵ units)**  

---
<details>
<summary>📂 <strong>How to Upload Data (Click to expand)</strong></summary>

To ensure the dashboard loads and functions correctly:

1. **Prepare an Excel file** (`.xlsx`) with two sheets:
   - One for **Current Week** data
   - One for **Previous Week** data

2. **Sheet names must be exactly as follows (no extra spaces):**
   - ✅ `Raw_Data`
   - ✅ `PreviousWeek_Raw_Data`  
   - ❌ Avoid names like ` Raw_Data` or `Raw_Data ` (with leading/trailing spaces)

3. **Upload the file** using the dashboard’s file uploader (limit: 200MB per file)

4. **Select the correct sheet names** using the dropdown after upload

> ⚠️ If you're not seeing charts or filters, double-check your sheet names for typos or spaces.

</details>

---

## 💻 Local Setup

# 1. Clone the repository
git clone https://github.com/yourusername/sales-dashboard.git
cd sales-dashboard

# 2. (Optional) Create & activate a virtual environment
python -m venv venv
source venv/bin/activate         # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the dashboard
streamlit run sales_dashboard.py


---

## ☁️ Deploy to Streamlit Cloud

```bash
# Push to GitHub
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/sales-dashboard.git
git push -u origin main
```

Then:

1. Visit [share.streamlit.io](https://share.streamlit.io/)  
2. Sign in with your GitHub account  
3. Click **"New app"** and select:
   - Repository
   - Branch: `main`
   - File: `sales_dashboard.py`  
4. Click **Deploy**

---

## 📑 Data Format Requirements

The Excel file (or Google Sheet) should have:

- Sheet: `Raw_Data`
- Columns:
  - Organization Name  
  - Opportunity Name  
  - Geography  
  - Expected Close Date  
  - Probability  
  - Amount (in Lakhs)  
  - Sales Stage  
  - Practice  
  - Quarter  
  - Hunting/Farming  
  - Sales Owner  
  - Tech Owner  

---

## 🚀 Usage

1. Upload an Excel file or provide a Google Sheet URL  
2. Select both `Raw_Data` and `PreviousWeek_Raw_Data` sheets  
3. Enter your sales target in Lakhs  
4. Use filters to explore the data  
5. View KPIs, summary charts, and deal breakdowns  
6. Export filtered data to CSV if needed  

---

## 📁 Project Structure

```
sales-dashboard/
├── .devcontainer/               # Dev container config
│   └── devcontainer.json
├── .streamlit/                 # Streamlit theme config
│   └── config.toml
├── auth.py                     # User authentication logic (optional)
├── futuristic_login.py        # Custom animated login UI
├── login.html                  # HTML template for login screen
├── particle_config.py          # Particle animation config
├── sales_dashboard.py          # Main Streamlit app
├── views.py                    # Page rendering and UI logic
├── Dummy Data of For Sales Project.xlsx  # Sample data
├── requirements.txt            # Python dependencies
├── README.md                   # Project documentation
└── .gitignore                  # Git ignore file
```

---

## 📝 Notes

- 📊 **Sample Data**: A file named `Dummy Data of For Sales Project.xlsx` is included for demo use.
- 📄 The uploaded Excel sheet **must** have a tab named `Raw_Data`.
- 🌐 Google Sheets must be **publicly accessible** for integration to work.
- 💰 All values are in **Lakhs (₹10⁵ units)**.
- 🧑‍💼 UI follows a clean, corporate-themed layout.
- 📁 Max file upload size: **200MB**.

---
