# 文本比较示例

[OpenAI API 的嵌入端点](https://beta.openai.com/docs/guides/embeddings) 可以用来衡量文本之间的相关性或相似度。

通过利用 GPT-3 对文本的理解，这些嵌入在无监督学习和迁移学习环境中[取得了最先进的结果](https://arxiv.org/abs/2201.10005)。

嵌入可以用于语义搜索、推荐、聚类分析、近似重复检测等。

更多信息，请阅读 OpenAI 的博客文章：

- [介绍文本和代码嵌入（2022年1月）](https://openai.com/blog/introducing-text-and-code-embeddings/)
- [新的改进嵌入模型（2022年12月）](https://openai.com/blog/new-and-improved-embedding-model/)

与其他嵌入模型比较，请参见 [大规模文本嵌入基准（MTEB）排行榜](https://huggingface.co/spaces/mteb/leaderboard)

## 语义搜索

嵌入可以单独使用或作为更大系统的一部分用于搜索。

使用嵌入进行搜索的最简单方法如下：

- 在搜索之前（预计算）：
  - 将你的文本语料库分割成小于令牌限制的块（`text-embedding-3-small` 为 8,191 个令牌）
  - 嵌入每个文本块
  - 将这些嵌入存储在你自己的数据库或向量搜索提供商如 [Pinecone](https://www.pinecone.io)、[Weaviate](https://weaviate.io) 或 [Qdrant](https://qdrant.tech)
- 在搜索时（实时计算）：
  - 嵌入搜索查询
  - 在你的数据库中找到最接近的嵌入
  - 返回最相关的结果

如何使用嵌入进行搜索的示例见 [Semantic_text_search_using_embeddings.ipynb](../examples/Semantic_text_search_using_embeddings.ipynb)。

在更高级的搜索系统中，嵌入的余弦相似度可以作为众多特征之一用于排序搜索结果。

## 问答

让 GPT-3 提供可靠诚实答案的最佳方法是给它提供源文档，以便它能找到正确答案。使用上述语义搜索过程，你可以廉价地搜索文档语料库中的相关信息，然后将这些信息通过提示传递给 GPT-3 来回答问题。我们在 [Question_answering_using_embeddings.ipynb](../examples/Question_answering_using_embeddings.ipynb) 中演示了这一点。

## 推荐

推荐与搜索非常相似，只是输入不是自由形式的文本查询，而是集合中的项目。

如何使用嵌入进行推荐的示例见 [Recommendation_using_embeddings.ipynb](../examples/Recommendation_using_embeddings.ipynb)。

与搜索类似，这些余弦相似度分数可以单独使用来排序项目，也可以作为更大排序算法中的特征。

## 定制嵌入

尽管 OpenAI 的嵌入模型权重不能微调，你仍然可以使用训练数据来定制嵌入以适应你的应用。

在 [Customizing_embeddings.ipynb](../examples/Customizing_embeddings.ipynb) 中，我们提供了一个使用训练数据定制嵌入的示例方法。该方法的思想是训练一个自定义矩阵，通过该矩阵乘以嵌入向量以获得新的定制嵌入。有了良好的训练数据，这个自定义矩阵将有助于强调与你的训练标签相关的特征。你可以等效地将矩阵乘法视为（a）嵌入的修改或（b）用于测量嵌入之间距离的距离函数的修改。