# FileBeat 版本


### 启动过程（定制自己的版本）

```
# 修改密码
.env/ELASTIC_PASSWORD
kibana/config/elasticsearch.password

# 修改elasticsearch 数据保存的路径
.env/ES_DATA

# 修改日志文件路径
.env/LOGS_DIR

# 修改读取日志的方式
filebeat/config/filebeat.docker.yml

    paths:
      - /filebeat/logs/*.log
    multiline.pattern: '^ERROR -- |^DEBUG -- |^WARN -- |^INFO -- '
    multiline.negate: true
    multiline.match: after

```

