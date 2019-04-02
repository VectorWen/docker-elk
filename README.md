# FileBeat 版本


### 定制自己的版本

修改elasticsearch 数据保存的路径

```
- /docker/elasticsearch/data:/usr/share/elasticsearch/data
```

修改日志文件路径

```
- /docker/filebeat/logs:/filebeat/logs
```

修改读取日志的方式

```
    paths:
      - /filebeat/logs/*.log
    multiline.pattern: '^ERROR -- |^DEBUG -- |^WARN -- |^INFO -- '
    multiline.negate: true
    multiline.match: after
```