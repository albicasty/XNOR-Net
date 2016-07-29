##XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks.

This is the Torch 7.0 implementation of XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks.

### Citation 
```bash
@inproceedings{rastegariECCV16,
    Author = {Mohammad Rastegari and Vicente Ordonez and Joseph Redmon and Ali Farhadi},
    Title = {XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks},
    Booktitle = {ECCV},
    Year = {2016}
}
```

### Requirements
This software is implemented on top of the implementation of [ImageNet-multiGPU](https://github.com/soumith/imagenet-multiGPU.torch) and has all the same requirements.

### Training Binary Weight Network

```bash
th main.lua -data [path to ImageNet dataset] -nGPU 1 -batchSize 128 -netType alexnet -binaryWeight -dropout 0.1
``` 
### Training XNOR-Networks
```bash
th main.lua -data /mnt/raid00/data/imagenet2012/ -nGPU 4 -batchSize 800 -netType alexnetxnor -binaryWeight -optimType adam -epochSize 1500
```
### Trained Models
To use the trained models use the option `-retrain`

[Binary-Weight-Network(BWN)](https://s3-us-west-2.amazonaws.com/ai2-vision/xnornet/alexnet_BWN.t7)

[XNOR-Network](https://s3-us-west-2.amazonaws.com/ai2-vision/xnornet/alexnet_XNOR.t7)

### License
By downloading this software you acknowledged that you agreed on the terms and conditions in the `SOFTWARE-LICENSE-AGREEMENT.lic`
