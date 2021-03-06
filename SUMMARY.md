# Summary

* [简介](README.md)
* [1 开始](getting-started/getting-started.md)
  * [1.1 基本概念](getting-started/basic-concepts.md)
    * [1.1.1 译者注\(基本概念\)](getting-started/translator-comment-on-basic-concepts.md)
  * [1.2 安装](getting-started/installation.md)
  * [1.3 探测你的集群](getting-started/exploring-your-cluster/README.md)
    * [1.3.1 集群健康状态](getting-started/exploring-your-cluster/cluster-health.md)
      * [1.3.1.1 译者注（集群健康状态）](getting-started/exploring-your-cluster/translator-note-on-cluster-health.md)
    * [1.3.2 列出所有索引](getting-started/exploring-your-cluster/list-all-indices.md)
    * [1.3.3 创建索引](getting-started/exploring-your-cluster/create-an-index.md)
    * [1.3.4 索引和查询文档](getting-started/exploring-your-cluster/index-and-query-a-document.md)
    * [1.3.5 删除索引](getting-started/exploring-your-cluster/delete-an-index.md)
  * [1.4 修改你的数据](getting-started/modifying-your-data/README.md)
    * [1.4.1 更新文档](getting-started/modifying-your-data/updating-documents.md)
      * [1.4.1.1 译者注\(更新文档\)](getting-started/modifying-your-data/translator-note-updating-documents.md)
    * [1.4.2 删除文档](getting-started/modifying-your-data/deleting-documents.md)
    * [1.4.3 批量处理](getting-started/modifying-your-data/batch-processing.md)
  * [1.5 探测你的数据](getting-started/exploring-your-data/README.md)
    * [1.5.1 查询API](getting-started/exploring-your-data/the-search-api.md)
    * [1.5.2 查询语言介绍](getting-started/exploring-your-data/introducing-the-query-language.md)
    * [1.5.3 执行查询](getting-started/exploring-your-data/executing-searches.md)
      * [1.5.3.1 译者注 - 关于嵌套布尔查询](getting-started/exploring-your-data/translator-note-executing-searches.md)
    * [1.5.4 执行过滤器](getting-started/exploring-your-data/executing-filters.md)
    * [1.5.5 执行聚合](getting-started/exploring-your-data/executing-aggregations.md)
  * [1.6 总结](getting-started/conclusion.md)
* [2 安装](setup/README.md)
  * [2.1 配置](setup/configuration.md)
    * [2.1.1 译者注](setup/translator-note-configuration.md)
  * [2.2 在Linux上以服务形式运行](setup/running-as-a-service-on-linux.md)
    * [2.2.1 译者注](setup/translator-note-running-as-a-service-on-linux.md)
  * [2.3 在Windows上以服务形式运行](setup/running-as-a-service-on-windows.md)
  * [2.4 目录结构](setup/directory-layout.md)
  * [2.5 仓库](setup/repositories.md)
  * [2.6 升级](setup/upgrading/README.md)
    * [2.6.1 备份你的数据](setup/upgrading/back-up-your-data.md)
    * [2.6.2 滚动升级\(Rolling upgrades\)](setup/upgrading/rolling-upgrades.md)
    * [2.6.3 全集群重启升级\(Rolling upgrades\)](setup/upgrading/full-cluster-restart-upgrade.md)
* [3 破坏性变化(Breaking changes)](breaking-changes/README.md)
* [4 API规则(API Conventions)](api-conventions/README.md)
  * [4.1 多索引(Multiple Indices)](api-conventions/multiple-indices.md)
    * [4.1.1 译者注 - 补充样例](api-conventions/translator-note-multiple-indices.md)
  * [4.2 索引名中的日期计算](api-conventions/date-math-support-in-index-names.md)
  * [4.3 通用选项(Common options)](api-conventions/common-options.md)
     * [4.3.1 译者注 - 通用选项(Common options)](api-conventions/translator-note-common-options.md)
  * [4.4 基于URL的访问控制](api-conventions/url-based-access-control.md)
    * [4.4.1 译者注 - 基于URL的访问控制](api-conventions/translator-note-url-based-access-control.md)
* [5 文档API(Document APIs)](document-apis/README.md)
  * [5.1 索引(Index) API](document-apis/index-api.md)
  * [5.2 获取(Get) API](document-apis/get-api.md)
  * [5.3 删除 API](document-apis/delete-api.md)
  * [5.4 更新 API](document-apis/update-api.md)
  * [5.6 多请求API(Multi Get API)](document-apis/multi-get-api.md)
  * [5.7 批量API(Bulk API)](document-apis/bulk-api.md)
* [6 查询接口](search-apis/README.md)
  * [6.2 URI查询](search-apis/uri-search.md)
  * [6.3 请求体查询](search-apis/request-body-search/README.md)
  * [6.7 多查询API(Multi Search API)](search-apis/multi-search-api.md)
* [7 聚合](aggregations/README.md)
  * [7.2 桶聚合(Bucket Aggregations)](aggregations/bucket-aggregations/README.md)
    * [7.2.3 日期范围聚合(Date Range Aggregations)](aggregations/bucket-aggregations/date-range-aggregation.md)
* [8 索引接口(Indices APIs)](indices-apis/README.md)
  * [8.1 创建索引](indices-apis/create-index.md)
  * [8.6 设置映射](indices-apis/put-mapping.md)
  * [8.10 索引别名](indices-apis/index-aliases.md)
  * [8.22 Flush](indices-apis/flush/README.md)
    * [8.22.1 同步Flush](indices-apis/flush/synced-flush.md)
* [9 cat APIs](cat-apis/README.md)
  * [9.5 cat health](cat-apis/cat-health.md)
  * [9.9 cat nodes](cat-apis/cat-nodes.md)
  * [9.12 cat recovery](cat-apis/cat-recovery.md)
* [10 集群API\(Cluster APIs\)](cluster-apis/README.md)
  * [10.1 集群健康\(Cluster Health\)](cluster-apis/cluster-health.md)
  * [10.2 集群状态\(Cluster State\)](cluster-apis/cluster-state.md)
  * [10.3 集群统计信息\(Cluster Stats\)](cluster-apis/cluster-stats.md)
  * [10.4 集群中挂起的任务](cluster-apis/pending-cluster-tasts.md)
  * [10.5 集群重新分配](cluster-apis/cluster-reroute.md)
  * [10.6 集群更新配置](cluster-apis/cluster-update-setting.md)
  * [10.7 节点统计信息\(Nodes Stats\)](cluster-apis/nodes-stats.md)
  * [10.8 节点信息\(Nodes Info\)](cluster-apis/nodes-info.md)
  * [10.9 任务管理API](cluster-apis/task-management-api.md)
  * [10.10 节点热点线程\(Nodes hot\_threads\)](cluster-apis/nodes-hot-threads.md)
* [11 查询领域专用语言\(DSL\)](query-dsl/README.md)
  * [11.3 全文检索](query-dsl/full-text-query/README.md)
    * [11.3.1 匹配查询\(Match Query\)](query-dsl/full-text-query/match-query.md)
  * [11.4 词条级查询\(Term level Query\)](query-dsl/term-level-query/README.md)
    * [11.4.3 范围查询\(Range Query\)](query-dsl/term-level-query/range-query.md)
  * [11.5 组合查询](query-dsl/compound-queries/README.md)
    * [11.5.2 布尔查询\(bool query\)](query-dsl/compound-queries/bool-query.md)
  * [11.7 Geo查询（Geo Queries）](query-dsl/geo-queries/README.md)
    * [11.7.3 Geo 距离查询（Geo Distance Query）](query-dsl/geo-queries/geo-distance-query.md)
    * [11.7.6 Geohash Cell 查询（Geohash Cell Query）](query-dsl/geo-queries/geohash-cell-query.md)
* [12 映射\(Mapping\)](mapping/README.md)
  * [12.2 字段数据类型](mapping/field-datatypes/README.md)
    * [12.2.4 日期类型](mapping/field-datatypes/date-datatype.md)
  * [12.3 原数据字段(Meta-Field)](mapping/meta-field/README.md)
    * [12.3.9 时间戳字段(_timestamp field)](mapping/meta-field/_timestamp-field.md)
    * [12.3.10 _ttl字段](mapping/meta-field/_ttl-field.md)
* [14 组件\(Modules\)](modules/README.md)
  * [14.2 发现](modules/discovery/README.md)
    * [14.2.4 Zen Discovery(发现)](modules/discovery/zen-discovery.md)
  * [14.4 HTTP](modules/http.md)
  * [14.9 脚本\(Scripting\)](modules/scripting/README.md)
  * [14.10 快照和恢复](modules/snapshot-and-restore.md)
* [15 索引组件](index-modules/README.md)
  * [15.1 分析](index-modules/analysis.md)
  * [15.2 索引分块分配](index-modules/index-shard-allocation/README.md)
    * [15.2.1 分块分配过滤(Shard Allocation Filtering)](index-modules/index-shard-allocation/shard-allocation-filtering.md)
    * [15.2.2 当节点离线时延迟分配](index-modules/index-shard-allocation/delaying-allocation-when-a-node-leaves.md)
    * [15.2.3 索引恢复优先级](index-modules/index-shard-allocation/index-recovery-prioritization.md)
    * [15.2.4 每个节点上的分块数量](index-modules/index-shard-allocation/total-shards-per-node.md)
  * [15.3 映射(Mapper)](index-modules/mapper.md)
  * [15.4 合并(Merge)](index-modules/merge.md)
  * [15.5 相似性组件(Similary module)](index-modules/similarity-module.md)
  * [15.6 查看日志](index-modules/show-log.md)
  * [15.7 存储](index-modules/store.md)
  * [15.8 事务日志(Translog)](index-modules/translog.md)
  、




 










