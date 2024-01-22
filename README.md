## Sales Insights Data Analysis Project

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`
**• Thorough Analysis:** I conducted an exhaustive analysis of the net sales performance, examining data across various dimensions, including year, customer, market, product, growth and division.

**• Target Alignment:** Ensured alignment with the strategic objectives by closely scrutinizing market performance against predefined targets.

**• In-Depth Insights:** Generated comprehensive insights that shed light on critical aspects of sales operations.

![sales_and_finance_analytics_project_using_excel_page-0001](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/fbd2d307-6189-4e3d-9d7d-ef35ec357673)

![sales_and_finance_analytics_project_using_excel_page-0002](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/ad7f7d6a-c5ce-4546-be1c-1c665ef5ecf4)

![sales_and_finance_analytics_project_using_excel_page-0003](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/06f708df-d0df-4cd7-9e36-4aecdb60290b)

![sales_and_finance_analytics_project_using_excel_page-0004](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/ded870c2-6600-4273-942f-6d44a98cf84b)

![sales_and_finance_analytics_project_using_excel_page-0005](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/d1918d5c-44ce-4fae-857f-e6b7f479d6d2)

![sales_and_finance_analytics_project_using_excel_page-0006](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/e073f1e0-9885-4c0f-83d3-6e1c3af550b5)

![sales_and_finance_analytics_project_using_excel_page-0007](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/cc1906f3-0e7a-4727-9205-3fe67a5abaff)

![sales_and_finance_analytics_project_using_excel_page-0008](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/222ec970-4cd1-4268-8e54-0e704b92e9d7)

![sales_and_finance_analytics_project_using_excel_page-0009](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/5f50426b-8342-4d12-9da6-a3536655aaba)

# Finance Analytics
**• Metric Development:** I designed and implemented essential financial metrics such as Net Sales, COGS, Gross Margin and Gross Margin % for the purpose of creating a P&L statement.

**• Decision-Making:** These metrics are responsible for generating valuable insights to perform data-driven decision-making .

![sales_and_finance_analytics_project_using_excel_page-0010](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/546c1798-c54b-4400-b662-e14e7aaa49cc)

![sales_and_finance_analytics_project_using_excel_page-0011](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/1deeeb39-f1f6-4b8b-8d47-7982bdecf80d)

![sales_and_finance_analytics_project_using_excel_page-0012](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/2ac7dd95-39fb-453e-81ea-baff4d7306d5)

![sales_and_finance_analytics_project_using_excel_page-0013](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/fe9e0d86-73b9-4bb3-8221-30825fba0040)

![sales_and_finance_analytics_project_using_excel_page-0014](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/22bbed3f-27fb-4b11-a4f2-00ac2eb0ce68)

![sales_and_finance_analytics_project_using_excel_page-0015](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/3f69dbca-9e55-4c29-870a-2a7ebed47d96)

![sales_and_finance_analytics_project_using_excel_page-0016](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/fa71dd09-5cf3-4630-833b-25a74c7f917a)

![sales_and_finance_analytics_project_using_excel_page-0017](https://github.com/MohdAkif919/Sales-and-Finance-Data-Analytics-Project/assets/58876003/5f82df99-68d2-4bc3-9777-5e87b0bf74d0)


Data Analysis Using Power BI
============================

1. Formula to create norm_amount column

`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`



