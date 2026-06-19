# RecSys-Index

A curated, lightweight directory of high-performance recommendation system implementations. This repository serves as a navigator for exploring various architectures, from classic matrix factorization to modern graph-based and sequential models.

## How to Use This Repo
This repository does not host the source code locally to ensure a minimal footprint. Instead, it provides vetted links to high-quality implementations. 

**To access the code, please click the links in the table below to be redirected to the respective source repositories.**

---

## Model Implementations

| Model | Category | Description | Source Link |
| :---: | :---: | :---: | :---: |
| **Matrix Factorization (MF)** | Classic ML | Classical collaborative filtering decomposing the user-item interaction matrix into low-rank latent factors. | [View Implementation](https://github.com/DuyTung24/Movie-Recommendation-System-on-different-aglos/tree/main/Matrix%20Factorization)|
| **Memory-Based CF** | Classic ML | Memory-based collaborative filtering identifying similar users to recommend items preferred by like-minded peers. | [View Implementation](https://github.com/DuyTung24/Movie-Recommendation-System-on-different-aglos/tree/main/Memory_based%20Filtering) |
| **Content-Based CF** | Classic ML | Traditional neighborhood-based collaborative filtering using matrix-wide similarity metrics to find correlations. | [View Implementation](https://github.com/DuyTung24/Movie-Recommendation-System-on-different-aglos/tree/main/Content_based%20Filtering) |
| **Hybrid (Item & Content CF)** | Hybrid | Blends neighborhood Item-Based Collaborative Filtering with Content-Based metadata features to balance interaction signals with item characteristics. | [View Implementation](https://github.com/quangpt22/Hybrid-Recommender-System---ML) |
| **NCF (Neural CF)** | Deep Learning | Deep learning framework that replaces the inner product in matrix factorization with a neural network architecture capable of learning non-linear user-item interactions. | [View Implementation](https://github.com/DuyTung24/Movie-Recommendation-System-on-different-aglos/tree/main/NCF%20Movie%20Recommendation) |
| **Two-Tower Retrieval** | Deep Learning | Dual-encoder architecture separating user and item feature representations for efficient candidate generation. | [View Implementation](https://github.com/sunnycloudhust/TwoTowerRetrival_RecommenderSystem) |
| **LightGCN** | Graph-based | Simplified Graph Convolutional Networks optimized specifically for collaborative filtering by removing feature transformations and non-linearities. | [View Implementation](https://github.com/tuananhlevan/lightgcn) |
| **SASRec** | Sequential | Self-Attentive Sequential Recommendation using a Transformer-based architecture to capture long-term and short-term user dynamics. | [View Implementation](https://github.com/CRedRiver/ml_sasrec) |

---

## Evaluation Metrics

All linked implementations focus on top-$K$ ranking performance:
* **Precision@K**: The proportion of recommended items in the top-$K$ that are relevant.
* **Recall@K**: The proportion of all relevant items that are captured in the top-$K$ list.
* **MRR@K (Mean Reciprocal Rank)**: Measures where the first relevant item appears in the top-$K$ list, rewarding higher placements.
* **NDCG@K (Normalized Discounted Cumulative Gain)**: Evaluates the ranking quality by accounting for the specific position of all relevant items.
* **HitRate@K**: Measures the proportion of testing instances where the ground-truth item is included in the top-$K$ recommendation list.

## Benchmark Results

| Random | NDCG@20 | Recall@20 | MRR@20 | Precision@20 |
| :---: | :---: | :---: | :---: | :---: |
| **Content-based Filtering** | 0.0049 ± 0.0001 | 0.0116 ± 0.0002 | 0.0030 ± 0.0001 | 0.0006 ± 0.0000 |
| **Hybrid Filtering** | ... | ... | ... | ... |
| **Memory-based Filtering** | 0.0363 ± 0.0008 | 0.0148 ± 0.0007 | 0.1014 ± 0.0018 | 0.0274 ± 0.0012 |
| **Matrix Factorization** | 0.2509 ± 0.0008 | 0.5100 ± 0.0008 | 0.2971 ± 0.0007 | 0.2028 ± 0.0006 |
| **Neural MF** | 0.3264 ± 0.0006 | 0.2268 ± 0.0006 | 0.5734 ± 0.0006 | 0.2460 ± 0.0006 |
| **Two Towers** | 0.0177 ± 0.0007 | 0.0490 ± 0.0019 | 0.0093 ± 0.0004 | 0.0024 ± 0.0001 |
|  **LightGCN** | 0.3578 ± 0.0011 | 0.2604 ± 0.0012 | 0.6077 ± 0.0022 | 0.2630 ± 0.0009 |

| Leave-one-out | NDCG@10 | HitRate@10 | MRR@10 |
| :---: | :---: | :---: | :---: |
| **Content-based Filtering** | 0.0054 | 0.0108 | 0.0037 |
| **Hybrid Filtering** | ... | ... | ... |
| **Memory-based Filtering** | 0.0020 | 0.0051 | 0.0011 |
| **Matrix Factorization** | 0.0045 ± 0.0001 | 0.0090 ± 0.0000 | 0.0090 ± 0.0002 |
| **Neural MF** | 0.0148 ± 0.0004 | 0.0329 ± 0.0010 | 0.0094 ± 0.0003 |
| **Two Towers** | 0.0980 ± 0.0024 | 0.1888 ± 0.0026 | 0.0706 ± 0.0025 |
| **LightGCN** | 0.0438 ± 0.0003 | 0.0899 ± 0.0013 | 0.0302 ± 0.0004 |
|  **SasRec** | 0.1932 ± 0.0019 | 0.3285 ± 0.0030 | 0.1518 ± 0.0016 |
