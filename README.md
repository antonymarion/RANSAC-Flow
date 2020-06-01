# Github page :

Results on the following cases:

  - Mer de glace
  - Notre Dame
  - Auvers sur Oise
  - Jocondes

https://antonymarion.github.io/fit_and_compare/?object=jocondes

# RANSAC-Flow
Pytorch implementation of Paper "RANSAC-Flow: generic two-stageimage alignment"

<!---
[[PDF(TODO)]]() [[Project webpage]]() [[Slides (TODO)]]() [[Demo]](https://www.youtube.com/watch?v=_18x4x4vcSY&feature=youtu.be)

-->

[[PDF]](http://imagine.enpc.fr/~shenx/RANSAC-Flow/RANSAC_Flow.pdf) [[Project webpage]](http://imagine.enpc.fr/~shenx/RANSAC-Flow/) [[Demo]](http://imagine.enpc.fr/~shenx/RANSAC-Flow/img/demo_ransac_flow.mp4) [[Demo YouTube]](https://youtu.be/ltZpqRtuA6A)



<p align="center">
<img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/overview.jpg" width="800px" alt="teaser">
</p>

If our project is helpful for your research, please consider citing : 
``` 
@inproceedings{shen2020ransac,
          title={RANSAC-Flow: generic two-stage image alignment},
          author={Shen, Xi and Darmon, Francois and Efros, Alexei A and Aubry, Mathieu},
          booktitle={Arxiv},
          year={2020}
        }
```
## Table of Content
* [1. Visual Results](#1-visual-results)
* [2. Installation](#2-installation)
* [3. Quick Start](#3-quick-start)
    * [Notebook of demo](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/quick_start/demo.ipynb)
* [4. Train](#4-train)
    * [Notebook to generate training pairs](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/generate_coarse_aligned_pair.ipynb)
* [5. Evaluation](#5-evaluation)

## 1. Visual Results

### 1.1. Aligning Artworks (More results can be found in our [project webpage](http://imagine.enpc.fr/~shenx/RANSAC-Flow/))

<p align="center">
<table>
  <tr>
    <th colspan="2">Input</th>
    <th colspan="2">Our Fine Alignment</th>
  </tr>
  <tr>
    <th>Animation</th>
    <th>Avg</th>
    <th>Animation</th>
    <th>Avg</th>
  </tr>
  
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/TARGET0.gif" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/avg_target0.jpg" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/FINE0.gif" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/avg_fine0.jpg" width="200px" alt="gif"></td>
  </tr>
  
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/TARGET1.gif" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/avg_target1.jpg" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/FINE1.gif" width="200px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/avg_fine1.jpg" width="200px" alt="gif"></td>
  </tr>
</table>
</p>

### 1.2. 3D recontruction 2-view geometry estimation (More results can be found in our [project webpage](http://imagine.enpc.fr/~shenx/RANSAC-Flow/))

<p align="center">
<table>

  <tr>
    <th>Source</th>
    <th>Target</th>
    <th>3D Reconstruction</th>
  </tr>
  
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_1_1.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_1_2.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_1_3.gif" width="250px" alt="gif"></td>
  </tr>
  
  <!--
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_2_1.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_2_2.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/3D_2_3.gif" width="250px" alt="gif"></td>
  </tr>
  -->
</table>
</p>


### 1.3. Texture transfer

<p align="center">
<table>

  <tr>
    <th>Source</th>
    <th>Target</th>
    <th>Texture Transfer</th>
  </tr>
  
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_s0.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_t0.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_st0.jpg" width="250px" alt="gif"></td>
  </tr>
  
  <!--
  <tr>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_s1.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_t1.jpg" width="250px" alt="gif"></td>
    <td><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/texture_transfer_st1.jpg" width="250px" alt="gif"></td>
  </tr>
  -->
</table>
</p>

**Other results (such as: aligning duplicated artworks, optical flow, localization etc.) can be seen in [our paper](http://imagine.enpc.fr/~shenx/RANSAC-Flow/RANSAC_Flow.pdf).**
 
## 2. Installation

### 2.1. Dependencies

Install Pytorch adapted to your CUDA version : 

* [Pytorch 1.2.0](https://pytorch.org/get-started/previous-versions/#linux-and-windows-1) 
* [Torchvision 0.4.0](https://pytorch.org/get-started/previous-versions/#linux-and-windows-1)

Other dependencies (tqdm, visdom, pandas, kornia, opencv-python) : 
``` Bash
bash requirement.sh
```

### 2.2. Pre-trained models 

Quick download : 

``` Bash
cd model/pretrained
bash download_model.sh
```

For more details of the pre-trained models, see [here](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/model/pretrained) 

### 2.3. Datasets


Download the results of [ArtMiner](http://imagine.enpc.fr/~shenx/ArtMiner/) : 

``` Bash
cd data/
bash Brueghel_detail.sh # Brueghel detail dataset (208M) : visual results, aligning groups of details
```

Download our training data [here (~9G)](https://drive.google.com/file/d/1SikcOvCJ-zznOyCRJCTGtpKtTp01Jx5g/view?usp=sharing). It includes the validation and test data as well.

## 3. Quick Start

A quick start guide of how to use our code is available in [demo.ipynb](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/quick_start/demo.ipynb)

<p align="center">
<a href="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/quick_start/demo.ipynb"><img src="https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/img/notebook.png" width="400px" alt="notebook"></a>
</p>


## 4. Train

### 4.1. Generating training pairs 

To run the training, we need pairs that are coarsely aligned. We provide a [notebook](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/generate_coarse_aligned_pair.ipynb) to show how to generate the training pairs. Note that, we also provide our training pairs in [here](https://drive.google.com/file/d/1SikcOvCJ-zznOyCRJCTGtpKtTp01Jx5g/view?usp=sharing). 



### 4.2. Reproducing the training on MegaDepth 

The training data need to be downloaded from [here](https://drive.google.com/file/d/1SikcOvCJ-zznOyCRJCTGtpKtTp01Jx5g/view?usp=sharing) and saved into `./data`. The file structure is : 

```
./RANSAC-Flow/data/MegaDepth
├── MegaDepth_Train/
├── MegaDepth_Train_Org/
├── Val/
└── Test/
```

As mentioned in the paper, the model trained on MegaDepth contains the following 3 different stages of training: 

* Stage 1 : we only trained the **reconstruction loss**. You can find the hyper-parameters in [train/stage1.sh](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/stage1.sh). You can run the training of this stage by : 
     
``` Bash
cd train/ 
bash stage1.sh
```

* Stage 2 : in this stage, we train jointly: **reconstruction loss + cycle consistency of the flow**. We started from the model trained in the stage 1. The hyper-parameters are in [train/stage2.sh](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/stage2.sh). You need to change the argument _--resumePth_ to your model path. Once it is done, run: 

``` Bash
cd train/ 
bash stage2.sh
```

* Stage 3 : finally, we trained all the three losses together: **reconstruction loss + cycle consistency of the flow + matchability loss**. We started from the model trained in the stage 2. The hyper-parameters are in [train/stage3.sh](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/stage3.sh). You need to change the argument _--resumePth_ to your model path. Once it is done, run: 

``` Bash
cd train/ 
bash stage3.sh
```

### 4.3. Fine-tuning on your own dataset 

If you want to conduct fine-tuning on your own dataset. It is recommended to start from our MegaDepth trained model. You can see all the arguments of training by : 
 
 ``` Bash
cd train/ 
python train.py --help
```

If you don't need to predict the matchability, you can set the weight of the matchability loss to 0 (_--eta 0_ in the [train.py](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/train.py)), and set your path of images (_--trainImgDir_). Please refer to [train/stage2.sh](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/stage2.sh) for other arguments.


In case of predicting matchability, you need to tune the weight of the matchability loss (argument _--eta_ in the [train.py](https://github.com/XiSHEN0220/RANSAC-Flow/blob/master/train/train.py)) depending on the dataset.


## 5. Evaluation 

The evaluation of different tasks can be seen in the following files: 

* [Hpatches (Dense Alignment)](evaluation/evalHpatch/)

* [KITTI (Optical Flow)](evaluation/evalKITTI/)

* [MegaDepth and RobotCar (Sparse Correspondences)](evaluation/evalCorr/)

* [YFCC (Two-View Geometry Estimation) ](evaluation/evalYFCC/)


















