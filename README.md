# RL4LLM

## Reinforcement Algorithm
| Title | Affiliation | Code |  Method |
|-----|-----|-----|-----|
| [Proximal Policy Optimization Algorithms (PPO)](https://arxiv.org/abs/1707.06347) | OpenAI 2017 | x | RLHF 中的经典强化算法。🔥采样重要性采样从 online RL 转向 offline RL，增强训练效率。🔥采用 clip 机制维持梯度更新“步长”，防止陷入局部最优。|
| [Direct Preference Optimization: Your Language Model is Secretly a Reward Model (DPO)](https://arxiv.org/abs/2305.18290) | Stanford 2024 | x | 依托 Bradley-Terry，隐式地与 PPO 实现相同的优化目标。🔥采用直接偏好学习代替显示的奖励建模，提升训练效率。 |
| [DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models (GRPO)](https://arxiv.org/abs/2402.03300) | DeepSeek 2024 | [code](https://github.com/deepseek-ai/DeepSeek-Math) | 在 PPO 的基础上进行改进。🔥舍弃了 Critic Model，针对同一 question 采样一组 responses，并对 responses 的 rewards 进行组内归一化得到每个 response 对应的 advantage。🔥在目标函数中引入了反向KL散度。 |
| [Understanding R1-Zero-Like Training: A Critical Perspective (Dr.GRPO)](https://arxiv.org/abs/2503.20783) | NUS 2025 | [code](https://github.com/sail-sg/understand-r1-zero) | 在 GRPO 的基础上进行改进。🔥认为 GRPO 中存在两方面的 bias: 1)GRPO 针对 responses 的长度取平均会引入 length bias，导致损失函数鼓励更短的优势输出和更长的劣势输出；2)GRPO对rewards进行组内归一化时除以标准差会引入 Question-level difficulty bias，即更难的问题往往伴随更大的方差，从而获得更小的梯度更新。🔥改进：直接舍弃掉了导致两种 bias 的算子。 |
| [DAPO: An Open-Source LLM Reinforcement Learning System at Scale (DAPO)](https://arxiv.org/abs/2503.14476) | ByteDance Seed 2025 | [code](https://github.com/volcengine/verl) | 在GRPO的基础上进行改进。🔥Clip-Higher: 避免 entropy collapse。🔥Dynamic Sampling: 提升训练效率与稳定性。🔥Token-Level Policy Gradient Loss: 适用于 long-CoT RL 场景。🔥Overlong Reward Shaping:减少 reward noise。 |

