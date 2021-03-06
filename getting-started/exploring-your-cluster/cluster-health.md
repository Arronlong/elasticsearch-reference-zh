# 集群健康状态

现在开始介绍基本的集群健康检查，通过健康检查我们可以知道集群当前的运行情况。这里我们使用curl命令做演示，当然你也可以使用任何可以发送HTTP\/REST请求的工具。假定我们仍在刚才启动Elasticsearch节点的机器上，并且打开另一个命令行窗口。

我们使用[\_cat API](/cat-apis/README.md)来检查集群健康状态。记住，之前我们的节点开放在9200端口：

```bash
curl 'localhost:9200/_cat/health?v'
```

响应信息：

```bash
epoch      timestamp cluster       status node.total node.data shards pri relo init unassign
1394735289 14:28:09  elasticsearch green           1         1      0   0    0    0        0
```

可以看到，我们的集群名为“elasticsearch”，并且状态是绿色的。

不论何时检查集群状态，我们都有可能得到绿色、黄色或者红色的状态值。绿色代表一切正常（集群功能完全可用），黄色代表所有数据都可用但是某些副本没有完成分配（集群功能完全可用），而红色代表某些数据由于某种原因不可用。需要注意的时，哪怕集群状态是红色，集群仍是部分可用的（也就是说，在可用分块上集群仍提供检索功能），但是由于数据丢失，你需要尽快的修复它。

通过上述响应信息还可以看到，目前我们拥有一个节点，0个分块，因为集群中还没有数据。另外，由于我们使用了默认的集群名（elasticsearch）并且Elasticsearch默认使用单播网络来自动探测本机上其他节点，所以你可以你在电脑上启动多个节点并将这些节点加入同一个集群。在这种情况下，你会在上述响应信息中看到多于1个的节点信息。

我们可以通过如下命令来获取节点列表：

```bash
curl 'localhost:9200/_cat/nodes?v'
```

响应如下：

```bash
curl 'localhost:9200/_cat/nodes?v'
host         ip        heap.percent ram.percent load node.role master name
mwubuntu1    127.0.1.1            8           4 0.00 d         *      New Goblin
```

这里可以看到，我们的节点名为“New Goblin”，是我们集群中的唯一节点。

