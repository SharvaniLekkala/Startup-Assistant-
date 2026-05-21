# AI Startup Strategy Engine — Version 1

# Workflow Execution Logic

The workflow operates sequentially.

Each agent:
1. Receives context from previous agent
2. Performs specialized reasoning
3. Generates structured output
4. Passes output to next agent

This demonstrates:
- layered AI reasoning
- context propagation
- multi-agent orchestration
- workflow automation

# Why Multiple Ollama Nodes Were Used

Each agent contains an independent Ollama inference stage because every agent performs a separate reasoning operation.

Benefits:
- isolated reasoning
- modular architecture
- specialized analysis
- scalable workflow design

This architecture reflects real-world agentic AI orchestration systems.

# Runtime Metrics

| Agent | Prompt Purpose | Ollama Model | Prompt Processing Time | Ollama Inference Time | Individual Agent Runtime | Cumulative Workflow Runtime |
|---|---|---|---|---|---|---|
| Idea Generator Agent | Generate startup concept | TinyLlama | 7 ms | 41.1 sec | 41.1 sec | 41.1 sec |
| Research Agent | Analyze market and competitors | TinyLlama | 14 ms | 9.1 sec | 9.1 sec | 50.2 sec |
| Technical Architect Agent | Generate technical architecture | TinyLlama | 142 ms | 45.8 sec | 45.8 sec | 1.6 min |
| Investor Agent | Evaluate monetization and scalability | TinyLlama | 14 ms | 16 sec | 16 sec | 1.26 min |
| Final Summarizer Agent | Generate final startup blueprint | TinyLlama | 18 ms | 1.02 min | 1.02 min | 2.28 min |


# Final Workflow Metrics

| Metric | Value |
|---|---|
| Total Agents | 5 |
| Workflow Type | Sequential Multi-Agent |
| Total Workflow Runtime | ~2.28 min |
| Execution Mode | Local Offline Inference |
| Context Passing | Enabled |
| Pipeline Depth | 5 Layers |
| AI Runtime | Ollama |
| Orchestration Framework | Langflow |

# Key Features Implemented

| Feature | Status |
|---|---|
| Multi-Agent Workflow | Implemented |
| Sequential Prompt Chaining | Implemented |
| Local LLM Execution | Implemented |
| Context Passing | Implemented |
| Structured AI Roles | Implemented |
| Startup Blueprint Generation | Implemented |
| Workflow Automation | Implemented |

# Challenges Encountered

| Challenge | Explanation |
|---|---|
| Slow Runtime | Sequential local inference increased cumulative latency |
| Formatting Collapse | Small models struggled with long-context summarization |
| Long Context Handling | Later agents received very large prompts |
| Output Consistency | Smaller models occasionally ignored formatting instructions |

# Solutions Implemented

| Problem | Solution |
|---|---|
| Poor Formatting | Added strict markdown headings |
| Slow Runtime | Reduced prompt complexity |
| Context Overload | Shortened responses |
| Inconsistent Outputs | Added explicit formatting instructions |
| Weak Summarization | Switched to Qwen2:0.5b |

# Key Observations

1. Sequential multi-agent systems improve reasoning depth.
2. Local LLM orchestration is possible without cloud APIs.
3. Prompt engineering strongly affects output quality.
4. Smaller models struggle with long-context consistency.
5. Multi-agent workflows increase cumulative inference latency.
6. Structured prompts significantly improve summarization quality.

![alt text](image.png)
