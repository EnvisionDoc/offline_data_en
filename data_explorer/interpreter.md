# Supported interpreters

## `%hive`

The following example shows how to use SQL to query a table of raw data.

```sql
%hive
select * from bank limit 10;
```

Click |run_note| to run the paragraph of code, and you'll get results similar to what's shown as follows.

.. image:: media/data_explorer_pic_3.png

## `%livy.spark`

The following example shows how to read file `bank.csv` and count the number of rows.

```
%livy.spark
val bank = sc.textFile("/user/data_explore_product_db/spark/input/bank.csv")
bank.count
```

.. image:: media/data_explorer_pic_4.png

## `%livy.pyspark`

The following samples code reads the table file `bank.csv` and count the number of rows excluding the first row, and displays the first ten rows of data.

```python
%livy.pyspark
from pyspark import SparkContext
from pyspark.sql import SQLContext
spark = SparkSession \
    .builder \
    .appName("PySparkTest") \
    .getOrCreate()
sc = spark.sparkContext
sc.setLogLevel("INFO")

sqlContext = SQLContext(sc)
df=sqlContext.read.format('com.databricks.spark.csv').options(header='true', inferschema='true').load("/user/data_explore_product_db/pyspark/input/bank.csv")

print df.count()
df.show(10)
```

.. image:: media/data_explorer_pic_5.png

## `%md`

The following example shows a markdown sample:

```markdown
%md
# hello world
- **hello world**
```

.. image:: media/data_explorer_pic_6.png

## `%mysql_report`

The following example shows how to retrive data from the database of EnOS Data Report:

```sql
%mysql_report
select * from bank limit 10;
```

.. image:: media/data_explorer_pic_7.png

The following example shows how to retrieve data with a more complex SQL query:

```sql
%mysql_report
select ${group_by}, count(1)as count, avg(balance)as balance_avg
from bank
where marital="${marital=single,single|divorced|married}" and age < ${maxAge=50}
group by ${group_by=education,education|job|age|marital};
```

.. image:: media/data_explorer_pic_8.png

## `%python`

The following example shows the foundational operation of python, that is to mark two coordinate points.

```python
%python
import matplotlib.pyplot as plt
z.configure_mpl(width=400, height=300, fmt='svg')
plt.plot([1,2,3,4], [1,4,9,16], 'ro')
```

.. image:: media/data_explorer_pic_9.png

## `%sh`

The following example shows the foundational operation of shell.

```
%sh
whoami
hadoop fs -ls /user
```

.. image:: media/data_explorer_pic_10.png

.. |run_note| image:: media/run_note.png

<!--end-->
