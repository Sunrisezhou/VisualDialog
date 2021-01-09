# 视觉对话

### 环境

1.运行环境：Pytorch 1.3.1, CUDA 10.0, CuDNN 7.6.5, Python 3.6.12

2.依赖库安装：`pip install -r requirements.txt`

### 数据集及相关依赖下载

1.下载数据集：下载[VisDial](https://visualdialog.org/data)数据集以及默认参数文件[test_btmup_f.hdf5](https://drive.google.com/file/d/1BXWPV3k-HxlTw_k3-kTV6JhWrdzXsT7W/view?usp=sharing)，并将其置于`PROJECT_ROOT/data/`文件夹下。

2.下载预训练Faster R-CNN，将其置于`PROJECT_ROOT/data/`文件夹下：
  
  - [features_faster_rcnn_x101_train.h5](https://s3.amazonaws.com/visual-dialog/data/v1.0/2019/features_faster_rcnn_x101_train.h5)
  
  - [features_faster_rcnn_x101_val.h5](https://s3.amazonaws.com/visual-dialog/data/v1.0/2019/features_faster_rcnn_x101_val.h5)
  
  - [features_faster_rcnn_x101_test.h5](https://s3.amazonaws.com/visual-dialog/data/v1.0/2019/features_faster_rcnn_x101_test.h5)

3.下载预训练[GloVe](http://nlp.stanford.edu/data/glove.6B.zip)词向量，将`glove.6B.300d.txt`置于`PROJECT_ROOT/data/`文件夹下。

### 数据预处理及词向量初始化

1.数据预处理
  ```
  cd PROJECT_ROOT/script/
  python prepro.py
  ```

2.词向量初始化
  ```
  cd PROJECT_ROOT/script/
  python create_glove.py
  ```

### 模型训练

  ```python main_v1.0.py``` or ```python main_v0.9.py```

### 模型保存

  模型保存在```saved_models```文件夹内
  
### 性能评价

  ```python eval_v1.0.py``` or ```python eval_v0.9.py```
