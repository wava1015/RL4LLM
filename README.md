# RL4LLM

## Reinforcement Algorithm
| Title | Affiliation | Code |  Method |
|-----|-----|-----|-----|
| [Chain of Draft: Thinking Faster by Writing Less](https://arxiv.org/pdf/2502.18600) | arXiv 2025.2.25 | [code](https://github.com/sileix/chain-of-draft) | Use prompt "with 5 words at most". |
| [Skeleton-of-Thought: Prompting LLMs for Efficient Parallel Generation](https://arxiv.org/pdf/2307.15337) | ICLR 2024 | [code](https://github.com/imagination-research/sot) | Use prompts to generate the skeleton and then complete each point in parallel. Train a router to decide which question to use SoT. |
| [Sketch-of-Thought: Efficient LLM Reasoning with Adaptive Cognitive-Inspired Sketching](https://arxiv.org/pdf/2503.05179) | arXiv 2025.3.7 | [code](https://github.com/SimonAytes/SoT) | Design a prompting method with 3 paradigms and train a router to select. |
| [Break the Chain: Large Language Models Can be Shortcut Reasoners](https://arxiv.org/pdf/2406.06580v1) | arXiv 2024.6.4 | x | Propose zero-shot prompting strategies to encourage the use of shortcuts. Introduce ShortcutQA, a dataset designed to evaluate reasoning through shortcuts. |
| [Token-Budget-Aware LLM Reasoning](https://arxiv.org/pdf/2412.18547) | arXiv 2025.2.17 | [code](https://github.com/GeniusHTX/TALE) | Use LLM to estimate the optimal CoT budget and then use prompt to generate shorter CoT. |
| [How Well do LLMs Compress Their Own Chain-of-Thought? A Token Complexity Approach](https://arxiv.org/pdf/2503.01141) | arXiv 2025.3.3 | [code](https://github.com/Compressed-CoT/compressed-cot) | Find the relationship between CoT length and accuracy and; there is an intrinsic shortest CoT for successfully solving each task. |
| [Stepwise Perplexity-Guided Refinement for Efficient Chain-of-Thought Reasoning in Large Language Models](https://arxiv.org/pdf/2502.13260) | arXiv 2025.2.28 | x | Use PPL to identify critical reasoning steps. Refine demonstration examples in few-shot CoT or finetuning the model using selected examples that include only critical steps. |
