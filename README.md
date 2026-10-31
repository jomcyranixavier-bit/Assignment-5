Calculated Columns:
Select Table tools then add new column
Category Type = 'Order Details (3)'[Category] & " " & 'Order Details (3)'[Sub-Category]
Revenue per Order = 'Order Details (3)'[Amount]*'Order Details (3)'[Quantity]
Sales Category = IF('Order Details (3)'[Amount] >= AVERAGE('Order Details (3)'[Amount]), "Above Average" , "Below Average")

Calculated Measures:

DAX Formula:
Order Count = DISTINCTCOUNT('Order Details (3)'[Order ID])
Average Profit in Delhi = CALCULATE(AVERAGE('Order Details (3)'[Profit]), 'List of Orders (4)'[State] = "Delhi")
YTD Sales = TOTALYTD([Total sales],calender[Date])
