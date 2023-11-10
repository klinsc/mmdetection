## Create env

`conda create --name openmmlab python=3.8 -y`
`conda activate openmmlab`

## Install pytorch with cuda 11.3

`conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3 -c pytorch`

## Install MMEngine and MMCV using MIM

`pip install -U openmim`
`mim install mmengine`
`mim install "mmcv>=2.0.0"`

## Install MMDetection

`pip install ninja seaborn clearml`
`pip install -v -e .`

## Verify the installation

`mim download mmdet --config rtmdet_tiny_8xb32-300e_coco --dest .`
`python demo/image_demo.py demo/demo.jpg rtmdet_tiny_8xb32-300e_coco.py --weights rtmdet_tiny_8xb32-300e_coco_20220902_112414-78e30dcc.pth --device gpu`
