# 执行过滤器

在之前的章节里，我们略过了关于文档分数（查询结果中的\_score字段）的介绍。文档分数的值是一个数字，用来描述查询到的文档与查询条件之间的匹配度。分数越高说明文档越匹配，分数越低则说明相关性越低。

不过不是所有查询条件都需要计算分数，尤其当其只需要“过滤”出文档集的时候。Elasticsearch会探测这些情况，并自动的优化查询执行过程从而忽略计算无用的分数。

前面章节中介绍的[布尔查询（bool query）](/query-dsl/compound-queries/bool-query.md)同样支持filter语句，通过filter过滤条件可以进一步过滤匹配文档的范围，而无需修改分数的计算规则。比如，[范围查询（range query）](/query-dsl/term-level-query/range-query.md)，该查询允许我们通过一个范围值过滤文档。通常用于数值型或日期型的字段过滤。

在下面的例子里，使用布尔查询范围账户余额在20000到30000之间的账户，包括20000和30000。话句话说，就是我们想要查询出余额大于等于20000或者小于等于30000的账户信息:

```bash
curl -XPOST 'localhost:9200/bank/_search?pretty' -d '
{
  "query": {
    "bool": {
      "must": { "match_all": {} },
      "filter": {
        "range": {
          "balance": {
            "gte": 20000,
            "lte": 30000
          }
        }
      }
    }
  }
}'
```

分析上述查询语句，布尔查询包含match\_all查询\(查询部分\)和range查询\(过滤部分\)两个语句。我们也可以在查询和过滤这两个部分插入任意的子查询语句。在上面的例子中，使用范围查询非常适合，因为落在该范围内的文档的匹配度都是相同的，没有哪个文档会比其它文档匹配度高。

除了match\_all, match, bool 和 range 查询之外，还有很多其他类型的查询语句，这里我们不一一赘述。因为我们已经理解了过滤器的运行原理，相信理解和应用其他类型的查询语句不会是一件难事。
