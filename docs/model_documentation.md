## 🧩 Data Model Documentation

The data model used in the **Merchandise Sales Analysis** project is structured to support a wide range of insights related to product sales, customer demographics, shipping methods, and sentiment analysis. The model connects multiple data sources to enable efficient slicing and dicing of the data.

### 🔢 Fact Table
- **Data**:  
  This is the central fact table that holds all transactional-level data related to merchandise sales, including order details, customer demographics, shipping data, and reviews.

### 📐 Dimension Tables & Relationships

| Dimension Table     | Connected Table | Join Column              | Description                                                                 |
|---------------------|------------------|---------------------------|-----------------------------------------------------------------------------|
| Product Table        | Data             | `Product ID`              | Contains metadata like product name and product image for each item sold.   |
| DateTable            | Data             | `Date`                    | Standard date table to enable time-based analysis such as trends and comparisons. |
| Sentiment_Table      | Data             | `Review`                  | Maps customer reviews to their corresponding sentiment classification (e.g., Positive, Neutral, Negative). |
| Countries Table      | Data             | `Order Location`          | Maps order locations to their respective countries and national flags.      |
| KPI Table            | Icon_Table       | `KPI`                     | Supports visual enhancement of KPIs by mapping them to iconography.         |

> 🔁 All relationships are one-to-many from the dimension tables to the `Data` fact table, ensuring efficient filtering and contextual analysis in Power BI.

### Data Model Screenshot

![Merchandise Sales Data Model](https://github.com/Chakradhar-M/Merchandise-Sales-Analysis-01-25/blob/main/resources/Merchandise_Data_Model.png?raw=true)
