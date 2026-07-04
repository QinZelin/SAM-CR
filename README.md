## Usage
The code framework is mainly borrowed from CGNet，a supervised change detection framework. Thus,
please refer to [CGNET-README.md](https://github.com/ChengxiHAN/CGNet-CD) for installing main packeges such as python, pytorch, etc.
## Training
Both SAM1 and SAM2 can be applied to this framework. 
Before running the code, you need to download the SAM source code and place it in this directory. The source codes are from [SAM1](https://github.com/facebookresearch/segment-anything),[SAM2](https://github.com/facebookresearch/sam2).

Training on LEVIR-CD dataset with a 5% labeled ratio: 

```
python train.py --epoch 50 --batchsize 8 --gpu_id '1' --data_name 'LEVIR' --model_name 'ResNet__PSP' --labeled_ratio 5 --flag 1
```

## Inference

Evaluation on LEVIR-CD dataset

```
python test.py --gpu_id '1' --data_name 'LEVIR' --model_name 'ResNet__PSP'
```
