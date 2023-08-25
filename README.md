# Home_Sales
Knowledge of SparkSQL to determine key metrics about home sales data. Experiment with Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

(Every question answered in two decimal points.)
Question 1: 
- What is the average price for a four-bedroom house sold for each year?
+--------------------+----------+
|round(avg(price), 2)|year(date)|
+--------------------+----------+
|           296363.88|      2022|
|           301819.44|      2021|
|           298353.78|      2020|
|            300263.7|      2019|
+--------------------+----------+

  
Question 2:
- What is the average price of a home for each year it was built that has three bedrooms and three bathrooms?
+--------------------+----------+
|round(avg(price), 2)|date_built|
+--------------------+----------+
|           292676.79|      2017|
|           290555.07|      2016|
|            288770.3|      2015|
|           290852.27|      2014|
|           295962.27|      2013|
|           293683.19|      2012|
|           291117.47|      2011|
|           292859.62|      2010|
+--------------------+----------+

Question 3:
- What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet?

+--------------------+----------+
|round(avg(price), 2)|date_built|
+--------------------+----------+
|           280317.58|      2017|
|            293965.1|      2016|
|           297609.97|      2015|
|           298264.72|      2014|
|           303676.79|      2013|
|           307539.97|      2012|
|           276553.81|      2011|
|           285010.22|      2010|
+--------------------+----------+


Question 4:
- What is the "view" rating for homes costing more than or equal to $350,000?
+----+--------------------+
|view|round(avg(price), 2)|
+----+--------------------+
|  51|           788128.21|
|  54|           798684.82|
|  69|           750537.94|
|  87|           1072285.2|
|  73|           752861.18|
|  64|           767036.67|
|  59|            791453.0|
|  85|          1056336.74|
|  52|           733780.26|
|  71|            775651.1|
|  98|          1053739.33|
|  99|          1061201.42|
|  96|          1017815.92|
| 100|           1026669.5|
|  70|           695865.58|
|  61|           746877.59|
|  75|          1114042.94|
|  78|          1080649.37|
|  89|          1107839.15|
|  77|          1076205.56|
+----+--------------------+
only showing top 20 rows

--- 0.1758711338043213 seconds ---
