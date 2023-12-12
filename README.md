# CSE597 Course Project
CSE 597 Course Project

**Paper:** COGMEN: COntextualized GNN based Multimodal Emotion recognitioN

**Repository**: [Github](https://github.com/exploration-lab/cogmen)

**Paper Link:** [COGMEN](https://paperswithcode.com/paper/cogmen-contextualized-gnn-based-multimodal)

**Dataset:** [IEMOCAP (The Interactive Emotional Dyadic Motion Capture (IEMOCAP) Database)](https://paperswithcode.com/dataset/iemocap)

Refer `cogmen.ipynb` for training and evaluation results.

Note: Training and evaluation scripts have been executed using Google Colab T4 GPU.

**Training Setting:**

| Parameter     | Value         |
| ------------- |:-------------:|
| Modalities    | atv (Audio+Visual+Textual) |
| Epochs    | 55 |
| Training starting point      | From beginning      |
| Batch Size  | 32      |
| Optimizer  | Adam      |
| Scheduler  | LR      |
| Learning Rate  | 0.0001      |
| Weight decay  | 1e-8      |
| Past Context Window Size  | 5      |
| Future Context Window Size  | 5      |
| Number of speakers  | 2      |
| Hidden size of two layer GCN  | 100      |
| Type of RNN cell  | transformer      |
| Type of positional encoding  | relational      |
| Random Seed  | 24      |
| Embedding Dimensions (a+t+v)  | 100 + 768 + 512      |

    F1 Score: 0.7968544632328719
    Paper Reported F1 Score: 0.84

**Hyperparameter Tuning:**

| Parameter     | Value         |
| ------------- |:-------------:|
| Epochs    | 10 |
| Past Context Window Size  | 4      |
| Future Context Window Size  | 4      |

    F1 Score: 0.7603731563847743
    Paper Reported F1 Score: 0.8671
