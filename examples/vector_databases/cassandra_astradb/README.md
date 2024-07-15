# 使用 Astra DB 和 Cassandra 的 RAG

本目录中的演示展示了如何利用 **DataStax Astra DB** 提供的向量搜索功能，Astra DB 是一个构建在 Apache Cassandra® 上的无服务器数据库即服务（Database-as-a-Service）。

这些示例笔记本展示了如何使用不同的库和 API 实现相同的 GenAI 标准 RAG 工作负载。

要通过 HTTP API 接口使用 [Astra DB](https://docs.datastax.com/en/astra/home/astra.html)，请前往 "AstraPy" 笔记本（`astrapy` 是与数据库交互的 Python 客户端）。

如果你更喜欢通过 CQL 访问数据库（无论是使用 [Astra DB](https://docs.datastax.com/en/astra-serverless/docs/vector-search/overview.html) 还是支持向量搜索的 Cassandra 集群 [supporting vector search](https://cassandra.apache.org/doc/trunk/cassandra/vector-search/overview.html)），请查看 "CQL" 或 "CassIO" 笔记本——它们在抽象层次上有所不同。

如果你想了解更多关于 Astra DB 及其向量搜索功能的信息，请访问 [datastax.com](https://docs.datastax.com/en/astra/home/astra.html)。

### 示例笔记本

以下示例展示了 OpenAI 和 DataStax Astra DB 如何轻松协同工作，为基于向量的人工智能应用提供支持。你可以使用本地 Jupyter 引擎或作为 Colab 笔记本运行它们：

| 用例 | 目标数据库 | 框架 | 笔记本 | Google Colab |
| -------- | --------------- | --------- | -------- | ------------ |
| 搜索/生成引语 | Astra DB | AstraPy | [笔记本](./Philosophical_Quotes_AstraPy.ipynb) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/openai/openai-cookbook/blob/main/examples/vector_databases/cassandra_astradb/Philosophical_Quotes_AstraPy.ipynb) |
| 搜索/生成引语 | 通过 CQL 的 Cassandra / Astra DB | CassIO | [笔记本](./Philosophical_Quotes_cassIO.ipynb) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/openai/openai-cookbook/blob/main/examples/vector_databases/cassandra_astradb/Philosophical_Quotes_cassIO.ipynb) |
| 搜索/生成引语 | 通过 CQL 的 Cassandra / Astra DB | 纯 Cassandra 语言 | [笔记本](./Philosophical_Quotes_CQL.ipynb) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/openai/openai-cookbook/blob/main/examples/vector_databases/cassandra_astradb/Philosophical_Quotes_CQL.ipynb) |

### 向量相似性，可视化表示

![3_vector_space](https://user-images.githubusercontent.com/14221764/262321363-c8c625c1-8be9-450e-8c68-b1ed518f990d.png)