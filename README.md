# STFANet

Code repo for the paper "Spatio-Temporal Filter Adaptive Network for Video Deblurring".&nbsp; [[arXiv]](https://arxiv.org/pdf/1904.05065.pdf) &nbsp; [[Project Page]](https://www.shangchenzhou.com/projects/stfan/)&nbsp;

<p align="center">
  <img width=95% src="https://user-images.githubusercontent.com/14334509/61511077-1b016200-aa28-11e9-94c1-63e97f55f093.png">
</p>



## Pretrained Models

You could download the pretrained model (21.5MB) of STFANet from [[Here]](https://hiteducn0-my.sharepoint.com/:f:/g/personal/sczhou_hit_edu_cn/EiVeE2qh_e5Omxa_JrfOj6UBXgSm13kyI3RHwUPnaDL9Hg?e=5YJFOx). 

## Prerequisites

- Linux (tested on Ubuntu 14.04/16.04)
- Python 2.7+
- Pytorch 0.4.1
- easydict
- tensorboardX

#### Installation

```
pip install -r requirements.txt
bash install.sh
```

## Get Started

Use the following command to train the neural network:

```
python runner.py 
        --phase 'train'\
        --data [dataset path]\
        --out [output path]
```

Use the following command to test the neural network:

```
python runner.py \
        --phase 'test'\
        --weights './ckpt/best-ckpt.pth.tar'\
        --data [dataset path]\
        --out [output path]
```
Use the following command to resume training the neural network:

```
python runner.py 
        --phase 'resume'\
        --weights './ckpt/best-ckpt.pth.tar'\
        --data [dataset path]\
        --out [output path]
```
You can also use the following simple command, with changing the settings in config.py:

```
python runner.py
```

## Results on the testing dataset and real blurry videos

Some results are shown in [[Project Page]](https://www.shangchenzhou.com/projects/stfan/).

## Citation
If you find STFANet, or FAC layer useful in your research, please consider citing:

```
@article{Zhou2019stfan,
  title={Spatio-Temporal Filter Adaptive Network for Video Deblurring},
  author={Zhou, Shangchen and Zhang, Jiawei and Pan, Jinshan and Xie, Haozhe and Zuo, Wangmeng and Ren, Jimmy},
  journal={arXiv preprint arXiv:1904.12257},
  year={2019}
}
```

## Contact

We are glad to hear if you have any suggestions and questions.

Please send email to shangchenzhou@gmail.com

## License

This project is open sourced under MIT license.