# Elasticsearch

Elasticsearch 是一款流行的搜索/分析引擎和[向量数据库](https://www.elastic.co/elasticsearch/vector-database)。它提供了一种高效的方式来大规模创建、存储和搜索向量嵌入。

如需技术细节，请参阅[Elasticsearch 文档](https://www.elastic.co/guide/en/elasticsearch/reference/current/knn-search.html)。

[`elasticsearch-labs`](https://github.com/elastic/elasticsearch-labs) 仓库包含了可执行的 Python 笔记本、示例应用和资源，供您测试 Elastic 平台。

## OpenAI 手册笔记本 📒

请查看本仓库中的笔记本，了解如何使用 Elasticsearch 作为向量数据库与 OpenAI 进行交互。

### [语义搜索](https://github.com/openai/openai-cookbook/blob/main/examples/vector_databases/elasticsearch/elasticsearch-semantic-search.ipynb)

在这个笔记本中，您将学习如何：

- 将 OpenAI 的维基百科嵌入数据集索引到 Elasticsearch 中
- 使用 `openai ada-02` 模型对问题进行编码
- 执行语义搜索

<hr>

### [检索增强生成](https://github.com/openai/openai-cookbook/blob/main/examples/vector_databases/elasticsearch/elasticsearch-retrieval-augmented-generation.ipynb)

这个笔记本在语义搜索笔记本的基础上，通过以下步骤进行扩展：

- 从语义搜索中选择最佳匹配结果
- 将该结果发送到 OpenAI 的[聊天补全](https://platform.openai.com/docs/guides/gpt/chat-completions-api) API 端点，以实现检索增强生成（RAG）