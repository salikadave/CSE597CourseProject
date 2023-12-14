# CSE597 Course Project
CSE 597 Course Project

**Paper:** COGMEN: COntextualized GNN based Multimodal Emotion recognitioN

**Paper Link:** [COGMEN](https://paperswithcode.com/paper/cogmen-contextualized-gnn-based-multimodal)

** Dataset: ** [IEMOCAP (The Interactive Emotional Dyadic Motion Capture (IEMOCAP) Database)](https://paperswithcode.com/dataset/iemocap)

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

### Summary of Results

| Experiment | Modality | Epochs | Optimizer | Window Past | Window Future | F1 Score |
| ----------- | ----------- |----------- |----------- |----------- |----------- |----------- |
| Varying Optimizer | atv | 10 | sgd | 4 | 4  | 0.14271 |
| Varying Modalites | a | 50 | adam | 4 | 4  | 0.6022 |
| Varying Modalites | t | 50 | adam | 10 | 10  | 0.7254 |
| Varying Modalites | v | 50 | adam | 10 | 10  | 0.4411 |
| Varying Modalites | av | 50 | adam | 10 | 10  | 0.6237 |
| Varying Modalites | tv | 50 | adam | 10 | 10  | 0.7583 |
| Varying Modalites | at | 50 | adam | 10 | 10  | 0.8223 |
