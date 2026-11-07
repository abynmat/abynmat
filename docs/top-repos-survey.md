# What the most-starred data-science repositories have in common

Survey date: 2026-11-06. Star counts come from the GitHub REST API (`search/repositories` sorted by stars, and
`repos/{owner}/{repo}`), queried the same day. They move daily; treat them as a ranking, not a number.

## 1. The top of the leaderboard by topic

| Topic query | Top project-style repos (not frameworks) | Stars |
|---|---|---|
| `machine-learning` | rasbt/LLMs-from-scratch | 107.9k |
| | mlabonne/llm-course | 84.9k |
| | rohitg00/ai-engineering-from-scratch | 77.1k |
| `deep-learning` | labmlai/annotated_deep_learning_paper_implementations | 67.7k |
| | microsoft/AI-For-Beginners | 70.6k |
| `data-science` | microsoft/ML-For-Beginners | 92.0k |
| | GokuMohandas/Made-With-ML | 49.9k |
| | microsoft/Data-Science-For-Beginners | 38.0k |
| `jupyter-notebook` + `data-science` | CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers | 28.2k |
| | recommenders-team/recommenders | 22.0k |
| `kaggle` | donnemartin/data-science-ipython-notebooks | 29.4k |
| | faridrashidi/kaggle-solutions | 6.6k |
| `bayesian-statistics` | markdregan/Bayesian-Modelling-in-Python | 2.5k |
| | AllenDowney/ThinkBayes2 | 2.1k |
| "from scratch" in name/description | eriklindernoren/ML-From-Scratch | 33.3k |
| | neonwatty/machine-learning-refined | 2.3k |
| | patrickloeber/MLfromscratch | 1.7k |

Frameworks (tensorflow 201k, transformers 169k, pytorch 105k, scikit-learn 68k, pandas 50k) dominate the raw
counts but are not portfolio material. The table above keeps only repos a single person or small team could have
written.

## 2. Single-author repos that became famous

| Repo | Stars | Last push | What it is |
|---|---|---|---|
| karpathy/nanoGPT | 64.5k | 2025-11 | Minimal GPT training in ~600 lines |
| jakevdp/PythonDataScienceHandbook | 50.4k | 2024-06 | Full book as notebooks: NumPy, pandas, matplotlib, sklearn |
| Avik-Jain/100-Days-Of-ML-Code | 52.0k | 2023-12 | Daily learning log with infographics |
| eugeneyan/applied-ml | 30.8k | 2024-07 | Curated papers/blogs on ML in production |
| donnemartin/data-science-ipython-notebooks | 29.4k | 2024-03 | Broad notebook collection |
| CamDavidsonPilon/Bayesian-Methods-for-Hackers | 28.2k | 2024-06 | Bayesian inference taught by code, PyMC |
| karpathy/nn-zero-to-hero | 25.3k | 2024-08 | Lecture code: micrograd, makemore, GPT |
| karpathy/minGPT | 25.0k | 2024-08 | Readable GPT in ~300 lines |
| trekhleb/homemade-machine-learning | 24.8k | 2025-11 | Classic ML in NumPy with notebooks and math |
| stas00/ml-engineering | 19.7k | 2026-11 | Large-model training engineering handbook |
| rlabbe/Kalman-and-Bayesian-Filters-in-Python | 19.5k | 2024-08 | Interactive book on filtering |
| mrdbourke/pytorch-deep-learning | 19.4k | 2026-09 | PyTorch course with exercises |
| karpathy/micrograd | 18.7k | 2026-08 | Scalar autograd engine in ~100 lines |
| ddbourgin/numpy-ml | 16.3k | 2023-10 | Very broad NumPy reimplementations |
| rushter/MLAlgorithms | 11.2k | 2026-09 | Minimal, clean ML algorithm implementations |
| Yorko/mlcourse.ai | 10.8k | 2026-09 | Open ML course with assignments |
| chiphuyen/machine-learning-systems-design | 10.7k | 2023-04 | ML system design booklet |
| matheusfacure/python-causality-handbook | 3.5k | 2026-10 | "Causal Inference for the Brave and True" |

## 3. Patterns

1. **Re-implementation beats application.** Eight of the top twenty single-author repos re-implement known
   methods from scratch in plain NumPy or PyTorch. The value is pedagogical: short, readable code, with the math
   next to it. Applied Kaggle-style notebooks rarely pass a few thousand stars.
2. **Breadth with a consistent template.** The big from-scratch repos cover 20-40 algorithms, each in the same
   file layout, each with a tiny demo. One deep project gets attention; a well-organised shelf of them gets stars.
3. **Book-like reading order.** Handbook, Bayesian Methods for Hackers, Kalman Filters and ThinkBayes are read
   top to bottom. Numbered chapters, a table of contents in the README and inline figures matter.
4. **Benchmark against the reference library.** The credible from-scratch repos show their implementation
   matches scikit-learn, statsmodels or PyTorch on the same data. That one table is what separates a learning
   exercise from a demonstration of understanding.
5. **Honest, small-scale results.** nanoGPT, micrograd and annotated papers all run on a laptop. Reviewers
   trust reproducible small numbers more than unreproducible large ones.
6. **Maintenance signal.** Repos last pushed in the past year (stas00, trekhleb, rushter, mrdbourke) keep
   climbing; dormant ones plateau. A visible roadmap and periodic commits count.
7. **The most upvoted Kaggle notebooks** (House Prices "Comprehensive data exploration", Titanic
   "Data Science Solutions", "Introduction to Ensembling/Stacking", "Credit Fraud: Dealing with Imbalanced
   Datasets") share one shape: a clear question, careful EDA with figures, a leakage-aware validation scheme, a
   comparison table of models and an ensemble at the end.

## 4. What this portfolio should replicate (as original re-implementations, with credit)

Everything below is to be written from scratch, on public or synthetic data, with each result benchmarked
against a reference library and the inspiring repos credited in a References section. Copying code or text
from the source repos is out of scope.

| Priority | Project | Inspired by | Why it ranks |
|---|---|---|---|
| 1 | **ml-from-scratch**: 12-15 classic algorithms in NumPy (linear/logistic regression, kNN, naive Bayes, decision tree, random forest, gradient boosting, SVM via SMO, k-means, GMM/EM, PCA, t-SNE-lite) each matched against scikit-learn on the same public datasets | ML-From-Scratch 33k, homemade-ml 25k, numpy-ml 16k, MLAlgorithms 11k | Pattern 1, 2, 4 |
| 1 | **autograd-engine**: a micrograd-style scalar/tensor autograd with an MLP trained on it, gradient-checked against PyTorch | micrograd 19k, nn-zero-to-hero 25k | Pattern 1, 4 |
| 1 | **bayesian-methods**: Metropolis-Hastings and a small HMC from scratch, Bayesian A/B testing, hierarchical model, Kalman and particle filters on simulated tracking, compared with PyMC/filterpy numbers where installed | Bayesian Methods for Hackers 28k, Kalman book 19k, ThinkBayes 2k | Pattern 3 |
| 2 | **annotated-papers**: side-by-side implementation and notes for Adam, BatchNorm/LayerNorm, ResNet, VAE, GAN and DDPM diffusion on MNIST/CIFAR-10-small, each with its headline figure | labml annotated 68k | Pattern 1, 3 |
| 2 | **tabular-playbook**: the Kaggle-classic workflow done properly on public OpenML data: House Prices regression with stacking, credit-card fraud with imbalance handling and cost curves, customer churn with calibration and uplift; leakage-aware CV, SHAP-style explanations implemented by hand | top Kaggle notebooks, applied-ml 31k | Pattern 7 |
| 2 | **recsys-from-scratch**: MovieLens-100k with item-kNN, matrix factorisation (SGD and ALS), BPR, and a two-tower model; offline metrics and a popularity-bias analysis | recommenders 22k, implicit 3.8k | Pattern 1, 4 |
| 3 | **experimentation**: A/B test design and analysis on synthetic traffic: power, CUPED variance reduction, sequential tests and peeking, interference | industry blogs (Netflix, Booking, Spotify) | Fills a gap few portfolios cover |
| 3 | **anomaly-detection-bench**: Isolation Forest, LOF, one-class SVM, autoencoder and Deep SVDD on ODDS/ADBench datasets with a results table | ADBench 1k, Deep-SVDD 0.8k | Pattern 4 |

## 5. Sources

- GitHub REST API search: https://docs.github.com/en/rest/search/search
- GitHub topic pages: https://github.com/topics/data-science , https://github.com/topics/machine-learning , https://github.com/topics/deep-learning
- Kaggle notebook study: "Mining the Characteristics of Jupyter Notebooks in Data Science Projects", https://arxiv.org/abs/2304.05325
- Repos cited by name link to `https://github.com/<owner>/<repo>`.
