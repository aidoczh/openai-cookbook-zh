**[SingleStoreDB](https://singlestore.com)** 通过我们的 [向量函数](https://docs.singlestore.com/managed-service/en/reference/sql-reference/vector-functions.html) 提供了一流的向量搜索支持。我们的向量数据库子系统自2017年首次推出后不断增强，能够通过SQL轻松实现极快的最近邻搜索，找到语义上相似的对象。

SingleStoreDB 支持使用 dot_product（用于余弦相似度）和 euclidean_distance 函数进行向量和向量相似度搜索。这些函数被我们的客户用于包括人脸识别、视觉产品照片搜索和基于文本的语义搜索等应用。随着生成式AI技术的爆发，这些功能为基于文本的AI聊天机器人奠定了坚实的基础。

但请记住，SingleStoreDB 是一个高性能、可扩展的现代SQL数据库管理系统，支持多种数据模型，包括结构化数据、基于JSON的半结构化数据、时间序列、全文、空间、键值以及当然的向量数据。立即开始使用 SingleStoreDB 为您的下一个智能应用赋能吧！

![SingleStore Open AI](https://user-images.githubusercontent.com/8846480/236985121-48980956-fdc5-49c8-b006-f3a412142676.png)

## 示例

此文件夹包含 SingleStoreDB 与 OpenAI 结合使用的示例。我们将持续添加更多场景，敬请关注！

| 名称 | 描述 |
| --- | --- |
| [OpenAI Wikipedia 语义搜索](./OpenAI_wikipedia_semantic_search.ipynb) | 通过 SingleStoreDB 的语义搜索提升 ChatGPT 在问答中的准确性 |