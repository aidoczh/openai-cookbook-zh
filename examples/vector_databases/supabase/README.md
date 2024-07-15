# Supabase 向量数据库

[Supabase](https://supabase.com/docs) 是一个基于 [Postgres](https://en.wikipedia.org/wiki/PostgreSQL)（一种生产级别的 SQL 数据库）构建的开源 Firebase 替代方案。

[Supabase Vector](https://supabase.com/docs/guides/ai) 是一个建立在 [pgvector](https://github.com/pgvector/pgvector) 之上的向量工具包，pgvector 是一个 Postgres 扩展，允许您将嵌入存储在与应用程序其他数据相同的数据库中。结合 pgvector 的索引算法，向量搜索在[大规模情况下仍然保持快速](https://supabase.com/blog/increase-performance-pgvector-hnsw)。

Supabase 在 Postgres 之上添加了一系列服务和工具，使得应用程序开发尽可能快速，包括：

- [自动生成的 REST API](https://supabase.com/docs/guides/api)
- [自动生成的 GraphQL API](https://supabase.com/docs/guides/graphql)
- [实时 API](https://supabase.com/docs/guides/realtime)
- [身份验证](https://supabase.com/docs/guides/auth)
- [文件存储](https://supabase.com/docs/guides/storage)
- [边缘函数](https://supabase.com/docs/guides/functions)

我们可以将这些服务与 pgvector 一起使用，以在 Postgres 中存储和查询嵌入。

## OpenAI 手册示例

以下是一些指南和资源，指导您如何将 OpenAI 嵌入模型与 Supabase Vector 结合使用。

| 指南                                       | 描述                                                         |
| ------------------------------------------ | ------------------------------------------------------------ |
| [语义搜索](./semantic-search.mdx)          | 使用 pgvector 大规模存储、索引和查询嵌入                     |

## 其他资源

- [向量列](https://supabase.com/docs/guides/ai/vector-columns)
- [向量索引](https://supabase.com/docs/guides/ai/vector-indexes)
- [带权限的 RAG](https://supabase.com/docs/guides/ai/rag-with-permissions)
- [进入生产环境](https://supabase.com/docs/guides/ai/going-to-prod)
- [计算选择](https://supabase.com/docs/guides/ai/choosing-compute-addon)