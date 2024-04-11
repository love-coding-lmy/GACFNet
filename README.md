# GACFNet
Our code will be publicly available after the paper is published
# GACFNet:A Global Attention Cross-Level Feature Fusion Network for Aerial Image Object Detection

## Introduction

Real-time object detection in aerial imagery is a challenging task, primarily due to the presence of small and densely-packed features, accompanied by signiffcant scale variations. Previous methods have addressed these issues by employing fusion structures similar to Feature Pyramid Networks (FPN). However, these fusion structures overlook the complementary relationship between feature information from non-adjacent layers. To tackle this, we propose a global attention cross-layer feature fusion network (GACFNet). Firstly, we have devised a global attention cross-layer feature fusion module, which integrates features of varying sizes to gather global information and uses an attention mechanism to highlight foreground features in the global feature map. Additionally, we connect the global attention feature map with other layers to establish correlations between non-adjacent layers. Secondly, a large-kernel separable pooling pyramid fusion (LKSPPF) module is proposed to capture a wider receptive ffeld and enhance context information. Thirdly, in order to better preserve small object information in low-resolution feature maps, the DVC2f module was constructed using deformable convolutions. Finally, given the prevalence of small objects in aerial images, we design the hybrid regression loss function NGIoU loss to improve sample allocation and detection accuracy for small objects, while also accelerating model convergence. The extended experimental results on VisDrone, UAVDT, and DIOR datasets demonstrate that the proposed method signiffcantly enhances the accuracy of aerial image object detection and achieves real-time performance with a speed of 69.9 frames per second. 

<img width="1048" alt="2" src="https://github.com/JSJ515-Group/GACFNet/assets/111633414/819ed035-e637-4b33-9b23-3e6a0bdc2cef">


## Prerequisite

We use Pytorch  1.12.0 , and CUDA 16.0. You can install them with `conda install pytorch=1.12.0 torchvision=0.13.0 cudatoolkit=16.0 -c pytorch` It should also be applicable to other Pytorch and CUDA versions.

Then install other packages by `pip install -r requirements.txt`

## Usage

### Test

If you want to use our weight test, follow these steps:

```python
python val.py
```

Modify the corresponding parameters in the val.py file.

If you want to use our weight train, follow these steps:

```
python train.py
```

In the train.py file, we have provided specific parameters. If you want to train different datasets and models, you can modify the corresponding parameters
