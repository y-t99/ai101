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

## A practical guide to building agents[^2]



---

[^1]: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents): a seminal writeup on simple, composable patterns for building production-ready AI agents.

[^2 ]: [A practical guide to building agents](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf): This guide is designed for product and engineering teams exploring how to build their first agents,

