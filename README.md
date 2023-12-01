# sparksql

Sample code

source_link = "https://raw.githubusercontent.com/quazimoinuddin/sample_db_with_notebooks/main/movies_metadata.csv"

dbfs_path = "/dbfs/data/movies_metadata.csv"

dbutils.fs.cp(source_link, dbfs_path)

data = spark.read.option("header", True).csv("/dbfs/data/movies_metadata.csv")
