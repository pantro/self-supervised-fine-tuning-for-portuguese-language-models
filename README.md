# Master's dissertation: Analysis of self-supervised approaches for fine-tuning language models for Portuguese tasks

This repository contains the code, datasets, and resources used for the doctoral dissertation **"Analysis of self-supervised approaches for fine-tuning language models for Portuguese tasks"**. This research addresses the challenges of adapting pre-trained language models for specific domains with limited labeled data, proposing a self-supervised fine-tuning approach for the BERTimbau Portuguese language model.

## Abstract

Organizations often face the limitation of having a small amount of labeled data to calibrate and refine their language models (LMs) in specific contexts. This scarcity of annotated data presents a significant challenge, as the quality and quantity of data are critical to the performance and generalization of the models. Furthermore, the acquisition or creation of labeled data is often expensive and time-consuming, creating a barrier to implementing tailored machine learning solutions.

In the literature, similar challenges have been addressed through self-supervised fine-tuning using various pre-training approaches. However, to our knowledge, no detailed description or evaluation of such training protocols existed for LMs in Portuguese. 

This dissertation proposes an adaptation of the BERTimbau pre-training protocol to a self-supervised fine-tuning procedure. We evaluated this procedure's impact on generalization and downstream tasks using unlabeled data. Experiments were conducted on three datasets from different domains, testing various configurations by unfreezing different layers of the model and using diverse learning rate settings. The results, focused on sentiment analysis as a downstream task, revealed that unfreezing only the last layer already yields good results. This enables users with limited computational resources to achieve excellent outcomes. Additionally, the effectiveness of self-supervised fine-tuning on larger datasets was highlighted, suggesting its potential for future research with more advanced pre-trained LMs.

## Research Questions

This research aims to answer the following questions:

1. **RQ 1**: How to adapt the pretraining protocol of BERTimbau for a self-supervised fine-tuning procedure on that model?
2. **RQ 2**: How does using unlabeled data in a specific domain in the proposed self-supervised fine-tuning approach impact BERTimbau's downstream performance and its generalization ability?
3. **RQ 3**: In which scenarios (e.g., data availability, type of domain) is it suitable to use that self-supervised fine-tuning approach?

## Key Contributions

- Adaptation of the **BERTimbau** pre-training protocol to a self-supervised fine-tuning approach for Portuguese language tasks.
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
    

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/pantro/self-supervised-fine-tuning-for-portuguese-language-models.git
   cd self-supervised-fine-tuning-for-portuguese-language-models
