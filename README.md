We have been sorting out the code and the pretrained models. Please stay tuned.

# Deep Snake for Real-Time Instance Segmentation

![city](assets/snake_city.png)

> [Deep Snake for Real-Time Instance Segmentation](https://arxiv.org/pdf/2001.01629v2.pdf)  
> Sida Peng, Wen Jiang, Huaijin Pi, Xiuli Li, Hujun Bao, Xiaowei Zhou  
> CVPR 2020

Any questions or discussions are welcomed!

## Installation

Please see [INSTALL.md](INSTALL.md).

## Testing

### Testing on Cityscapes

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/EX6rAwkK7jBEp7LxKbYIjAkB0QCFjBL4Ov6_aaK1zZFfrA?e=fRWG2x) and put it to `$ROOT/data/model/rcnn_snake/long_rcnn/197.pth`.
2. Test:
    ```
    # use coco evaluator
    python run.py --type evaluate --cfg_file configs/city_rcnn_snake.yaml
    # use the cityscapes offical evaluator
    python run.py --type evaluate --cfg_file configs/city_rcnn_snake.yaml test.dataset CityscapesVal
    ```

### Testing on Kitti

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/ERrNrpFPg71HmaegOIqypFkBzqeYn84RF5Sq9dUZM7nsbg?e=bQZ8bp) and put it to `$ROOT/data/model/snake/kins/149.pth`.
2. Test:
    ```
    python run.py --type evaluate --cfg_file configs/kins_snake.yaml test.dataset KinsVal
    ```

### Testing on Sbd

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/EVIoAulD8ORAli3qjdPBMOoBbRTHaxhPHn_a76EznL_W-g?e=EzQQS1) and put it to `$ROOT/data/model/snake/Sbd/149.pth`.
2. Test:
    ```
    python run.py --type evaluate --cfg_file configs/sbd_snake.yaml test.dataset SbdVal
    ```

## Visualization

### Visualization on Cityscapes

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/EX6rAwkK7jBEp7LxKbYIjAkB0QCFjBL4Ov6_aaK1zZFfrA?e=fRWG2x) and put it to `$ROOT/data/model/rcnn_snake/long_rcnn/197.pth`.
2. Visualize:
    ```
    # Visualize Cityscapes test set
    python run.py --type visualize --cfg_file configs/city_rcnn_snake.yaml test.dataset CityscapesTest ct_score 0.3
    # Visualize Cityscapes val set
    python run.py --type visualize --cfg_file configs/city_rcnn_snake.yaml test.dataset CityscapesVal ct_score 0.3
    ```

If setup correctly, the output will look like

![vis_city](assets/vis_city.png)

### Visualization on Kitti

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/ERrNrpFPg71HmaegOIqypFkBzqeYn84RF5Sq9dUZM7nsbg?e=bQZ8bp) and put it to `$ROOT/data/model/snake/kins/149.pth`.
2. Visualize:
    ```
    python run.py --type visualize --cfg_file configs/kins_snake.yaml test.dataset KinsVal ct_score 0.3
    ```

### Visualization on Sbd

1. Download the pretrained model [here](https://zjueducn-my.sharepoint.com/:u:/g/personal/pengsida_zju_edu_cn/EVIoAulD8ORAli3qjdPBMOoBbRTHaxhPHn_a76EznL_W-g?e=EzQQS1) and put it to `$ROOT/data/model/snake/Sbd/149.pth`.
2. Visualize:
    ```
    python run.py --type visualize --cfg_file configs/sbd_snake.yaml test.dataset SbdVal ct_score 0.3
    ```

## Citation

If you find this code useful for your research, please use the following BibTeX entry.

```
@inproceedings{peng2020deep,
  title={Deep Snake for Real-Time Instance Segmentation},
  author={Peng, Sida and Jiang, Wen and Pi, Huaijin and Li, Xiuli and Bao, Hujun and Zhou, Xiaowei},
  booktitle={CVPR},
  year={2020}
}
```
