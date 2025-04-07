# RL4LLM

## Reinforcement Algorithm
| Title | Affiliation | Code |  Method |
|-----|-----|-----|-----|
| [Proximal Policy Optimization Algorithms (PPO)](https://arxiv.org/abs/1707.06347) | OpenAI 2017 | x | RLHF中的经典强化算法。🔥采样重要性采样从 online RL 转向 offline RL，增强训练效率。🔥采用 clip 机制维持梯度更新“步长”，防止陷入局部最优。|
| [Direct Preference Optimization: Your Language Model is Secretly a Reward Model (DPO)](https://arxiv.org/abs/2305.18290) | Stanford 2024 | x | 依托 Bradley-Terry，隐式地与PPO实现相同的优化目标。🔥采用直接偏好学习代替显示的奖励建模，提升训练效率。 |
| [DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models (GRPO)](https://arxiv.org/abs/2402.03300) | DeepSeek 2024 | [code](https://github.com/deepseek-ai/DeepSeek-Math) | 在PPO的基础上进行优化。🔥舍弃了 Critic Model，针对同一 question 采样一组 responses，并对 responses 的 rewards 进行组内归一化得到每个 response 对应的 advantage。🔥在目标函数中引入了反向KL散度。 |
| [Break the Chain: Large Language Models Can be Shortcut Reasoners](https://arxiv.org/pdf/2406.06580v1) | arXiv 2024.6.4 | x | Propose zero-shot prompting strategies to encourage the use of shortcuts. Introduce ShortcutQA, a dataset designed to evaluate reasoning through shortcuts. |
| [Token-Budget-Aware LLM Reasoning](https://arxiv.org/pdf/2412.18547) | arXiv 2025.2.17 | [code](https://github.com/GeniusHTX/TALE) | Use LLM to estimate the optimal CoT budget and then use prompt to generate shorter CoT. |
| [How Well do LLMs Compress Their Own Chain-of-Thought? A Token Complexity Approach](https://arxiv.org/pdf/2503.01141) | arXiv 2025.3.3 | [code](https://github.com/Compressed-CoT/compressed-cot) | Find the relationship between CoT length and accuracy and; there is an intrinsic shortest CoT for successfully solving each task. |
| [Stepwise Perplexity-Guided Refinement for Efficient Chain-of-Thought Reasoning in Large Language Models](https://arxiv.org/pdf/2502.13260) | arXiv 2025.2.28 | x | Use PPL to identify critical reasoning steps. Refine demonstration examples in few-shot CoT or finetuning the model using selected examples that include only critical steps. |
