# clickhouse driver
```
mkdir plugins
export METABASE_VERSION=v0.53.x
export METABASE_CLICKHOUSE_DRIVER_VERSION=1.53.3
curl -L -o plugins/ch.jar https://github.com/ClickHouse/metabase-clickhouse-driver/releases/download/$METABASE_CLICKHOUSE_DRIVER_VERSION/clickhouse.metabase-driver.jar


```
docker run -d -p 3000:3000 \
  --mount type=bind,source=$PWD/plugins/ch.jar,destination=/plugins/clickhouse.jar \
  metabase/metabase:$METABASE_VERSION