# Typesense

Typesense 是一个开源的内存搜索引擎，你可以选择[自行托管](https://typesense.org/docs/guide/install-typesense.html#option-2-local-machine-self-hosting)或在[Typesense Cloud](https://cloud.typesense.org/)上运行。

## 为什么选择 Typesense？

Typesense 通过将整个索引存储在 RAM 中（并在磁盘上备份）来专注于性能，同时也通过简化可用选项和设置良好默认值来提供开箱即用的开发者体验。

它还允许你将基于属性的过滤与向量查询结合起来，以获取最相关的文档。

### 其他功能

除了向量存储和搜索，Typesense 还提供以下功能：

- 拼写容错：优雅地处理拼写错误，开箱即用。
- 可调排名：轻松定制搜索结果至完美。
- 排序：在查询时动态根据特定字段排序（对于“按价格升序排序”等功能很有帮助）。
- 分面与过滤：深入细化结果。
- 分组与去重：将相似结果分组以显示更多多样性。
- 联合搜索：通过单个 HTTP 请求跨多个集合（索引）进行搜索。
- 作用域 API 密钥：生成仅允许访问某些记录的 API 密钥，适用于多租户应用程序。
- 同义词：定义互为等价的单词，搜索一个单词时也会返回定义的同义词结果。
- 精选与 merchandizing：将特定记录提升到搜索结果中的固定位置，以突出显示它们。
- 基于 Raft 的集群：设置一个高可用的分布式集群。
- 无缝版本升级：随着 Typesense 新版本的发布，升级就像替换二进制文件并重启 Typesense 一样简单。
- 无运行时依赖：Typesense 是一个单一二进制文件，你可以在本地或生产环境中通过一个命令运行。

## 如何使用

- 要了解如何将 Typesense 与 OpenAI 嵌入结合使用，请参阅此处的示例笔记本：[examples/vector_databases/Using_vector_databases_for_embeddings_search.ipynb](/examples/vector_databases/Using_vector_databases_for_embeddings_search.ipynb)
- 要了解更多关于 Typesense 的向量搜索功能，请阅读文档：[https://typesense.org/docs/0.24.1/api/vector-search.html](https://typesense.org/docs/0.24.1/api/vector-search.html)。