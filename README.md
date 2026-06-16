# RecSys-Index

A curated, lightweight directory of high-performance recommendation system implementations. This repository serves as a navigator for exploring various architectures, from classic matrix factorization to modern graph-based models.

## How to Use This Repo
This repository does not host the source code locally to ensure a minimal footprint. Instead, it provides vetted links to high-quality implementations. 

**To access the code, please click the links in the table below to be redirected to the respective source repositories.**

---

## Model Implementations

| Model | Category | Description | Source Link |
| :---: | :---: | :---: | :---: |
| **BPR-MF** | Classic ML | Bayesian Personalized Ranking for implicit feedback. | [View Implementation](https://github.com/guoyang9/BPR-pytorch) |
| **NCF** | Deep Learning | Neural Collaborative Filtering (GMF + MLP). | [View Implementation](https://github.com/yihong-chen/neural-collaborative-filtering) |
| **Item + Content Based CF** | Hybrid | Jointly trained wide and deep models for ranking. | [View Implementation](https://github.com/quangpt22/Hybrid-Recommender-System---ML) |
| **SASRec** | Sequential | Self-Attentive Sequential Recommendation (Transformer-based). | [View Implementation](https://github.com/CRedRiver/ml_sasrec) |
| **LightGCN** | Graph-based | Simplified Graph Convolutional Networks for RecSys. | [View Implementation](https://github.com/tuananhlevan/lightgcn) |
| **DeepFM** | Hybrid | Factorization-Machine based Neural Network. | [View Implementation](https://github.com/ChenglongChen/tensorflow-DeepFM) |

---

## Evaluation Metrics

All linked implementations focus on top-$K$ ranking performance:
* **Precision@K**: The proportion of recommended items in the top-$K$ that are relevant.
* **Recall@K**: The proportion of all relevant items that are captured in the top-$K$ list.
* **MRR@K (Mean Reciprocal Rank)**: Measures where the first relevant item appears in the top-$K$ list, rewarding higher placements.
* **NDCG@K (Normalized Discounted Cumulative Gain)**: Evaluates the ranking quality by accounting for the specific position of all relevant items.

## Benchmark Results

| Model | NDCG@20 | Recall@20 | MRR@20 | Precision@20 |
| :---: | :---: | :---: | :---: | :---: |
|  **LightGCN** | 0.3578 ± 0.0011 | 0.2604 ± 0.0012 | 0.6077 ± 0.0022 | 0.2630 ± 0.0009 |

| Model | NDCG@10 | HitRate@10 | MRR@10 |
| :---: | :---: | :---: | :---: |
|  **SasRec** | 0.1464 ± 0.0030 | 0.2680 ± 0.0047 | 0.1097 ± 0.0026 |