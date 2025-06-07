# RL-MoE
Anomaly detection in time series is a vital component in ensuring the reliability and safety of
industrial systems. While various models exist—ranging from statistical to deep learning-based
detectors—each has its own strengths and weaknesses depending on the nature of the anomaly.
Inspired by the work of Zhang et al. (2022)(Time Series Anomaly Detection via Reinforcement
Learning-Based Model Selection ), which used reinforcement learning to select the best anomaly
detector per time step (via hard selection), we propose an soft mixture-of-experts (MoE) approach
using reinforcement learning. Unlike hard routing, our model softly weighs expert predictions
per sample using a dynamic routing policy trained via Proximal Policy Optimization (PPO). This
allows multiple detectors to contribute based on their confidence and reliability, enabling better
generalization and interpretability. We enhance the routing policy with entropy bonuses to encourage
exploration and use diversity-based rewards to avoid overfitting to a single expert. Our method
is benchmarked on two real-world datasets including SMD and NAB. Same As with RLMSAD
( Zhang et al. (2022)), our current implementation uses ground-truth labels from the test set for
proof-of-concept training. In future work, we aim to improve generalization by training the RL agent
on a validation split and benchmarking against stronger baselines.

This is for submission for Deakin University Research Intern.
