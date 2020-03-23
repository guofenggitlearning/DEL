# [DEL: Deep Embedding Learning for Efficient Image Segmentation](https://mmcheng.net/del/)

### Introduction

Image segmentation has been explored for many years and still remains a crucial vision problem. Some efficient or accurate segmentation algorithms have been widely used in many vision applications. However, it is difficult to design a both efficient and accurate image segmenter. In this paper, we propose a novel method called DEL (deep embedding learning) which can efficiently transform superpixels into image segmentation. Starting with the SLIC superpixels, we train a fully convolutional network to learn the feature embedding space for each superpixel. The learned feature embedding corresponds to a similarity measure that measures the similarity between two adjacent superpixels. With the deep similarities, we can directly merge the superpixels into large segments. The evaluation results on BSDS500 and PASCAL Context demonstrate that our approach achieves a good trade-off between efficiency and effectiveness. Specifically, our DEL algorithm can achieve comparable segments when compared with MCG but is much faster than it, _i.e._ 11.4fps _vs._ 0.07fps.

### Citations

If you are using the code/model/data provided here in a publication, please consider citing our paper:

    @conference{liu2018deep,
      title={{DEL}: Deep Embedding Learning for Efficient Image Segmentation},
      author={Yun Liu and Peng-Tao Jiang and Vahan Petrosyan and Shi-Jie Li and Jiawang Bian and Le Zhang and Ming-Ming Cheng},
      booktitle={International Joint Conference on Artificial Intelligence},
      pages={864--870},
      year={2018}
    }
    
    @inproceedings{cheng2016hfs,
      title={{HFS}: Hierarchical feature selection for efficient image segmentation},
      author={Cheng, Ming-Ming and Liu, Yun and Hou, Qibin and Bian, Jiawang and Torr, Philip and Hu, Shi-Min and Tu, Zhuowen},
      booktitle={European Conference on Computer Vision},
      pages={867--882},
      year={2016},
      organization={Springer}
    }
    
### Pretrained models

DEL models for BSDS500 dataset is available: [CPU SLIC](https://1drv.ms/u/s!AtAJxn0z15QehA30g1rtRGwMBCBe) and [GPU SLIC](https://1drv.ms/u/s!AtAJxn0z15QehA9KBDV6fXV3BHpw).

DEL models for PASCAL Context dataset is available: [CPU SLIC](https://1drv.ms/u/s!AtAJxn0z15QehA5NT2sESAsOxMjV) and [GPU SLIC](https://1drv.ms/u/s!AtAJxn0z15QehBANSy4I7HeEmTc1).

The initialization model pretrained on SBD dataset is available [here](https://1drv.ms/u/s!AtAJxn0z15QehBHWphkXlazDzmG_).

The test data for BSDS500 and PASCAL Context datasets is available [here](https://1drv.ms/u/s!AtAJxn0z15QehBJ0UQsNgAEORlsT).

### Training 

The training data of BSDS500 dataset can be found [here](https://1drv.ms/u/s!AtAJxn0z15QehBRUdGCzWZq9AN59). In the provided data, the CPU SLIC superpixels can be generated by the code [here](https://ivrl.epfl.ch/research/superpixels). The GPU SLIC superpixels can be generated by the code [here](http://www.robots.ox.ac.uk/~victor/gslicr/). 

**Note** that these superpixels are indexed from 0 and stored in png images with 16 bits. Each image in the folder of sort_groundTruth is one of ground truth segmentation, which has most regions (8 bits).
