# Hive-Assignment
assignment number- 1

from table sales_order_data_orc;

hive> set hive.cli.print.header=true;
A. hive> select year_id, sum(sales) as total_sales from sales_order_data_orc group by year_id;
Result
year_id	total_sales
2003	3514108.547241211
2004	4724162.593383789
2005	1791486.7086791992
![Scs 22-2610-1](https://user-images.githubusercontent.com/115145715/198038189-8442cc36-b72d-46b3-be44-782a1ab63a03.jpg)
Time taken: 69.183 seconds, Fetched: 3 row(s)

B. hive> select productline, max(sales) as maximum_sales from sales_order_data_orc group by productline;
Result
productline	maximum_sales
Classic Cars	12001.0
Motorcycles	11886.6
Planes	10066.6
Ships	6960.48
Trains	8977.05
Trucks and Buses	8844.12
Vintage Cars	14082.8
![image](https://user-images.githubusercontent.com/115145715/198043740-7fb15fad-e7f4-4420-bc5a-e0899caaa24b.png)

c. hive> select sales, min(sales) as Minimum_sales, otr_id as Quarter from sales_order_data_orc group by sales, otr_id order by Otr_id limit 1;
Result
![image](https://user-images.githubusercontent.com/115145715/198054624-f7c55d98-2293-4139-afda-e4dbe2c17091.png)

D.hive> select s1.country as Country_on_maximum_sale from sales_order_data_orc s1 where s1.sales in (select max(s2.sales) from sales_order_data_orc s2);
Result
![image](https://user-images.githubusercontent.com/115145715/198056908-15004436-de4e-47e0-bbfa-6b80d90b6815.png)

D.2.hive> select s1.country as Country_on_minimum_sale from sales_order_data_orc s1 where s1.sales in (select min(s2.sales) from sales_order_data_orc s2);
Result
![image](https://user-images.githubusercontent.com/115145715/198058115-cc4c3464-e6cf-4b8f-b5e0-43cd3ae0fbc6.png)

E.


