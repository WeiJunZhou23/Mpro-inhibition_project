# Mpro-Inhibition Project

This repository is a fork of [KANO](https://github.com/HICAI-ZJU/KANO). It has been adapted and extended for use in research on SARS-CoV-2 main protease (Mpro) inhibitors.

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

### Usage
```bash
bash finetune_Mpro.sh  # Fine-tune the model to predict Mpro-inhibition probability.
bash finetune_logP.sh  # Fine-tune the model to predict logP.
bash finetune_logS.sh  # Fine-tune the model to predict logS.
