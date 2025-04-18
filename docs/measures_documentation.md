
### Measures Table:

| Measure Name      | Measure Function                                                       | DAX Formula                                                                                                   |
|-------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Avg Customer Age  | Calculates the average age of customers (buyers) in the dataset.         | `AVERAGE(Data[Buyer Age])`                                                                                    |
| Avg Shipping Charges | Calculates the average shipping charges for all orders.                 | `AVERAGE(Data[Shipping Charges])`                                                                             |
| Total Shipping Charges | Calculates the total shipping charges across all orders.               | `SUM(Data[Shipping Charges])`                                                                                 |
| Avg Rating        | Calculates the average rating provided by customers.                    | `AVERAGE(Data[Rating])`                                                                                       |
| Order Count       | Counts the total number of orders in the dataset.                       | `COUNT(Data[Order ID])`                                                                                       |
| Quantity Sold     | Calculates the total quantity of products sold in all orders.           | `SUM(Data[Quantity])`                                                                                         |
| Revenue (USD)     | Calculates the total revenue generated from all sales.                   | `SUM(Data[Total Sales])`                                                                                      |
| Avg Order Value   | Calculates the average order value by dividing revenue by the number of orders. | `[Revenue (USD)] / [Order Count]`                                                                               |
| MoM%              | Calculates the Month-over-Month percentage change for a given KPI.      | `VAR CurrentValue = [KPI_Measure]  VAR PreviousMonthValue = CALCULATE([KPI_Measure], DATEADD('DateTable'[Date], -1, MONTH)) RETURN IF(NOT ISBLANK(PreviousMonthValue), DIVIDE(CurrentValue - PreviousMonthValue, PreviousMonthValue, 0), BLANK())` |

