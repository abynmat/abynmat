### Hi, I'm Abyn 👋

I'm a machine learning scientist interested in **graph neural networks**, **risk and anomaly detection on graphs**, and **how small language models learn**. I like small, readable implementations with honest, reproducible experiments.

Everything below is written from the equations in plain PyTorch or NumPy, runs on a laptop, and reports only numbers produced by the code in the repo. Each project checks itself against a reference library or an exact answer, and each README has a "What's different here" section.

#### 🔬 Repositories

| Repo | What's inside | A result |
|---|---|---|
| [**language-models**](https://github.com/abynmat/language-models) | A GPT positional-encoding ablation; a full LLM pipeline (BPE, Llama-style block, scaling sweep, KV cache, SFT); a reasoning model trained with GRPO on verifiable tasks | GRPO raised a model's `<think>` rate from 10% to 83% and accuracy from 68% to 84%; from a model with no chain-of-thought, RL changed nothing |
| [**ml-from-scratch**](https://github.com/abynmat/ml-from-scratch) | 20 classic estimators in NumPy with a parity benchmark; a tensor autograd engine; six landmark papers (Adam, BatchNorm, ResNet, VAE, GAN, DDPM) each with an ablation | Nine estimators match scikit-learn exactly; autograd gradients match PyTorch to 5e-16 |
| [**statistics**](https://github.com/abynmat/statistics) | An 11-chapter causal-inference guide with 12 ground-truth examples; a 9-chapter Bayesian computation guide with MCMC, HMC and filters from scratch | Static TWFE gives 1.16 for a true staggered ATT of 2.70; from-scratch HMC gets 24-33× more effective samples per evaluation than Metropolis |
| [**applied-data-science**](https://github.com/abynmat/applied-data-science) | Kaggle-style tabular problems done rigorously; recommenders on MovieLens; an A/B-testing toolkit; a tabular anomaly-detection benchmark | SMOTE before the split inflates PR-AUC by +0.147; sampled-negative recsys metrics reorder the models |
| [**graph-ml**](https://github.com/abynmat/graph-ml) | GCN, GraphSAGE and GAT in ~200 lines with Cora benchmarks; a synthetic fraud-ring graph and a study of graph features vs GNNs | GCN 82.7% on Cora (paper 81.5%); graph features reach 0.90 AUPRC vs 0.55 for GraphSAGE |

Notes on how these were built, what the most-starred ML repositories have in common, and a roadmap are in [`docs/`](docs/).

#### 🧰 Tools
Python · PyTorch · NumPy · scikit-learn · pandas · Spark SQL · NetworkX · matplotlib

#### 📫 Reach me
✉️ [abyn.mathew.scaria@gmail.com](mailto:abyn.mathew.scaria@gmail.com)
