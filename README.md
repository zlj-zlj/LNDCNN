# LNDCNN

LNDCNN is a lung nodule detector. Implementation of paper - [LNDCNN: A Lung Nodule Detection Model Based on Improved YOLOv7]



## Requirements



``` shell
matplotlib>=3.2.2
numpy>=1.18.5
opencv-python>=4.1.1
Pillow>=7.1.2
PyYAML>=5.3.1
requests>=2.23.0
scipy>=1.4.1
torch>=1.7.0,!=1.12.0
torchvision>=0.8.1,!=0.13.0
tqdm>=4.41.0
protobuf<4.21.3
tensorboard>=2.4.1
pandas>=1.1.4
seaborn>=0.11.0
```

</details>

## train



``` shell
python train.py --workers 8 --device 0 --batch-size 8 --data data/luna16.yaml --img 640 640 --cfg cfg/training/yolov7_luna.yaml --weights '' --hyp data/hyp.scratch.p5.yaml

```
## Testing

``` shell

python test.py --data data/luna16.yaml --img 640 --batch 8 --device 0 --weights best.pt

```
