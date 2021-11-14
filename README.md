# MSDN

This is anonymous project website of the paper "MSDN: Mutually Semantic Distillation Network for Zero-Shot Learning" submitted to CVPR 2022. This website includes the following materials for testing and checking our results reported in our paper:

1. The trained model
2. The test scripts
3. More visualization of attention maps.

## Preparing Dataset and Model

We provide trained models ([Google Drive](https://drive.google.com/drive/folders/1WK9pm2eX2Rl4rWqXqe_EZiAM8wWB8yqG?usp=sharing)) on three different datasets: [CUB](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html), [SUN](http://cs.brown.edu/~gmpatter/sunattributes.html), [AWA2](http://cvml.ist.ac.at/AwA2/) in the CZSL/GZSL setting. You can download model files as well as corresponding datasets, and organize them as follows: 
```
.
├── saved_model
│   ├── CUB_MSDN_CZSL.pth
│   ├── CUB_MSDN_GZSL.pth
│   ├── SUN_MSDN_CZSL.pth
│   ├── SUN_MSDN_GZSL.pth
│   ├── AWA2_MSDN_CZSL.pth
│   └── AWA2_MSDN_GZSL.pth
├── data
│   ├── CUB/
│   ├── SUN/
│   └── AWA2/
└── ···
```

## Requirements
The code implementation of **TransZero** mainly based on [PyTorch](https://pytorch.org/). All of our experiments run and test in Python 3.8.8. To install all required dependencies:
```
$ pip install -r requirements.txt
```
## Runing
Runing following commands and testing **TransZero** on different dataset:

CUB Dataset: 
```
$ python Test_cub.py     
```
SUN Dataset:
```
$ python Test_sun.py     
```
AWA2 Dataset: 
```
$ python Test_awa2.py     
```

## Results
Results of our released models using various evaluation protocols on three datasets, both in the conventional ZSL (CZSL) and generalized ZSL (GZSL) settings.

| Dataset | Acc(CZSL) | U(GZSL) | S(GZSL) | H(GZSL) |
| :-----: | :-----: | :-----: | :-----: | :-----: |
| CUB | 75.7 | 68.7 | 67.5 | 68.1 |
| SUN | 65.6 | 51.8 | 34.3 | 41.3 |
| AWA2 | 68.1 | 60.8 | 74.6 | 67.0 |

**Note**: All of above results are run on a server with an AMD Ryzen 7 5800X CPU and a NVIDIA RTX A6000 GPU.

## Attention Maps
Visualization of attention maps for the two mutual attention sub-nets. For each group, the first row attention maps are learned by attribute->visual subnet, the second row attention maps are learned by visual->attribute subnet. The scores are the attribute scores. 

![](images/t-v/Acadian_Flycatcher_0008_795599.jpg)
![](images/v-t/Acadian_Flycatcher_0008_795599.jpg)
##
![](images/t-v/American_Goldfinch_0092_32910.jpg)
![](images/v-t/American_Goldfinch_0092_32910.jpg)
##
![](images/t-v/Canada_Warbler_0117_162394.jpg)
![](images/v-t/Canada_Warbler_0117_162394.jpg)
##
![](images/t-v/Elegant_Tern_0085_151091.jpg)
![](images/v-t/Elegant_Tern_0085_151091.jpg)
##
![](images/t-v/European_Goldfinch_0025_794647.jpg)
![](images/v-t/European_Goldfinch_0025_794647.jpg)
##

![](images/t-v/Vesper_Sparrow_0090_125690.jpg)
![](images/v-t/Vesper_Sparrow_0090_125690.jpg)
##
![](images/t-v/Western_Gull_0058_53882.jpg)
![](images/v-t/Western_Gull_0058_53882.jpg)
##
![](images/t-v/White_Throated_Sparrow_0128_128956.jpg)
![](images/v-t/White_Throated_Sparrow_0128_128956.jpg)
##
![](images/t-v/Winter_Wren_0118_189805.jpg)
![](images/v-t/Winter_Wren_0118_189805.jpg)
##
![](images/t-v/Yellow_Breasted_Chat_0044_22106.jpg)
![](images/v-t/Yellow_Breasted_Chat_0044_22106.jpg)
