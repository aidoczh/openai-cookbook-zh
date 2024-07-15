# Weaviate <> OpenAI

[​Weaviate](https://weaviate.io) 是一个开源的向量搜索引擎（[文档](https://weaviate.io/developers/weaviate) - [Github](https://github.com/weaviate/weaviate)），能够存储和搜索 OpenAI 嵌入向量及数据对象。该数据库支持相似性搜索、混合搜索（结合多种搜索技术，如基于关键词和向量搜索）以及生成式搜索（如问答）。Weaviate 还支持多种基于 OpenAI 的模块（例如，[`text2vec-openai`](https://weaviate.io/developers/weaviate/modules/retriever-vectorizer-modules/text2vec-openai)、[`qna-openai`](https://weaviate.io/developers/weaviate/modules/reader-generator-modules/qna-openai)），使您能够快速高效地向量化和查询数据。

您可以通过以下三种方式运行 Weaviate（包括所需的 OpenAI 模块）：

1. 在 Docker 容器内运行开源版本（[示例](./docker-compose.yml)）
2. 使用 Weaviate 云服务（[开始使用](https://weaviate.io/developers/weaviate/quickstart/installation#weaviate-cloud-service)）
3. 在 Kubernetes 集群中（[了解更多](https://weaviate.io/developers/weaviate/installation/kubernetes)）

### 示例

本文件夹包含多种 Weaviate 和 OpenAI 示例。

| 名称 | 描述 | 语言 | Google Colab |
| --- | --- | --- | --- |
| [Weaviate 和 OpenAI 入门](./getting-started-with-weaviate-and-openai.ipynb) | 使用 Weaviate 中的 OpenAI 向量化模块（`text2vec-openai`）进行*语义向量搜索*的简单入门 | Python 笔记本 | [链接](https://colab.research.google.com/drive/1RxpDE_ruCnoBB3TfwAZqdjYgHJhtdwhK) |
| [Weaviate 和 OpenAI 混合搜索](./hybrid-search-with-weaviate-and-openai.ipynb) | 使用 Weaviate 中的 OpenAI 向量化模块（`text2vec-openai`）进行*混合搜索*的简单入门 | Python 笔记本 | [链接](https://colab.research.google.com/drive/1E75BALWoKrOjvUhaznJKQO0A-B1QUPZ4) |
| [Weaviate 和 OpenAI 问答](./question-answering-with-weaviate-and-openai.ipynb) | 使用 Weaviate 中的 OpenAI 问答模块（`qna-openai`）进行*问答（Q&A）*的简单入门 | Python 笔记本 | [链接](https://colab.research.google.com/drive/1pUerUZrJaknEboDxDxsuf3giCK0MJJgm) |
| [Docker-compose 示例](./docker-compose.yml) | 启用所有 OpenAI 模块的 Docker-compose 文件 | Docker |