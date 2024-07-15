# 网络上的相关资源

人们正在编写优秀的工具和论文，以改进GPT的输出。以下是我们看到的一些很棒的资源：

## 提示库与工具（按字母顺序排列）

- [Arthur Shield](https://www.arthur.ai/get-started)：一个付费产品，用于检测毒性、幻觉、提示注入等。
- [Baserun](https://baserun.ai/)：一个付费产品，用于测试、调试和监控基于LLM的应用程序。
- [Chainlit](https://docs.chainlit.io/overview)：一个用于制作聊天机器人界面的Python库。
- [Embedchain](https://github.com/embedchain/embedchain)：一个用于管理和同步LLM与非结构化数据的Python库。
- [FLAML（一个快速自动机器学习与调优库）](https://microsoft.github.io/FLAML/docs/Getting-Started/)：一个用于自动选择模型、超参数和其他可调选项的Python库。
- [Guidance](https://github.com/microsoft/guidance)：微软提供的一个方便的Python库，使用Handlebars模板来交错生成、提示和逻辑控制。
- [Haystack](https://github.com/deepset-ai/haystack)：一个开源的LLM编排框架，用于在Python中构建可定制、生产就绪的LLM应用程序。
- [HoneyHive](https://honeyhive.ai)：一个企业平台，用于评估、调试和监控LLM应用程序。
- [LangChain](https://github.com/hwchase17/langchain)：一个流行的Python/JavaScript库，用于链接语言模型提示的序列。
- [LiteLLM](https://github.com/BerriAI/litellm)：一个用于以一致格式调用LLM API的最小Python库。
- [LlamaIndex](https://github.com/jerryjliu/llama_index)：一个用于增强LLM应用程序数据的Python库。
- [LMQL](https://lmql.ai)：一种编程语言，用于支持类型化提示、控制流、约束和工具的LLM交互。
- [OpenAI Evals](https://github.com/openai/evals)：一个开源库，用于评估语言模型和提示的任务性能。
- [Outlines](https://github.com/normal-computing/outlines)：一个Python库，提供特定领域的语言来简化提示和约束生成。
- [Parea AI](https://www.parea.ai)：一个用于调试、测试和监控LLM应用程序的平台。
- [Portkey](https://portkey.ai/)：一个用于LLM应用程序的可观察性、模型管理、评估和安全的平台。
- [Promptify](https://github.com/promptslab/Promptify)：一个用于使用语言模型执行NLP任务的小型Python库。
- [PromptPerfect](https://promptperfect.jina.ai/prompts)：一个用于测试和改进提示的付费产品。
- [Prompttools](https://github.com/hegelai/prompttools)：用于测试和评估模型、向量数据库和提示的开源Python工具。
- [Scale Spellbook](https://scale.com/spellbook)：一个用于构建、比较和发布语言模型应用程序的付费产品。
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel)：微软提供的一个Python/C#/Java库，支持提示模板、函数链、向量化记忆和智能规划。
- [Vellum](https://www.vellum.ai/)：一个付费的AI产品开发平台，用于实验、评估和部署高级LLM应用程序。
- [Weights & Biases](https://wandb.ai/site/solutions/llmops)：一个用于跟踪模型训练和提示工程实验的付费产品。
- [YiVal](https://github.com/YiVal/YiVal)：一个开源的GenAI-Ops工具，用于使用自定义数据集、评估方法和进化策略调整和评估提示、检索配置和模型参数。

## 提示指南

- [Brex的提示工程指南](https://github.com/brexhq/prompt-engineering)：Brex对语言模型和提示工程的介绍。
- [learnprompting.org](https://learnprompting.org/)：一个关于提示工程的入门课程。
- [Lil'Log Prompt Engineering](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/)：一位OpenAI研究员对提示工程文献的回顾（截至2023年3月）。
- [OpenAI Cookbook: 提高可靠性的技术](https://cookbook.openai.com/articles/techniques_to_improve_reliability)：一篇稍旧（2022年9月）的关于提示语言模型的技术的回顾。
- [promptingguide.ai](https://www.promptingguide.ai/)：一个展示多种技术的提示工程指南。
- [Xavi Amatriain的Prompt Engineering 101 提示工程入门](https://amatriain.net/blog/PromptEngineering) 和 [202 高级提示工程](https://amatriain.net/blog/prompt201)：一个基本但有主见的提示工程介绍，以及一个后续集合，包含许多从CoT开始的高级方法。

## 视频课程

- [Andrew Ng的DeepLearning.AI](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)：一个关于开发者提示工程的短期课程。
- [Andrej Karpathy 的 Let's build GPT](https://www.youtube.com/watch?v=kCc8FmEb1nY)：深入探讨 GPT 背后的机器学习原理。
- [DAIR.AI 的 Prompt Engineering](https://www.youtube.com/watch?v=dOxUroR57xs)：关于各种 Prompt Engineering 技术的一小时视频。
- [Scrimba 关于 Assistants API 的课程](https://scrimba.com/learn/openaiassistants)：关于 Assistants API 的 30 分钟互动课程。
- [LinkedIn 课程：Prompt Engineering 简介：如何与 AI 对话](https://www.linkedin.com/learning/prompt-engineering-how-to-talk-to-the-ais/talking-to-the-ais?u=0)：关于 Prompt Engineering 的短视频介绍。

## 提升推理能力的进阶提示技术论文

- [思维链提示在大型语言模型中引发推理（2022）](https://arxiv.org/abs/2201.11903)：通过少样本提示让模型逐步思考，可以提高其推理能力。PaLM 在数学应用题（GSM8K）上的得分从 18% 提升到 57%。
- [自一致性改善语言模型中的思维链推理（2022）](https://arxiv.org/abs/2203.11171)：从多个输出中投票可以进一步提高准确性。在 40 个输出中投票，PaLM 在数学应用题上的得分从 57% 提升到 74%，`code-davinci-002` 从 60% 提升到 78%。
- [思维树：大型语言模型中的深思熟虑问题解决（2023）](https://arxiv.org/abs/2305.10601)：通过在逐步推理的树中搜索，比在思维链中投票更能帮助解决问题。这提升了 `GPT-4` 在创意写作和填字游戏上的得分。
- [语言模型是零样本推理者（2022）](https://arxiv.org/abs/2205.11916)：告诉遵循指令的模型逐步思考，可以提高其推理能力。这使得 `text-davinci-002` 在数学应用题（GSM8K）上的得分从 13% 提升到 41%。
- [大型语言模型是人类级别的提示工程师（2023）](https://arxiv.org/abs/2211.01910)：通过自动搜索可能的提示，找到了一个将数学应用题（GSM8K）得分提升到 43% 的提示，比《语言模型是零样本推理者》中的手动提示高出 2 个百分点。
- [Reprompting：通过 Gibbs 采样自动推理链提示推断（2023）](https://arxiv.org/abs/2305.09993)：通过自动搜索可能的思维链提示，ChatGPT 在几个基准测试中的得分提高了 0-20 个百分点。
- [使用大型语言模型进行可信推理（2022）](https://arxiv.org/abs/2208.14271)：通过结合以下系统可以提高推理能力：由选择和推理提示生成的思维链，选择-推理循环中选择何时停止的停止模型，搜索多个推理路径的价值函数，以及帮助避免幻觉的句子标签。
- [STaR：通过推理引导推理（2022）](https://arxiv.org/abs/2203.14465)：可以通过微调将思维链推理融入模型中。对于有答案的任务，可以通过语言模型生成示例思维链。
- [ReAct：在语言模型中协同推理和行动（2023）](https://arxiv.org/abs/2210.03629)：对于使用工具或环境的任务，如果规定性地交替进行**推理**步骤（思考该做什么）和**行动**（从工具或环境中获取信息），思维链效果更好。
- [Reflexion：具有动态记忆和自我反思的自主代理（2023）](https://arxiv.org/abs/2303.11366)：通过记忆先前的失败来重试任务，可以提高后续表现。
- [演示-搜索-预测：为知识密集型 NLP 组合检索和语言模型（2023）](https://arxiv.org/abs/2212.14024)：通过“检索-然后-阅读”增强知识的模型，可以通过多跳搜索链进一步改进。
- [通过多代理辩论改进语言模型中的事实性和推理（2023）](https://arxiv.org/abs/2305.14325)：在几个回合中生成几个 ChatGPT 代理之间的辩论，可以提高各种基准测试的得分。数学应用题得分从 77% 提升到 85%。