# Train CIFAR10 with PyTorch

I'm playing with [PyTorch](http://pytorch.org/) on the CIFAR10 dataset.

## Prerequisites
- Python 3.6+
- PyTorch 1.0+

## Training
```
# Start training with: 
python main.py

# You can manually resume the training with: 
python main.py --resume --lr=0.01
```

## Accuracy
| Model             | Acc.        |
| ----------------- | ----------- |
| [VGG16](https://arxiv.org/abs/1409.1556)              | 92.64%      |
| [ResNet18](https://arxiv.org/abs/1512.03385)          | 93.02%      |
| [ResNet50](https://arxiv.org/abs/1512.03385)          | 93.62%      |
| [ResNet101](https://arxiv.org/abs/1512.03385)         | 93.75%      |
| [RegNetX_200MF](https://arxiv.org/abs/2003.13678)     | 94.24%      |
| [RegNetY_400MF](https://arxiv.org/abs/2003.13678)     | 94.29%      |
| [MobileNetV2](https://arxiv.org/abs/1801.04381)       | 94.43%      |
| [ResNeXt29(32x4d)](https://arxiv.org/abs/1611.05431)  | 94.73%      |
| [ResNeXt29(2x64d)](https://arxiv.org/abs/1611.05431)  | 94.82%      |
| [SimpleDLA](https://arxiv.org/abs/1707.064)           | 94.89%      |
| [DenseNet121](https://arxiv.org/abs/1608.06993)       | 95.04%      |
| [PreActResNet18](https://arxiv.org/abs/1603.05027)    | 95.11%      |
| [DPN92](https://arxiv.org/abs/1707.01629)             | 95.16%      |
| [DLA](https://arxiv.org/pdf/1707.06484.pdf)           | 95.47%      |

# You can modify the code by annotating, we have the folllowing models in our project with corresponding annotation:
```

All the structures in our project report can be reproduced by properly adjustifying the annotations.We only used restnet.py in the Model file.

```

Please re-annotating resnet.py in directory /models when testing with different models:
```

Testing different models by changing the code at line 146-148 in main.py
    # net = my_ResNet0_0()
    net = my_ResNet1_0()
    # net = my_ResNet2_0()

```
1.my_ResNet0
Please use class "my_ResNet0" and corresponding defination my_ResNet0_0 with block structure in our report.

2.my_ResNet1
Please use class "my_ResNet0" and corresponding defination my_ResNet0_0 with block structure in our report.

3.my_ResNet2
Please use class "my_ResNet0" and corresponding defination my_ResNet0_0 with block structure in our report.

4.my_ResNet3
Please use class "BasicBlock1" and "my_ResNet1" and corresponding defination my_ResNet1_0 with block structure in our report.

5.my_ResNet4
Please use class "BasicBlock1" and "my_ResNet1" and corresponding defination my_ResNet1_0 with block structure in our report.

6.my_ResNet1-C my_ResNet2-C my_ResNet3-C 
All you need to do is re-annotate the code in line 107 in main.py:
"transform_train.transforms.append(Cutout(1, 8))"
With this augmentation, all structure from my_ResNet0 to my_ResNet5 can be tested.
