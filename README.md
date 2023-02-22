# Differentially Private Data Distillation Federated Learning

## Literature Review

* [Federated Learning via Synthetic Data](https://arxiv.org/pdf/2008.04489.pdf)
* [Meta Knowledge Condensation for Federated Learning](https://arxiv.org/pdf/2209.14851.pdf)
* [Federated Learning via Decentralized Dataset Distillation in Resource-Constrained Edge Environments](https://arxiv.org/pdf/2208.11311.pdf)
* [FedSynth: Gradient Compression via Synthetic Data in Federated Learning](https://arxiv.org/pdf/2204.01273.pdf)
* [Distilled One-Shot Federated Learning](https://arxiv.org/pdf/2009.07999.pdf)
* [DYNAFED: Tackling Client Data Heterogeneity with Global Dynamics](https://arxiv.org/pdf/2211.10878.pdf)

### Distribution Matching
* [FedDM: Iterative Distribution Matching for Communication-Efficient Federated Learning](https://arxiv.org/pdf/2207.09653.pdf)
  * DP via clipped gradient and GM 

### Data-Distillation
* [Private Set Generation with Discriminative Information](https://arxiv.org/pdf/2211.04446.pdf)
  * Class-agnostic distillation and DP
  * one round distillation

### Data-Distillation for FL
* [An experimental study on private aggregation of teacher ensemble learning for end-to-end speech recognition](https://assets.amazon.science/7c/58/a63db89c4c3c8b0a9a4ec6f51180/an-experimental-study-on-private-aggregation-of-teacher-ensemble-learning-for-end-to-end-speech-recognition.pdf)
  * Knowledge-Distillation and Ensemble
  * Average gradients + DP > DP-SGD?
* [Fed-GLOSS-DP: Federated, Global Learning using Synthetic Sets with Record Level Differential Privacy](https://arxiv.org/pdf/2302.01068.pdf)
  * Class-agnostic distillation and record-level DP
  * multiple-round FL
  * privacy-preserving learning that uses synthetic data to train federated models
  * simulate the global optimization by transmitting a small set of synthetic samples that reflect the local loss landscapes
  * (Eq. 13) w_k that is sufficiently close to the initial point of the local update, NTK condition, no change + always in the right direction => novelty
    * NTK network doesn't need to be shared / has to be uniform?
    
  Questions
    * the weights are synchronized/ communicated between client and central. A: no DP leak as its sanitized
    * minimizing the distance between gradients => NTK? MMD
