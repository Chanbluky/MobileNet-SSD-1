# MobileNet-SSD
MobileNetV2 and MobileNetV2-SSD For Object Detection   

## File Lists  

>MobileNetV2_train_val.txt: train_val prototxt for imagenet, In this version, Depthwise Convolution is implemented by caffe group convolution.  

>MobileNetV2_deploy.prototxt: deploy file for MobileNetV2

>MobileNetV2_deploy.prototxt: training config file  


## Results on ImageNet-100
**Because of the limitation of my GPUs, I only use 100 classes from imagenet for train. The train data is selected randomly**  

| Name | accuracy/top1 | accuracy/top5 | inference time | model size |Depthwise conv type |
| - | :-: | :-: | :-: | :-: | -: |
| MobileNetV2 | 85% | 90% | | |group convolution |
| MobileNetV2_dw | 87% | 90% | | | depthwise convolution |


## Detection Result of MobileNet-SSD