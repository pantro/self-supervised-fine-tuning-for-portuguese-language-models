# Paper: Reducing Dependence on Labeled Data: A Self-Supervised Fine-Tuning Approach for Low-Resource Language Models

This repository contains the code, datasets, and resources used for the paper **"Reducing Dependence on Labeled Data: A Self-Supervised Fine-Tuning Approach for Low-Resource Language Models"**. This research addresses the challenges of adapting pre-trained language models for specific domains with limited labeled data, proposing a self-supervised fine-tuning approach for the BERTimbau Portuguese language model.

## Abstract

The development of domain-specific language models faces limitations due to the scarcity of labeled data, which is costly and time-consuming to obtain. This challenge is especially relevant in low-resource languages such as Portuguese. To address this, we investigate a self-supervised fine-tuning strategy based on the BERTimbau pre-training protocol, aiming to enhance Language Model generalization without relying on annotated data. Our approach explores different combinations of unfrozen layers and hyperparameters. We evaluate its effectiveness on three sentiment analysis datasets in Portuguese from distinct domains. Results show that unfreezing only the final layer, combined with a suitable learning rate, achieves competitive performance compared to the traditional fine-tuning approach. This demonstrates the method’s viability in low-resource settings and its scalability to larger unlabeled datasets.

## Key Contributions

- Adaptation of the **BERTimbau Base** pre-training protocol to a self-supervised fine-tuning approach for Portuguese language tasks.
- Evaluation of how self-supervised fine-tuning affects downstream performance and generalization using unlabeled domain-specific data.
- Experiments exploring various configurations (e.g., layer unfreezing and learning rate settings) to identify an optimal training regime.
- Insights into how computationally efficient methods can be used to achieve significant performance improvements, particularly for users with limited resources.


## Repository Structure
- **`data/`**: Includes the preprocessed datasets used in this research (instructions for downloading external datasets are provided).
- **`notebooks/`**: Jupyter notebooks with exploratory data analysis and key visualizations.
  - **`experiment_LRxLAYERS_B2W/`**: Contains notebooks related to exploratory data analysis in B2W..
    - `code_selfsupervised_BERTimabauBase-B2W_1lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-B2W_1lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-B2W_1lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-B2W_2lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-B2W_2lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-B2W_2lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-B2W_4lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-B2W_4lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-B2W_4lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-B2W_12lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-B2W_12lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-B2W_12lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-6.
    - `MultiClass_BERTimbauBase_B2W.ipynb`: Multiclass downstream task with original BERTimbau only.
    - `MultiClass_SSL-BERTimbauBase_B2W_1layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_B2W_2layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_B2W_4layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_B2W_12layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-5.
  
  - **`experiment_LRxLAYERS_UTLCapps/`**: Contains notebooks related to exploratory data analysis in UTLCapps.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_1lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_1lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_1lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_2lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_2lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_2lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_4lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_4lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_4lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_12lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_12lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCapps_12lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-6.
    - `MultiClass_BERTimbauBase_UTLCapps.ipynb`: Multiclass downstream task with original BERTimbau only.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_1layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_1layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_1layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_2layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_2layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_2layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_4layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_4layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_4layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_12layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_12layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCapps_12layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-6.
    
  - **`experiment_LRxLAYERS_UTLCmovies/`**: Contains notebooks related to exploratory data analysis in UTLCmovies.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_1lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_1lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_1lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_2lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_2lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_2lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 2 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_4lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_4lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_4lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 4 last layer and using LR equal to 1e-6.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_12lastlayersdefreeze-LR1e4.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-4.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_12lastlayersdefreeze-LR1e5.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-5.
    - `code_selfsupervised_BERTimabauBase-UTLCmovies_12lastlayersdefreeze-LR1e6.ipynb`: Self-supervised learning by unfreezing only the 12 last layer and using LR equal to 1e-6.
    - `MultiClass_BERTimbauBase_UTLCmovies.ipynb`: Multiclass downstream task with original BERTimbau only.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_1layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_1layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_1layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_2layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_2layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_2layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 2 last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_4layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_4layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_4layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 4 last layer and with the LR equal to 1e-6.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_12layers_1e4.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-4.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_12layers_1e5.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-5.
    - `MultiClass_SSL-BERTimbauBase_UTLCmovies_12layers_1e6.ipynb`: Multiclass downstream task with the model obtained from self-supervised learning by unfreezing only the 12 last layer and with the LR equal to 1e-6.
    