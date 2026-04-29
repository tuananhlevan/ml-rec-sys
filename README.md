# RecSys-Index

A curated, lightweight directory of high-performance recommendation system implementations. This repository serves as a navigator for exploring various architectures, from classic matrix factorization to modern graph-based models.

## 📌 How to Use This Repo
This repository does not host the source code locally to ensure a minimal footprint. Instead, it provides vetted links to high-quality implementations. 

**To access the code, please click the links in the table below to be redirected to the respective source repositories.**

---

## 🛠 Model Implementations

| Model | Category | Description | Source Link |
| :--- | :--- | :--- | :--- |
| **BPR-MF** | Classic ML | Bayesian Personalized Ranking for implicit feedback. | [View Implementation](https://github.com/guoyang9/BPR-pytorch) |
| **NCF** | Deep Learning | Neural Collaborative Filtering (GMF + MLP). | [View Implementation](https://github.com/yihong-chen/neural-collaborative-filtering) |
| **Wide & Deep** | Hybrid | Jointly trained wide and deep models for ranking. | [View Implementation](https://github.com/jrjohansson/wide-and-deep-learning) |
| **SASRec** | Sequential | Self-Attentive Sequential Recommendation (Transformer-based). | [View Implementation](https://github.com/pmixer/SASRec.pytorch) |
| **LightGCN** | Graph-based | Simplified Graph Convolutional Networks for RecSys. | [View Implementation](https://github.com/gusye1234/LightGCN-PyTorch) |
| **Mult-VAE** | Generative | Variational Autoencoders for Collaborative Filtering. | [View Implementation](https://github.com/dawenliou/VAE_CF) |
| **DeepFM** | Hybrid | Factorization-Machine based Neural Network. | [View Implementation](https://github.com/ChenglongChen/tensorflow-DeepFM) |

---

## 📊 Evaluation Metrics

All linked implementations focus on top-$K$ ranking performance:
* **Precision@K**: The proportion of recommended items in the top-$K$ that are relevant.
* **Recall@K**: The proportion of all relevant items that are captured in the top-$K$ list.
* **MRR@K (Mean Reciprocal Rank)**: Measures where the first relevant item appears in the top-$K$ list, rewarding higher placements.
* **NDCG@K (Normalized Discounted Cumulative Gain)**: Evaluates the ranking quality by accounting for the specific position of all relevant items.