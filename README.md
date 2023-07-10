# SurfelNeRF: Neural Surfel Radiance Fields for Online Photorealistic Reconstruction of Indoor Scenes

[Project Sites](https://gymat.github.io/SurfelNeRF-web/)
 | [Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Gao_SurfelNeRF_Neural_Surfel_Radiance_Fields_for_Online_Photorealistic_Reconstruction_of_CVPR_2023_paper.pdf)

This is an unofficial version of SurfelNeRF.


## Installation

### Requirements
All the codes are tested in the following environment:
* Python 3.8+
* PyTorch 1.6 or higher (tested on PyTorch 1.6)
* CUDA 10.2 or higher (tested on CUDA 10.2)

### Install
Install the dependent libraries as follows:

* Install the dependent python libraries (recommend to use conda):
```
conda create -n new python=3.8
source activate new
conda install -c pytorch pytorch=1.6.0 torchvision cudatoolkit=10.2
conda install -c fvcore -c iopath -c conda-forge fvcore iopath
conda install -c pytorch3d pytorch3d
pip install matplotlib scikit-image lpips opencv-python inplace_abn open3d
```

* Then compile the dependent libraries:
```
sh build.sh
```


## Quick Start

### Data preparation

We provide the test data and an inference code for 8 test scenes on ScanNet without per-scene optimization. You can direct download
the preprocessed data provided by us at here: [Google-Drive](). To speed up inference and training, we preprocess the raw data to 
obtain the corresponding world 3D coordinates as surfels initialization for each pixel based on estimated depth. 
The layout of data should look like:
```
SurfelNeRF
├── datasets
│   ├── export_Scannet_test
    │   │──scene0000_01
    │   │   │──color
    │   │   │──depth
    │   │   │──pose
    │   │   │──intrinsic
    ├── export_Scannet_train
```

### Download pre-trained checkpoint

We trained 

### Run inference code


## Train SurfelNeRF

### Data prepration





## Acknowledgement
Our repo is mainly developed based on [PointNeRF](https://github.com/Xharlie/pointnerf), [NeRFingMVS](https://github.com/weiyithu/NerfingMVS), 
[MVSNeRF](https://github.com/apchenstu/mvsnerf), and [DSS](https://github.com/yifita/DSS). Thanks for their great and excellent works again!


Please also consider citing the corresponding papers.


## Contact
If you have any questions, feel free to contact me, Yiming Gao (gaoym9 AT mail3 dot sysu dot edu dot cn).


## Reference
If you find our work interesting, please cite our paper.

```
@inproceedings{gao2023surfelnerf,
  title={SurfelNeRF: Neural Surfel Radiance Fields for Online Photorealistic Reconstruction of Indoor Scenes},
  author={Gao, Yiming and Cao, Yan-Pei and Shan, Ying},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={108--118},
  year={2023}
}
```

## LICENSE
The repo is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 2.0, and is restricted to academic use only.