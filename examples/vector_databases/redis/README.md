# Redis

### 什么是 Redis？

大多数有 Web 服务背景的开发者可能对 Redis 并不陌生。Redis 本质上是一个开源的键值存储系统，可用作缓存、消息代理和数据库。开发者选择 Redis 是因为它速度快、拥有庞大的客户端库生态系统，并且多年来已被众多大型企业部署使用。

除了传统的用途，Redis 还提供了 [Redis 模块](https://redis.io/modules)，这是一种通过新功能、命令和数据类型扩展 Redis 的方式。例如模块包括 [RedisJSON](https://redis.io/docs/stack/json/)、[RedisTimeSeries](https://redis.io/docs/stack/timeseries/)、[RedisBloom](https://redis.io/docs/stack/bloom/) 和 [RediSearch](https://redis.io/docs/stack/search/)。

### 部署选项

部署 Redis 有多种方式。对于本地开发，最快的方法是使用 [Redis Stack Docker 容器](https://hub.docker.com/r/redis/redis-stack)，我们将在本文中使用它。Redis Stack 包含多个 Redis 模块，可以组合使用，创建一个快速的多模型数据存储和查询引擎。

对于生产环境，最简单的入门方法是使用 [Redis Cloud](https://redislabs.com/redis-enterprise-cloud/overview/) 服务。Redis Cloud 是一个完全托管的 Redis 服务。你也可以使用 [Redis Enterprise](https://redislabs.com/redis-enterprise/overview/) 在自己的基础设施上部署 Redis。Redis Enterprise 是一个完全托管的 Redis 服务，可以在 Kubernetes、本地或云中部署。

此外，每个主要的云服务提供商（[AWS Marketplace](https://aws.amazon.com/marketplace/pp/prodview-e6y7ork67pjwg?sr=0-2&ref_=beagle&applicationId=AWSMPContessa)、[Google Marketplace](https://console.cloud.google.com/marketplace/details/redislabs-public/redis-enterprise?pli=1) 或 [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/garantiadata.redis_enterprise_1sp_public_preview?tab=Overview)）都在其市场产品中提供了 Redis Enterprise。

### 什么是 RediSearch？

RediSearch 是一个 [Redis 模块](https://redis.io/modules)，为 Redis 提供查询、二级索引、全文搜索和向量搜索功能。要使用 RediSearch，首先需要在 Redis 数据上声明索引，然后可以使用 RediSearch 客户端查询这些数据。有关 RediSearch 功能集的更多信息，请参阅 [RediSearch 文档](https://redis.io/docs/stack/search/)。

### 功能

RediSearch 使用压缩的倒排索引，实现快速索引且内存占用低。RediSearch 索引通过提供精确短语匹配、模糊搜索和数值过滤等功能增强了 Redis。例如：

* Redis 哈希中多个字段的全文索引
* 无性能损失的增量索引
* 向量相似性搜索
* 文档排名（使用 [tf-idf](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)，可选用户提供的权重）
* 字段加权
* 使用 AND、OR 和 NOT 运算符的复杂布尔查询
* 前缀匹配、模糊匹配和精确短语查询
* 支持 [双元音音标匹配](https://redis.io/docs/stack/search/reference/phonetic_matching/)
* 自动完成建议（带模糊前缀建议）
* 多语言的词干查询扩展（使用 [Snowball](http://snowballstem.org/)）
* 支持中文分词和查询（使用 [Friso](https://github.com/lionsoul2014/friso))
* 数值过滤和范围
* 使用 [Redis 地理空间索引](/commands/georadius) 的地理空间搜索
* 强大的聚合引擎
* 支持所有 utf-8 编码文本
* 检索完整文档、选定字段或仅文档 ID
* 排序结果（例如，按创建日期）
* 通过 RedisJSON 支持 JSON

### 客户端

鉴于 Redis 庞大的生态系统，很可能有你需要的语言的客户端库。你可以使用任何标准的 Redis 客户端库来运行 RediSearch 命令，但使用封装了 RediSearch API 的库最为方便。以下是一些示例，但你可以在 [这里](https://redis.io/resources/clients/) 找到更多客户端库。

| 项目 | 语言 | 许可证 | 作者 | 星标 |
|----------|---------|--------|---------|-------|
| [jedis][jedis-url] | Java | MIT | [Redis][redis-url] | ![Stars][jedis-stars] |
| [redis-py][redis-py-url] | Python | MIT | [Redis][redis-url] | ![Stars][redis-py-stars] |
| [node-redis][node-redis-url] | Node.js | MIT | [Redis][redis-url] | ![Stars][node-redis-stars] |
| [nredisstack][nredisstack-url] | .NET | MIT | [Redis][redis-url] | ![Stars][nredisstack-stars] |

[redis-url]: https://redis.com

[redis-py-url]: https://github.com/redis/redis-py
[redis-py-stars]: https://img.shields.io/github/stars/redis/redis-py.svg?style=social&amp;label=Star&amp;maxAge=2592000
[redis-py-package]: https://pypi.python.org/pypi/redis

[jedis-url]: https://github.com/redis/jedis
[jedis-stars]: https://img.shields.io/github/stars/redis/jedis.svg?style=social&amp;label=Star&amp;maxAge=2592000
[Jedis-package]: https://search.maven.org/artifact/redis.clients/jedis

[nredisstack-url]: https://github.com/redis/nredisstack
[nredisstack-stars]: https://img.shields.io/github/stars/redis/nredisstack.svg?style=social&amp;label=Star&amp;maxAge=2592000
[nredisstack-package]: https://www.nuget.org/packages/nredisstack/

[node-redis-url]: https://github.com/redis/node-redis
[node-redis-stars]: https://img.shields.io/github/stars/redis/node-redis.svg?style=social&amp;label=Star&amp;maxAge=2592000
[node-redis-package]: https://www.npmjs.com/package/redis

[redis-om-python-url]: https://github.com/redis/redis-om-python
[redis-om-python-author]: https://redis.com
[redis-om-python-stars]: https://img.shields.io/github/stars/redis/redis-om-python.svg?style=social&amp;label=Star&amp;maxAge=2592000

[redisearch-go-url]: https://github.com/RediSearch/redisearch-go
[redisearch-go-author]: https://redis.com
[redisearch-go-stars]: https://img.shields.io/github/stars/RediSearch/redisearch-go.svg?style=social&amp;label=Star&amp;maxAge=2592000

[redisearch-api-rs-url]: https://github.com/RediSearch/redisearch-api-rs
[redisearch-api-rs-author]: https://redis.com
[redisearch-api-rs-stars]: https://img.shields.io/github/stars/RediSearch/redisearch-api-rs.svg?style=social&amp;label=Star&amp;maxAge=2592000


### 部署选项

部署带有 RediSearch 的 Redis 有多种方式。最简单的入门方法是使用 Docker，但还有许多其他潜在的部署选项，例如：

- [Redis Cloud](https://redis.com/redis-enterprise-cloud/overview/)
- 云市场：[AWS Marketplace](https://aws.amazon.com/marketplace/pp/prodview-e6y7ork67pjwg?sr=0-2&ref_=beagle&applicationId=AWSMPContessa)、[Google Marketplace](https://console.cloud.google.com/marketplace/details/redislabs-public/redis-enterprise?pli=1) 或 [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/garantiadata.redis_enterprise_1sp_public_preview?tab=Overview)
- 本地部署：[Redis Enterprise Software](https://redis.com/redis-enterprise-software/overview/)
- Kubernetes：[Redis Enterprise Software on Kubernetes](https://docs.redis.com/latest/kubernetes/)
- [Docker (RediSearch)](https://hub.docker.com/r/redislabs/redisearch)
- [Docker (Redis Stack)](https://hub.docker.com/r/redis/redis-stack)


### 集群支持

RediSearch 有一个分布式集群版本，可以扩展到数十亿文档，跨越数百台服务器。目前，分布式 RediSearch 作为 [Redis Enterprise Cloud](https://redis.com/redis-enterprise-cloud/overview/) 和 [Redis Enterprise Software](https://redis.com/redis-enterprise-software/overview/) 的一部分提供。

更多信息请参见 [RediSearch on Redis Enterprise](https://redis.com/modules/redisearch/)。

### 示例

- [产品搜索](https://github.com/RedisVentures/redis-product-search) - 电子商务产品搜索（包含图像和文本）
- [产品推荐与 DocArray / Jina](https://github.com/jina-ai/product-recommendation-redis-docarray) - 基于内容的产品推荐示例，使用 Redis 和 DocArray。
- [Redis VSS 在推荐系统中的应用](https://github.com/RedisVentures/Redis-Recsys) - 三种端到端的 Redis 与 NVIDIA Merlin 推荐系统架构。
- [Azure OpenAI 嵌入式问答](https://github.com/ruoccofabrizio/azure-open-ai-embeddings-qna) - 在 Azure 上使用 OpenAI 和 Redis 作为问答服务。
- [ArXiv 论文搜索](https://github.com/RedisVentures/redis-arXiv-search) - 对 arXiv 学术论文进行语义搜索


### 更多资源

有关如何将 Redis 用作向量数据库的更多信息，请查看以下资源：

- [Redis 向量相似性文档](https://redis.io/docs/stack/search/reference/vectors/) - Redis 官方向量搜索文档。
- [Redis-py 搜索文档](https://redis.readthedocs.io/en/latest/redismodules.html#redisearch-commands) - Redis-py 客户端库的 RediSearch 文档。
- [向量相似性搜索：从基础到生产](https://mlops.community/vector-similarity-search-from-basics-to-production/) - 介绍向量相似性搜索和 Redis 作为向量数据库的博客文章。
- [AI 驱动的文档搜索](https://datasciencedojo.com/blog/ai-powered-document-search/) - 涵盖 AI 驱动文档搜索用例和架构的博客文章。
- [向量数据库基准测试](https://jina.ai/news/benchmark-vector-search-databases-with-one-million-data/) - Jina AI 对 Redis 与其他向量数据库的基准测试比较。