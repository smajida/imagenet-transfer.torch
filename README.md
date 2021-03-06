## Imagenet Transfer Learning on torch using caffe model

This repository is torch code to transfer learning using caffe model(used [loadcaffe](https://github.com/szagoruyko/loadcaffe)). You can make good performance using small amount of data if you fine tuning or transfer learning using pretrained model.

This code is based on [imagenet-multiGPU.torch](https://github.com/soumith/imagenet-multiGPU.torch).


### Dependencies
- loadcaffe(https://github.com/szagoruyko/loadcaffe)
- cudnn(https://github.com/soumith/cudnn.torch)

### Data Preprocessing
Traning and test data needs to store in root/train and root/val respectively. First subdirectory name is going to be class name. You don't need to have label files in data.

### Training Type
- Transfer Learning: Use pretrain model as feature extractor and train last fully connected layer only.
- Fine Tunning: Use pretrain model as initializer and train whole modules including convolution layer.

### Running
Setting up the parameters in `opt.lua`. And run it.
```bash
th main.lua
```

### Thanks to
- [Soumith Chintala](https://github.com/soumith)
- [Sergey Zagoruyko](https://github.com/szagoruyko)


