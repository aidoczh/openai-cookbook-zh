# 什么是 Neon？

[Neon](https://neon.tech/) 是为云构建的无服务器 Postgres。Neon 将计算和存储分离，提供现代开发者功能，如自动扩展、数据库分支、零规模等。

## 向量搜索

Neon 支持使用 [pgvector](https://neon.tech/docs/extensions/pgvector) 开源 PostgreSQL 扩展进行向量搜索，使 Postgres 成为用于存储和查询嵌入的向量数据库。

## OpenAI 手册笔记本

查看本仓库中的笔记本，了解如何将 Neon 无服务器 Postgres 作为向量数据库使用。

### 使用 Neon Postgres 和 pgvector 以及 OpenAI 进行语义搜索

在这个笔记本中，您将学习如何：

1. 使用 OpenAI API 创建的嵌入
2. 将嵌入存储在 Neon 无服务器 Postgres 数据库中
3. 使用 OpenAI API 将原始文本查询转换为嵌入
4. 使用带有 `pgvector` 扩展的 Neon 进行向量相似性搜索

## 扩展支持

Neon 使您能够通过以下功能扩展您的 AI 应用程序：

- [自动扩展](https://neon.tech/docs/introduction/read-replicas)：如果您的 AI 应用程序在一天中的某些时段或不同时间遇到高负载，Neon 可以自动扩展计算资源，无需手动干预。在非活动期间，Neon 能够缩减至零。
- [即时只读副本](https://neon.tech/docs/introduction/read-replicas)：Neon 支持即时只读副本，这些副本是独立的只读计算实例，旨在对与您的读写计算相同的数据执行读操作。通过只读副本，您可以将读取操作从读写计算实例卸载到专用的只读计算实例，以供您的 AI 应用程序使用。
- [Neon 无服务器驱动程序](https://neon.tech/docs/serverless/serverless-driver)：Neon 支持适用于 JavaScript 和 TypeScript 应用程序的低延迟无服务器 PostgreSQL 驱动程序，使您能够从无服务器和边缘环境中查询数据，从而实现亚 10 毫秒的查询。

## 更多示例

- [构建一个 AI 驱动的语义搜索应用程序](https://github.com/neondatabase/yc-idea-matcher) - 提交一个创业想法，获取 YCombinator 之前投资过的类似想法列表
- [构建一个 AI 驱动的聊天机器人](https://github.com/neondatabase/ask-neon) - 一个使用 Postgres 作为向量数据库的 Postgres Q&A 聊天机器人
- [Vercel Postgres pgvector 入门](https://vercel.com/templates/next.js/postgres-pgvector) - 使用 Vercel Postgres（由 Neon 驱动）进行向量相似性搜索

## 其他资源

- [使用 Neon 构建 AI 应用程序](https://neon.tech/ai)
- [Neon AI 和嵌入文档](https://neon.tech/docs/ai/ai-intro)
- [使用 Vercel、OpenAI 和 Postgres 构建 AI 驱动的聊天机器人](neon.tech/blog/building-an-ai-powered-chatbot-using-vercel-openai-and-postgres)
- [基于 Web 的 AI SQL 游乐场以及从浏览器连接到 Postgres](https://neon.tech/blog/postgres-ai-playground)
- [pgvector GitHub 仓库](https://github.com/pgvector/pgvector)