# sparkavro
Load Avro data into Spark with sparklyr

## Usage

```r
library(sparklyr)
library(sparkavro)
sc <- spark_connect(master = "spark://HOST:PORT")
df <- spark_read_avro(sc, "test_table", "/user/foo/test.avro")

spark_write_avro(df, "/tmp/output")
```

Expamle data are from https://github.com/miguno/avro-cli-examples