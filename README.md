# Mpro-Inhibition Project

The SARS-CoV-2 main protease (Mpro) plays a critical role in the viral replication cycle, making it an attractive drug target for COVID-19 therapies. This project leverages deep learning to identify and evaluate potential Mpro inhibitors. Using the KANO model as a foundation, the repository integrates fine-tuning on custom datasets, enabling the identification of novel candidates with high precision and druglikeness properties. By advancing computational approaches to drug discovery, this project aims to accelerate the development of effective treatments for viral diseases.

## Table of Contents
- [Project Overview](#project-overview)
- [Original Repository Acknowledgment](#original-repository-acknowledgment)
- [Prerequisites](#prerequisites)
- [Usage](#usage)

## Project Overview
This project aims to identify potential inhibitors of SARS-CoV-2 Mpro using advanced machine learning techniques. By fine-tuning the KANO model on a custom dataset of Mpro inhibitors, we hope to improve precision and discover novel drug candidates.

## Original Repository Acknowledgment
This repository is based on the work of Fang, Y., Zhang, Q., Zhang, N., et al. The original repository can be found [here](https://github.com/HICAI-ZJU/KANO). We are grateful for their contributions, which laid the foundation for this project.

### Prerequisites
The prerequisites for running this project are listed in the original [KANO repository](https://github.com/HICAI-ZJU/KANO).

```sh
python          3.7
torch           1.13.1
rdkit           2018.09.3
numpy           1.20.3
gensim          4.2.0
nltk            3.4.5
owl2vec-star    0.2.1
Owlready2       0.37
torch-scatter   2.0.9
```

### Usage
```sh
bash finetune_Mpro.sh  # Fine-tune the pre-trained model to predict Mpro-inhibition probability.
bash finetune_logP.sh  # Fine-tune the pre-trained model to predict logP.
bash finetune_logS.sh  # Fine-tune the pre-trained model to predict logS.
```
#### To make predictions using the fine-tuned regression model, use the following command:
```sh
python get_predict_regression.py --gpu 0 --test_path "${test_path}" --checkpoint_dir "${model_paths}" --preds_path "${output_path}"
```
