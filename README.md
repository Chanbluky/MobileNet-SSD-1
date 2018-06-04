# MobileNet-SSD
MobileNetV2 and MobileNetV2-SSD For Object Detection   

## File Lists  

MobileNetV2_GC_train_val.txt: train_val prototxt for imagenet, In this version, Depthwise Convolution is implemented by caffe group convolution.   
MobileNetV2_GC_deploy.prototxt: deploy file for MobileNetV2  
MobileNetV2_GC_solver.prototxt: training config file    


MobileNetV2_DW_train_val.txt: train_val prototxt for imagenet, In this version, Depthwise Convolution is implemented by DepthwiseConvolution layer.   
MobileNetV2_DW_deploy.prototxt: deploy file for MobileNetV2  
MobileNetV2_DW_solver.prototxt: training config file  


## DepthwiseConvolution  
The implementation of depthwise convolution is from [yonghenglh6/DepthwiseConvolution
](https://github.com/yonghenglh6/DepthwiseConvolution)  

Source code is in src folder. And by the way, during training, **DepthwiseConvolution is faster than Group Convolution about most 15 times**.

## Results on ImageNet-100
Because of the limitation of my GPUs, I only use 100 classes from imagenet for train. The train data is selected randomly

| Name | accuracy/top1 | accuracy/top5 | inference time | model size |Depthwise conv type |
| - | :-: | :-: | :-: | :-: | -: |
| MobileNetV2 | 85% | 90% | | |group convolution |
| MobileNetV2_dw | 67.6% | 89.3% | | | depthwise convolution |


## Detection Result of MobileNet-SSD
