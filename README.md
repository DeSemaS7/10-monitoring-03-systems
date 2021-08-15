## Task 1
[grafana screenshot](prom-datasource.png)

## Task 2
Утилизация CPU для nodeexporter (в процентах, 100-idle)
```json
100 - (avg by (instance) (rate(node_cpu_seconds_total{job="node",mode="idle"}[1m])) * 100)'''
```

CPULA 1/5/15
```json
node_load1{instance="localhost:9100",job="node"}
node_load5{instance="localhost:9100",job="node"}
node_load15{instance="localhost:9100",job="node"}
```
Количество свободной оперативной памяти
```json
node_memory_MemFree_bytes{instance="localhost:9100"}
```
Количество места на файловой системе
```json
node_filesystem_avail_bytes{device="/dev/sde",instance="localhost:9100",job="node"}
```

[dashboard screenshot](dashboard.png)

## Task2