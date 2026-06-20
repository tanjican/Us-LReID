# AHN: Unsupervised Lifelong Person Re-Identification via Affinity Harmonization

Official PyTorch implementation of our ACM TOMM paper:

**Unsupervised Lifelong Person Re-Identification via Affinity Harmonization**
Jican Tan, Jinjia Peng, Songyu Zhang, Zhen Wang, Huibing Wang
*ACM Transactions on Multimedia Computing, Communications, and Applications, 2026*

[[Paper](https://dl.acm.org/doi/10.1145/3779124)]

---

## Introduction

This repository provides the official implementation of **AHN**, an unsupervised lifelong person re-identification method.
AHN aims to continuously learn from unlabeled person ReID domains while alleviating catastrophic forgetting.

---

## Requirements

```bash
conda create -n env_ucr python=3.6
source activate env_ucr 
pip install numpy torch==1.4.0 torchvision==0.5.0 h5py six Pillow scipy sklearn metric-learn tqdm faiss-gpu==1.6.3
python setup.py develop
```

---

## Dataset Preparation

Please organize the datasets as follows:

```bash
data/
├── market1501/
├── cuhk_sysu/
├── dukemtmc/
├── msmt17/
├── cuhk03/
├── viper/
├── prid/
├── grid/
├── ilids/
├── cuhk01/
├── cuhk02/
└── sensereid/
```

Modify the dataset paths in the corresponding configuration files if necessary.

---

## Training

```bash
sh unsupervised_lifelong.sh
```



---

## Evaluation

```bash
python examples/test.py --init examples/logs/step3.pth.tar
```

---

## Citation

If you find this work useful, please consider citing our paper:

```bibtex
@article{tan2026unsupervised,
  title={Unsupervised Lifelong Person Re-Identification via Affinity Harmonization},
  author={Tan, Jican and Peng, Jinjia and Zhang, Songyu and Wang, Zhen and Wang, Huibing},
  journal={ACM Transactions on Multimedia Computing, Communications, and Applications},
  volume={22},
  number={4},
  year={2026},
  publisher={ACM},
  doi={10.1145/3779124}
}
```

---










