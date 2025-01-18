
# Chocolate Sales Analysis in Power BI

This project demonstrates an in-depth analysis of chocolate sales using **Power BI**, with a focus on using DAX functions for dynamic insights. The project incorporates the ACMBU methodology to ensure a structured and efficient data analysis process.



## 📂 Project Overview

The goal of this project is to analyze chocolate sales performance and derive actionable insights by leveraging Power BI's advanced analytics capabilities. The dataset provides detailed information about shipments, products, regions, and calendars. 

This repository contains:
1. The Power BI file: `DAX practice.pbix`
2. The source dataset: `sample-chocolate-sales-data-all.xlsx`



## 🛠 ACMBU Framework Explained

### 1. **A - Acquire Business Knowledge**
   - Understanding the context and business requirements is essential. For this project:
     - **Key Questions**:
       - Which regions generate the highest sales?
       - What is the sales performance by product category?
       - How do sales trends vary over time?
     - **Stakeholder Focus**: Sales managers and regional heads.

### 2. **C - Clean Data**
   - **Data Cleaning Steps**:
     - Removed unnecessary columns.
     - Formatted dates and ensured proper data types.
     - Addressed missing values in the "Shipments" and "Dimension Data" sheets.

### 3. **M - Model for Needs**
   - **Data Modeling**:
     - Relationships between tables (fact and dimension tables) were established in Power BI.
     - Dimension tables include:
       - `Dimension Data`: Contains product and geographic details.
       - `Calendar`: Provides a comprehensive date table.
     - The fact table is:
       - `Shipments`: Records details of all shipments, including sales amount, order status, and product information.

### 4. **B - Blocks Not Black Box**
   - **Transparent Workflows**:
     - Created calculated columns and measures for easy traceability.
     - Used meaningful naming conventions for all DAX measures and columns.

### 5. **U - Use Variables and DAX Query View**
   - **Optimized DAX Queries**:
     - Variables (`VAR`) were used to simplify calculations and improve readability.
     - Measures were written with a focus on reusability and clarity.



## 📊 Dataset Description

### 1. **Shipments Sheet**
- **Fields**:
  - `ShipmentID`: Unique identifier for each shipment.
  - `SPID`, `PID`, `GID`: Codes for salespersons, products, and regions.
  - `Shipdate`: Shipment date.
  - `Amount`: Total sales amount.
  - `Boxes`: Number of boxes shipped.
  - `Order_Status`: Status of the order (e.g., Delivered, Pending).
- **Insights**:
  - Track shipment performance by region and salesperson.
  - Analyze sales trends over time.

### 2. **Dimension Data Sheet**
- **Fields**:
  - Product details: Name, category, cost per box.
  - Geographic details: Region, geo codes, sales team.
  - Images: Links to salesperson pictures.
- **Insights**:
  - Understand product performance by category and region.

### 3. **Calendar Sheet**
- **Fields**:
  - `cal_date`: Calendar dates.
  - `month_name`, `year`: Grouping for temporal analysis.
  - `weekday_name`: Days of the week for weekday-based insights.
- **Insights**:
  - Temporal trend analysis by year, month, or weekday.



## 🔢 Key DAX Measures

### **Sales Rating**
Categorizes performance based on sales amount:
- ⭐⭐⭐: > 2.5 million
- ⭐⭐: > 2.25 million
- ⭐: > 2 million
- 🔴 Red Light: < 2 million

**DAX Code**:
DAX
Sales Rating = SWITCH(
    TRUE(),
    SUM(Sales[SalesAmount]) > 2500000, "⭐⭐⭐",
    SUM(Sales[SalesAmount]) > 2250000, "⭐⭐",
    SUM(Sales[SalesAmount]) > 2000000, "⭐",
    "🔴 Red Light"
)


## 📈 Visualizations and Insights

### 1. Regional Sales Analysis
- **Chart Type**: Map visualization.
- **Insights**: Identify high-performing regions and compare across categories.

### 2. Sales Trend Analysis
- **Chart Type**: Line chart with filters for year and month.
- **Insights**: Seasonal trends and overall growth.

### 3. Product Category Performance
- **Chart Type**: Bar chart with slicers for regions.
- **Insights**: Performance comparison across product categories.



## 📂 File Structure
.
├── DAX practice.pbix          # Power BI file with analysis
├── sample-chocolate-sales-data-all.xlsx  # Source dataset
├── README.md                  # Documentation



## 🤝 Contributing
Contributions are welcome! If you have suggestions or want to collaborate, please open an issue or submit a pull request.



## 🧾 License
This project is open-sourced under the MIT License.


## 📬 Contact
If you have any questions or feedback, feel free to reach out!


Would you like any adjustments or additional details?
