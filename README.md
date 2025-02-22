# **Customer Segmentation Analysis - Data Cleaning Project**

## **Project Overview**  
This project focuses on **cleaning and preparing** the `AB_NYC_2019.csv` dataset using Python in Jupyter Notebook. The goal is to ensure data integrity by handling missing values, removing duplicates, standardizing formats, and detecting outliers for reliable analysis.

---

## **Dataset Information**  
- **Dataset:** `AB_NYC_2019.csv`
- **Source:** Airbnb listings in New York City  
- **Columns:**  
  - `id`: Unique listing ID  
  - `name`: Listing title  
  - `host_id`: Host's unique ID  
  - `host_name`: Name of the host  
  - `neighbourhood_group`: NYC borough (Manhattan, Brooklyn, etc.)  
  - `neighbourhood`: Specific neighborhood  
  - `latitude`, `longitude`: Geolocation  
  - `room_type`: Type of listing (Entire home, Private room, etc.)  
  - `price`: Listing price per night  
  - `minimum_nights`: Minimum required stay  
  - `number_of_reviews`: Count of total reviews  
  - `last_review`: Date of last review  
  - `reviews_per_month`: Average reviews per month  
  - `calculated_host_listings_count`: Total listings per host  
  - `availability_365`: Available days in a year  

---

## **Data Cleaning Process**  

### ✅ **1. Data Integrity Check**  
- Checked column names and data types (`df.info()`, `df.describe()`)  
- Ensured no incorrect or inconsistent values  

### ✅ **2. Handling Missing Values**  
- Identified missing values using `df.isnull().sum()`  
- Filled missing values:  
  - **"reviews_per_month"** → Imputed with median  
  - **"last_review"** → Replaced with a default date  

### ✅ **3. Duplicate Removal**  
- Checked for duplicates (`df.duplicated().sum()`)  
- Removed duplicates (`df.drop_duplicates(inplace=True)`)  

### ✅ **4. Standardization**  
- Converted text columns to lowercase and removed extra spaces (`str.strip().str.lower()`)  
- Ensured consistent formatting for numerical values  

### ✅ **5. Outlier Detection & Handling**  
- Visualized numeric data outliers using boxplots (`plt.boxplot()`)  
- Used **IQR method** to detect and handle extreme values  

---

## **Results & Final Dataset**  
After cleaning, the dataset was saved as:  
```bash
cleaned_AB_NYC_2019.csv
```
**No missing values, no duplicates, and improved data consistency.**  

---

## **How to Use This Project**
### **Prerequisites**
- Install dependencies:  
```bash
pip install pandas numpy matplotlib
```
- Run Jupyter Notebook:  
```bash
jupyter notebook
```
- Load dataset in Python:
```python
import pandas as pd
df = pd.read_csv("cleaned_AB_NYC_2019.csv")
```

---

## **Next Steps**  
- Perform **Exploratory Data Analysis (EDA)**  
- Build **visualizations** for insights  
- Use the cleaned dataset for **machine learning models**  

---

### **Author:** [Namratha K Kadam]  
🚀 **Project Completed Successfully!** 🚀  
