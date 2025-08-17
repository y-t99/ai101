## Building effective agents [^1]

### When (and when not) to use agents

When building applications with LLMs, we recommend finding the simplest solution possible, and only increasing complexity when needed. This might mean not building agentic systems at all. Agentic systems often trade latency and cost for better task performance, and you should consider when this tradeoff makes sense.

When more complexity is warranted, workflows offer predictability and consistency for well-defined tasks, whereas agents are the better option when flexibility and model-driven decision-making are needed at scale. For many applications, however, optimizing single LLM calls with retrieval and in-context examples is usually enough.

### Building blocks, workflows, and agents

The common patterns for agentic systems we’ve seen in production:

1. Building block: The augmented LLM | The basic building block of agentic systems is an LLM enhanced with augmentations such as retrieval, tools, and memory.

   > Each LLM call has access to these augmented capabilities in the follower patterns.

2. Workflow: Prompt chaining |Prompt chaining decomposes a task into a sequence of steps, where each LLM call processes the output of the previous one.

3. Workflow: Routing | Routing classifies an input and directs it to a specialized followup task.

4. Workflow: Parallelization | LLMs can sometimes work simultaneously on a task and have their outputs aggregated programmatically.

5. Workflow: Orchestrator-workers | In the orchestrator-workers workflow, a central LLM dynamically breaks down tasks, delegates them to worker LLMs, and synthesizes their results.

6. Workflow: Evaluator-optimizer | In the evaluator-optimizer workflow, one LLM call generates a response while another provides evaluation and feedback in a loop.

7. Agents | understanding complex inputs, engaging in reasoning and planning, using tools reliably, and recovering from errors.

---

## Reading

- [x] A Survey on Large Language Model based Autonomous Agents
- [x] [Claude’s extended thinking ](https://www.anthropic.com/research/visible-extended-thinking)
- [x] [The "think" tool: Enabling Claude to stop and think in complex tool use situations](https://www.anthropic.com/engineering/claude-think-tool)
- [ ] Understanding the planning of LLM agents: A survey
- [ ] ReAct: Synergizing Reasoning and Acting in Language Models
- [ ] Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
- [ ] Tree of Thoughts: Deliberate Problem Solving with Large Language Models
- [ ] Self-Refine: Iterative Refinement with Self-Feedback

---

A Survey on Large Language Model based Autonomous Agents[^4]：主要涵盖智能体的构建、应用和评估方法。

1. 应设计何种架构以更好地利用LLM？
   ![image-20250812102251937](/Users/itoung/Project/ai101/picture/agent-architecture.png)
2. 在给定架构下，如何使智能体获得完成特定任务的能力？ 一是通过微调获取能力，二是通过提示工程或机制工程。

---



---

[^1]: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents): a seminal writeup on simple, composable patterns for building production-ready AI agents.

[^2]: [A practical guide to building agents](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf): This guide is designed for product and engineering teams exploring how to build their first agents.

[^3]: [Context Engineering for AI Agents: Lessons from Building Manus](https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus)
[^4]: [A Survey on Large Language Model based Autonomous Agents](https://arxiv.org/abs/2308.11432)
[^5]: [Understanding the planning of LLM agents: A survey](https://arxiv.org/abs/2402.02716)

