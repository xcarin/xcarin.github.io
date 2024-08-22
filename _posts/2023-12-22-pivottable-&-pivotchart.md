---
layout: post
---
![chocolate](https://github.com/user-attachments/assets/abc36cbf-0fc5-4772-bab4-a549a111bb1b)

> Problem

- Large amount of 300 mock records of chocolate sales data in different countries.

> Solution

- To identify top chocolate sales in different countries using advanced excel.

> Advanced Excel

- PivotTable & PivotChart
- Slicer to filter data

<br/>
<br/>

# Data Analysis using Excel Table, PivotTable & PivotChart

The dataset consists of 300 records of chocolate sales data in different countries which include sales person, geography (country), product sold, sales amount, units sold, cost per unit, total cost, profit earned and profit percentage.

## Basic Statistical
Excel can use to perform basic statistical functions, a few of the commonly used example functions will be discussed below:

(a) COUNTA(value1, [value2], …)

<b>Quantity of chocolate products sold</b>
- Select the product column
- This formula is used to count any type of values, including numeric, text, blank or error values.

      =COUNTA(E2:E301)
      =300
    
(b) STDEV(number1, [number2], …)

<b>Standard deviation of chocolate products sold</b>

- Select the product column

      =STDEV(E2:E301)
      =118.0994989

(c) SUM(number1, [number2], …)

- Total amount of chocolate products sold
- Select the amount column

      =SUM(D2:D301)
      =$1,240,869

(d) AVERAGE(number1, [number2], …)

<b>Average (mean) chocolate products sold</b>

      =AVERAGE(D2:D301)
      =$4,136

(e) MEDIAN(number1, [number2], …)

<b>Median chocolate products sold</b>

     =MEDIAN(D2:D301)
     =$3,437

<br/>
<br/>

## EDA using Excel Table
<b>Find the top three products</b>

There are a few conditional formatting methods which can apply to find the answer, however one of the methods will be discussed as explained below:

- Select amount column > Conditional Formatting > Top/Bottom Rules > Top 10 Items

> Top three products

![1 1](https://github.com/user-attachments/assets/abf10f2c-b12a-4522-b827-cdcb228cfe60)

The same sales person named "Gigi Bowling" has sold Mint Chip Choco and Orange Choco with the highest amount in Canada and India.

<b>Find the duplicate values in any of the products</b>

- Select units column > Conditional Formatting > Highlight Cells Rules > Duplicate Values

There are a total of 251 red highlighted duplicate values found in same or different chocolate products.

![1 2](https://github.com/user-attachments/assets/93953349-d31e-4d26-b103-d7071f8c53ee)

## Interactive Dashboard using PivotTable & PivotChart

Below are the steps & questions:

1. Understand the data

Before applying PivotTable, select the specific column, filter and highlight the result to find the average, sum and count at the bottom of the spreadsheet.

> Random select 3 countries before applying PivotTable

![1 3](https://github.com/user-attachments/assets/ce17f1b5-f796-4d81-a74f-69cdde4971b3)

2. PivotTable

- Select the table > Insert PivotTable > Select either new or existing worksheet > Ok

![1 4](https://github.com/user-attachments/assets/91b1b250-4046-41cc-adf4-3c11603fe31c)

3. PivotTable fields

- Drag the field name into either filters, columns, rows or values.

> 1PivotTable field

![1 5](https://github.com/user-attachments/assets/413a71d6-1b30-4da6-a432-860a38f23762)

> PivotTable values

![1 6](https://github.com/user-attachments/assets/440f59b6-ac43-400e-8ba2-0afb59094e16)

PivotTable values are same as the before applying PivotTable values.

4. PivotChart

- Select the PivotTable and insert PivotChart
- Select the PivotChart > Design > Add Chart Element to add axis title and edit axes, etc.
- Select the PivotChart and add data labels

<b>Which country has generated highest chocolate sales?</b>

The PivotTable shows the total number of sales in six different countries. From the PivotTable, it can be seen that India generated the highest chocolate sales of $252 469.

![1 7](https://github.com/user-attachments/assets/fb039ba3-3070-46db-90a8-56684597c76c)

<b>Who is the top chocolate sales person?</b>

The top three sales persons are Ches Bonnell, Gigi bohling and Ram Mahesh. However, Gigi bohling earned the most amount of $165 725 and profit of $131 191 as compared with others.

![1 8](https://github.com/user-attachments/assets/89be28bc-d224-4b1f-8d8b-90206f3aa809)

<b>Which chocolate is the most popular?</b>

There are 3207 Caramel Stuffed Bars sold and generated $72 373. It can be observed that Caramel Stuffed Bar with the top sales amount is the most popular chocolates among the six countries.

![1 9](https://github.com/user-attachments/assets/f4cad968-4a3d-4981-bc16-25a3aad732e7)

![2 0](https://github.com/user-attachments/assets/24cf31aa-5111-4ebc-a5a5-9ed0efebdcdb)

5. Slicer

- A slicer is a control button that is used to filter an Excel Table or Pivot Table over large amount of data.
- In the dashboard view, select a PivotChart and go to insert slicer to choose the number of slicers.
- To create an interactive effect with slicer, select a slicer and click on report connections. Select the PivotTables and PivotChart to connect the filter. With multiple connections, the data can be automatically selected from only one filter option (slicer).

![2 1](https://github.com/user-attachments/assets/828661d9-6e99-429f-93c8-d3dd2dcf0b82)

6. Dashboard

![2 3](https://github.com/user-attachments/assets/7087735f-0cdd-492f-9458-b9a2f4abeda5)

![2 2](https://github.com/user-attachments/assets/69abbc7e-0ac3-4f73-9305-aac5f11d541a)