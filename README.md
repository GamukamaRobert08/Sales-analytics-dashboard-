
## 📊 Excel Sales Analytics Dashboard

![Excel Dashboard](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Dashboard](https://img.shields.io/badge/Dashboard-Interactive-blue)
![Data Analysis](https://img.shields.io/badge/Data-Analytics-orange)
 ## 🎯 Project Overview
Interactive Excel dashboard for analyzing Q1 2024 sales data, identifying key performance trends, and supporting business decision-making with real-time filtering and visualizations.

## 📥 Download & Quick Start
[Download Excel Dashboard](Sales_analytics_dashboard.xlsx)

1. **Download** the Excel file above
2. **Open** in Microsoft Excel (2013+)
3. **Enable editing** if prompted
4. **Navigate** to Dashboard sheet
5. **Use slicers** to filter data

## ✨ Key Features
- **Interactive Slicers**: Filter by Region, Category, or Customer Tier
- **Dynamic Charts**: Real-time updates with all filters
- **Top 5 Customers**: Always shows highest revenue clients
- **Automated Calculations**: 15+ Excel functions for data cleaning
- **Key Metrics Dashboard**: Total revenue, order counts, averages
- **One-click Data Refresh**: Easy update system

## 📊 Dashboard Preview

### Main Dashboard Interface
![Dashboard View](https://via.placeholder.com/800x400/2E86C1/FFFFFF?text=Sales+Analytics+Dashboard+Preview)

### Interactive Filtering
![Slicers](https://via.placeholder.com/400x300/27AE60/FFFFFF?text=Interactive+Slicers)

## 📁 Project Structure

### Excel Workbook Sheets:
| Sheet Name | Purpose | Key Components |
|------------|---------|----------------|
| **_README** | Documentation | Project overview, data dictionary, user guide |
| **Orders** | Raw transaction data | 30+ sales orders with customer/product details |
| **Products** | Product catalog | 10 products with categories, pricing, margins |
| **Customers** | Customer database | 8 customers with tier levels and locations |
| **Data_Clean** | Master analysis table | Calculated columns, enriched data, formulas |
| **Analysis** | Key metrics | SUMIFS, COUNTIFS, AVERAGEIFS calculations |
| **Dashboard** | Interactive reports | Charts, slicers, Top 5 customers, trends |

### Data Flow:
```

Raw Orders → Data Cleaning → Analysis → Dashboard Visualization

## 📈 Key Metrics & Analysis

### Calculated Metrics:
1. **Total Revenue (Delivered, East)**: `=SUMIFS(tbl_Practice[Revenue],tbl_Practice[Status],"Delivered",tbl_Practice[Region],"East")`
2. **Count of Large Orders (Silver Tier)**: `=COUNTIFS(tbl_Practice[OrderSize],"Large",tbl_Practice[CustomerTier],"Silver")`
3. **Average Discount (Furniture Category)**: `=AVERAGEIFS(tbl_Practice[DiscountValue],tbl_Practice[Category],"Furniture")`

### Data Enrichment (Data_Clean Sheet):
- **Customer Information**: VLOOKUP from Customers table
- **Product Details**: VLOOKUP from Products table
- **Time Intelligence**: Month, Year, Quarter calculations
- **Revenue Calculation**: `Quantity × UnitPrice × (1 - Discount)`
- **Order Size Categorization**: Large (>$500) vs Standard

## 🛠️ How to Use the Dashboard

### 1. Filtering Data
- **Slicers Location**: Right side of Dashboard sheet
- **Filter by**: Region, Category, or Customer Tier
- **Multiple selections**: Use Ctrl+Click
- **Clear filters**: Click "Clear Filter" icon on slicer

### 2. Interpreting Charts
- **Monthly Sales Trend**: Line chart showing revenue over time
- **Revenue by Category**: Bar chart comparing product categories
- **Top 5 Customers**: Table showing highest revenue clients

### 3. Key Metrics Section
- **Top-left section** of Dashboard
- Shows current filtered view totals
- Updates in real-time with slicer selections

## 🔄 Refreshing Data

### Adding New Orders:
1. **Go to** `Data_Clean` sheet
2. **Add new rows** to the table (tbl_Practice)
3. **Ensure formulas** copy down automatically

### Updating Dashboard:
1. **Click** Data tab → Refresh All (or Ctrl+Alt+F5)
2. **All** pivot tables, charts, and metrics update automatically

### Updating Reference Data:
- **New Products**: Add to `Products` sheet
- **New Customers**: Add to `Customers` sheet
- **Formulas** in `Data_Clean` will automatically reference new entries

## 📋 Data Dictionary

### tbl_Practice (Main Analysis Table):
| Column | Description | Sample Value |
|--------|-------------|--------------|
| OrderID | Unique Order Identifier | 1001 |
| Revenue | Calculated: Quantity × UnitPrice × (1 - Discount) | 53.98 |
| OrderSize | Categorized: "Large" if Revenue > $500, else "Standard" | Standard |
| CustomerTier | Customer loyalty level (Gold/Silver/Bronze) | Gold |
| Category | Product category group | Electronics |
| Region | Sales region (North/South/East/West) | East |
| Status | Order status (Delivered/Processing/Cancelled) | Delivered |

### tbl_Products (Product Catalog):
| Column | Description | Sample |
|--------|-------------|--------|
| ProductID | Unique product identifier | P101 |
| ProductName | Product description | Wireless Mouse |
| Category | Product category | Electronics |
| UnitPrice | Selling price | 29.99 |
| Cost | Product cost | 15.00 |
| ProductMargin | Profit margin | 0.4998 |

### tbl_Customers (Customer Database):
| Column | Description | Sample |
|--------|-------------|--------|
| CustomerID | Unique customer identifier | C001 |
| CustomerName | Customer full name | John Smith |
| Tier | Loyalty tier | Gold |
| City/State | Customer location | New York, NY |

## 🚀 Advanced Features

### Excel Functions Used:
- **VLOOKUP**: Customer and product data enrichment
- **SUMIFS/COUNTIFS/AVERAGEIFS**: Conditional calculations
- **TEXT**: Date formatting for month/year extraction
- **IF**: Order size categorization
- **TRIM/PROPER**: Data cleaning and standardization

### Pivot Tables:
- **Monthly Sales Trend**: Summarizes revenue by month
- **Revenue by Category**: Groups sales by product category
- **Connected to slicers** for interactive filtering

### Excel Requirements:
- Microsoft Excel 2013 or later
- Macros enabled (if any)
- Data Analysis ToolPak (not required but helpful)

### Feature Requests:
- Suggest new metrics or visualizations
- Recommend UI/UX improvements
- Propose additional data analyses

## 🙏 Acknowledgments
- Built with Microsoft Excel 2013+
- Inspired by business intelligence best practices
- Special thanks to data analytics community

**⭐ If you find this dashboard useful, please star the repository!**

*Last Updated: $(date)*  
*Dashboard Version: 1.0*  
*Data Period: Q1 2024 (January - March)*  
*Total Records: 30 orders, 8 customers, 10 products*

<div align="center">
  <em>Made with ❤️ and Excel</em><br>
  <sub>Professional Sales Analytics Dashboard</sub>
</div>

