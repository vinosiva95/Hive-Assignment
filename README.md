# Hive-Assignment
assignment number- 1

from table sales_order_data_orc;
hive> set hive.cli.print.header=true;
A. hive> select year_id, sum(sales) as total_sales from sales_order_data_orc group by year_id;

