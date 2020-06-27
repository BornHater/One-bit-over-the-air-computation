# One-bit over-the-air computation

Two experiments are conducted
1) CNN on MNIST dataset
2) ResNet18 on CIFAR10 dataset

## Requirements
python = 3.6.5  
pytorch = 1.0.0

## Commands for running the experiments:

1) Command for CNN on MINIST dataset:
> CUDA_VISIBLE_DEVICES=0 python main_fed.py --dataset mnist --iid --num_channels 1 --model cnn --num_users 100 --epochs 300 --lr 0.0001 --frac 1.0 --local_ep 1 --momentum 0.0 --local_bs 50 --bs 50 


2) Command for ResNet18 on Cifar10 dataset:
> CUDA_VISIBLE_DEVICES=2 python main_fed.py --dataset cifar --iid --num_channels 3 --model resnet18 --num_users 100 --snr 10 --epochs 300 --lr 0.001 --frac 1.0 --local_ep 1 --momentum 0.0 --local_bs 512 --bs 512 --lr-scheduler --mode NP_CSI --thd 2.8 --delta 0.01 



## Note

1) The output of the experiment is a .log file including all the training results, e.g. training loss and test accuracy;

2) The configurable parameters in the code are defined in the file "option.py".
