# 集群健康状态

现在开始介绍基本的集群健康检查，通过健康检查我们可以知道集群当前的运行情况。这里我们使用curl命令做演示，当然你也可以使用任何可以发送HTTP\/REST请求的工具。假定我们仍在刚才启动Elasticsearch节点的机器上，并且打开另一个命令行窗口。

我们使用\_cat API来检查集群健康状态。记住，之前我们的节点开放在9200端口：

```
curl 'localhost:9200/_cat/health?v'
```

响应信息：

```
epoch      timestamp cluster       status node.total node.data shards pri relo init unassign
1394735289 14:28:09  elasticsearch green           1         1      0   0    0    0        0
```

可以看到，我们的集群名为“elasticsearch”，并且状态是绿色的。


