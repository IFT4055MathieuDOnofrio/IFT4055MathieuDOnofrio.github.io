# Inverse reinforcement learning with multiple morphologies

## Project description

In the domain of reinforcement learning (RL), an agent learns optimal decision-making by interacting with an environment, guided by a specific reward signal. However, explicitly defining or even determining a reward function in real-world applications can be challenging. Inverse reinforcement learning (IRL) seeks to infer this reward function based on observed behavior.

This project aims to derive a universal reward function that can effectively accommodate agents with various morphologies—a significant challenge given the complex nature of designing "properly shaped" reward functions. We are exploring the use of a transformer architecture to formulate this reward function. Our approach involves training a policy for one morphology using data from another in-domain morphology with distinct dynamics, thus addressing major challenges in reward and policy generalization across different agent forms.

## Reports

Some of the dates may not be entirely accurate, since I estimated them from my notes and memory.

### 4/29/2023

Task: Prepare presentation and finalize report.

### 4/21/2024

Task: Continue executing final experiments.

### 4/15/2024

Task: Ongoing experiments with adjustments to architecture for enhanced performance and stability.

Challenges:
- ML-IRL with the transformer-based reward, when trained on a single morphology, performs approximately 30% worse than the MLP-based reward.
- Stability issues persist with the transformer reward, despite various experimental adjustments.
- When applied to multiple morphologies, the transformer reward underperforms compared to expert benchmarks by roughly 38%.
- Reward transfer using the transformer model fails to converge, even for familiar morphologies.

Achievements:
- Resolved issues related to transformer model size, significantly boosting performance.
- Stability improvements noted when the transformer reward is applied across multiple morphologies.
- Both full transformer architecture and transformer encoder-only setups show promising results, the latter being beneficial for state-only ML-IRL and potential transfer learning applications.

### 4/8/2024

Task: Implemented initial transformer architecture inspired by AnyMorph and started the primary experiments.

Implemented the initial transformer architecture based off the AnyMorph architecture and started running the main experiments.

Observations:
- MLP reward models closely match expert returns, yet exhibit fluctuations and sporadic failures.
- The ML-IRL feedback loop was particularly sensitive to the transformer model size, requiring considerable adjustments.

### 4/1/2024

With assistance from Adriana, one of Glen's students, resolved issues with the Tianshou library affecting reward modifications.

### 3/25/2024

Encountered a major setback as the ML-IRL algorithm seemed to ignore the modified reward function and relied on the original rewards.

### 3/18/2024

Implemented and trained Soft Actor-Critic (SAC) policies for various morphologies and began integrating the ML-IRL algorithm into our codebase.

### 3/11/2024

Discussed the AnyMorph paper and related concerns with Brandon, the author. This clarified the tokenization approach and confirmed that AnyMorph aims solely for in-domain generalization.

### 3/4/2024

Integrated the ModularRL environments into our codebase, adapting them for the latest version of Gymnasium.

### 2/26/2024

Reviewed the ML-IRL paper and set up a work environment in Glen’s lab for remote model training. Opted to develop our ML-IRL implementation from scratch instead of using an unmaintained codebase.

ML-IRL paper: https://arxiv.org/abs/2210.01282

### 2/5/2024

Reviewed literature of single-policy-multiple-morphology including the AnyMorph paper.

AnyMorph: https://arxiv.org/abs/2206.12279
Shared Modular Policies: https://arxiv.org/abs/2007.04976
Amorpheus: https://arxiv.org/abs/2010.01856

### Start of semester

Dedicated time to identifying a suitable project, I delved into various concepts of reinforcement learning (RL) and deep reinforcement learning (Deep RL). Additionally, I explored popular frameworks and libraries, including Gymnasium.

Ultimately, we decided to pursue a project that integrates Maximum-likelihood Inverse Reinforcement Learning (ML-IRL) with a morphology-agnostic transformer architecture, known as AnyMorph.



