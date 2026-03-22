# 📊 Python Sales Data Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Latest-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-11557c?style=for-the-badge&logo=matplotlib&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Dataset Description](#dataset-description)
- [Installation & Setup](#installation--setup)
- [How to Run](#how-to-run)
- [Key Business Questions & Findings](#key-business-questions--findings)
- [Visualizations](#visualizations)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## 📖 About the Project

This project performs an **Exploratory Data Analysis (EDA)** on 12 months of real-world sales data from an electronics store. The goal is to extract actionable business insights by answering key questions around:

- **When** to advertise for maximum impact
- **Where** to focus sales efforts geographically
- **What** products to promote and bundle together
- **How much** revenue each month and city generates

The analysis covers data cleaning, feature engineering, grouping, aggregation, and rich visualizations — all done in Python using Pandas and Matplotlib.

---

## 📁 Project Structure

```
Python-Sales-Data-Analysis/
│
│   README.md                        ← You are here!
│
└───SalesAnalysis/
    │   Sales_Data_Analysis.ipynb    ← Main analysis notebook
    │
    ├───Data/                        ← Raw monthly CSV files
    │       Sales_January_2019.csv
    │       Sales_February_2019.csv
    │       Sales_March_2019.csv
    │       Sales_April_2019.csv
    │       Sales_May_2019.csv
    │       Sales_June_2019.csv
    │       Sales_July_2019.csv
    │       Sales_August_2019.csv
    │       Sales_September_2019.csv
    │       Sales_October_2019.csv
    │       Sales_November_2019.csv
    │       Sales_December_2019.csv
    │
    ├───Misc/
    │       create_data.py           ← Data generation/utility script
    │
    └───Output/
            all_data.csv             ← Merged & cleaned dataset
```

---

## 🛠 Technologies Used

| Tool | Purpose |
|------|---------|
| **Python 3.8+** | Core programming language |
| **Pandas** | Data manipulation & analysis |
| **Matplotlib** | Data visualization & plotting |
| **Jupyter Notebook** | Interactive analysis environment |
| **itertools** | Product pair combination analysis |
| **collections.Counter** | Frequency counting for product pairs |

---

## 📦 Dataset Description

- **Source:** 12 monthly CSV files (January 2019 – December 2019)
- **Total Records:** ~186,850 rows after merging
- **Total Columns:** 6 raw columns

| Column | Description |
|--------|-------------|
| `Order ID` | Unique identifier for each order |
| `Product` | Name of the product sold |
| `Quantity Ordered` | Number of units ordered |
| `Price Each` | Price per unit in USD |
| `Order Date` | Date and time of the order |
| `Purchase Address` | Full delivery address |

### 🔧 Engineered Features

| Feature | Description |
|---------|-------------|
| `Month` | Extracted month number from Order Date |
| `Sales` | Computed as Quantity Ordered × Price Each |
| `City` | Extracted city + state from Purchase Address |
| `Hour` | Extracted hour from Order Date |
| `Minute` | Extracted minute from Order Date |

---

## ⚙️ Installation & Setup

### Prerequisites
Make sure you have the following installed:

```bash
Python 3.8+
pip
Jupyter Notebook or JupyterLab
```

### Clone the Repository

```bash
git clone https://github.com/adityabobade7900/Sales-Data-Analysis-Python.git
cd Python-Sales-Data-Analysis
```

### Install Required Libraries

```bash
pip install pandas matplotlib jupyter
```

---

## ▶️ How to Run

1. **Navigate to the SalesAnalysis folder:**

```bash
cd SalesAnalysis
```

2. **Launch Jupyter Notebook:**

```bash
jupyter notebook
```

3. **Open the notebook:**

```
Sales_Data_Analysis.ipynb
```

4. **Run all cells** — Go to `Kernel` → `Restart & Run All`

> ✅ The notebook will automatically merge all 12 CSV files, clean the data, and generate all visualizations.

---

## 🔍 Key Business Questions & Findings

### ❓ Q1. What was the best month for sales?

| Month | Revenue |
|-------|---------|
| January | $1,822,256 |
| February | $2,202,022 |
| March | $2,807,100 |
| April | $3,390,670 |
| May | $3,152,606 |
| June | $2,577,802 |
| July | $2,647,775 |
| August | $2,244,467 |
| September | $2,097,560 |
| October | $3,736,726 |
| November | $3,199,603 |
| **December** | **$4,613,443** ✅ |

> 🏆 **December was the best month** with over **$4.6 Million** in revenue — driven by holiday season shopping.

---

### ❓ Q2. What city had the highest number of sales?

| City | Revenue |
|------|---------|
| **San Francisco, CA** | **$8,262,203** ✅ |
| Los Angeles, CA | $5,452,570 |
| New York City, NY | $4,664,317 |
| Boston, MA | $3,661,642 |
| Atlanta, GA | $2,795,498 |
| Dallas, TX | $2,767,975 |
| Seattle, WA | $2,747,755 |
| Portland, OR | $1,870,732 |
| Austin, TX | $1,819,581 |
| Portland, ME | $449,758 |

> 🏆 **San Francisco led all cities** with over **$8.2 Million** in total sales.

---

### ❓ Q3. What time should ads be displayed?

> 📢 **Best times to display advertisements:** Around **11 AM** and **7 PM**

These are the peak hours when order volume is highest — just before customers are about to make purchasing decisions.

---

### ❓ Q4. What products are most often sold together?

| Product Pair | Count |
|-------------|-------|
| **iPhone + Lightning Charging Cable** | **2,140** ✅ |
| Google Phone + USB-C Charging Cable | 2,116 |
| iPhone + Wired Headphones | 987 |
| Google Phone + Wired Headphones | 949 |
| iPhone + Apple Airpods Headphones | 799 |
| Vareebadd Phone + USB-C Charging Cable | 773 |

> 🛒 **Bundling phones with their cables** is the most common purchasing pattern — great opportunity for cross-selling!

---

### ❓ Q5. What product sold the most? Why?

| Product | Quantity Ordered |
|---------|-----------------|
| **AAA Batteries (4-pack)** | **31,017** ✅ |
| AA Batteries (4-pack) | 27,635 |
| USB-C Charging Cable | 23,975 |
| Lightning Charging Cable | 23,217 |
| Wired Headphones | 20,557 |

> 💡 **AAA Batteries sold the most** because of their **low price point ($2.99)** — making them an easy, frequent impulse buy compared to premium electronics.

The dual-axis chart clearly shows an **inverse relationship** between price and quantity ordered — cheaper products sell in much higher volumes.

---

## 📊 Visualizations

The notebook generates the following charts:

1. **📅 Monthly Sales Bar Chart** — Revenue per month
2. **🏙️ City Sales Bar Chart** — Revenue per city
3. **⏰ Hourly Order Line Chart** — Order volume by hour of day
4. **📦 Product Quantity Bar Chart** — Units sold per product
5. **💰 Dual-Axis Chart** — Quantity ordered vs Price per product

---

## 🚀 Future Improvements

- [ ] **Revenue by Product** — Identify most profitable products (not just highest quantity)
- [ ] **Weekly Trends** — Which day of the week drives most sales?
- [ ] **City vs Product Heatmap** — Which city buys which product most?
- [ ] **Monthly Growth Rate** — Percentage change in revenue month over month
- [ ] **Interactive Dashboard** — Build using Plotly or Power BI
- [ ] **Predictive Analysis** — Forecast next month's sales using ML models

---

## 👨‍💻 Author

**Aditya Bobade**

[![GitHub](https://img.shields.io/badge/GitHub-adityabobade7900-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/adityabobade7900)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aditya%20Bobade-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adityabobade7900)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit%20Here-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://adityabobade7900.github.io/adityabobade/)

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify and distribute.

---

> ⭐ **If you found this project helpful, please give it a star on GitHub!** ⭐
