---
title: Table functions supported in Aiven for ClickHouse®
sidebar_label: Table functions
---

[Table
functions](https://clickhouse.com/docs/en/sql-reference/table-functions)
can be used to construct tables, for example, in a FROM clause of a
query or in an INSERT INTO TABLE FUNCTION statement.

:::note[Sample usage of the S3 table function]
```bash
SELECT *
FROM deltaLake('s3://bucket/path/to/lake')
```
:::

:::note
Occasionally, you may find specific table functions disabled for
security reasons.
:::

Aiven for ClickHouse® supports the following table functions:

-   `azureBlobStorage`
-   `base64URLEncode`
-   `base64URLDecode`
-   `cluster`
-   `clusterAllReplicas`
-   `cosn`
-   `deltaLake`
-   `format`
-   `fuzzQuery`
-   `gcs`
-   `generateRandom`
-   `generateSnowflakeID`
-   `generateUUIDv7`
-   `hudi`
-   `iceberg`
-   `input`
-   `loop`
-   `merge`
-   `mysql`
-   `null`
-   `numbers`
-   `numbers_mt`
-   `oss`
-   `postgresql`
-   `printf`
-   `remoteSecure`
-   `s3`
-   `s3Cluster`
-   `snowflakeIDToDateTime`
-   `url`
-   `values`
-   `view`
-   `viewExplain`
-   `viewIfPermitted`
-   `zeros`
-   `zeros_mt`
