# classification
## 垃圾分类-数据分析和预处理
* 整体数据探测
* 分析数据不同类别分布
* 分析图片长宽比例分布
* 切分数据集和验证集
* 数据可视化展示（可视化工具 pyecharts,seaborn,matplotlib)

## 代码结构
.
├── app_WSL-Images_resnext.py
├── app_garbage.py
├── args.py
├── checkpoint
│   ├── checkpoint.pth.tar
│   ├── garbage_resnext101_model_9_9547_9588.pth
│   └── resnext101_16d_log_iter10_cuda.txt
├── data
│   ├── ImageNet1k_label.txt
│   ├── class.txt
│   ├── garbage-classify-for-pytorch
│   ├── garbage_label.txt
│   ├── train1.txt
│   └── val1.txt
├── facebookresearch_WSL-Images_resnext.ipynb
├── garbage-classification-using-pytorch.py
├── json_utils.py
├── living.ipynb
├── model.py
├── models
│   ├── alexnet.py
│   ├── densenet.py
│   ├── inception.py
│   ├── resnet.py
│   ├── squeezenet.py
│   └── vgg.py
├── preprocess
├── transform.py
├── utils
│   ├── eval.py
│   ├── json_utils.py
│   ├── logger.py
│   └── misc.py

## resnext101网络架构
* pre_trained_model resnext101 网络架构原理
* 基于pytorch 数据处理、resnext101 模型分类预测
* 在线服务API 接口

## 垃圾分类-训练
python garbage-classification-using-pytorch.py \
        --model_name resnext101_32x16d \
        --lr 0.001 \
        --optimizer  adam \
        --start_epoch 1 \
        --epochs 2 \
        --num_classes 4 
* model_name 模型名称
* lr 学习率
* optimizer 优化器
* start_epoch 训练过程断点重新训练
* num_classes 分类个数
## 垃圾分类-评估
python garbage-classification-using-pytorch.py \
    --model_name resnext101_32x16d \
    --evaluate  \
    --resume checkpoint/checkpoint.pth.tar \
    --num_classes 4 
    
* model_name 模型名称
* evaluate 模型评估
* resume 指定checkpoint 文件路径，保存模型以及训练过程参数

## 垃圾分类-在线预测

python app_garbage.py \
    --model_name resnext101_32x16d \
    --resume checkpoint/garbage_resnext101_model_9_9547_9588.pth
    
* model_name 模型名称
* resume 训练模型文件路径    
* 模型预测   
命令行验证和postman 方式验证    
举例说明：命令行模式下预测    
curl -X POST -F file=@cat.jpg http://ip:port/predict

## 附录

对于python 和 pytorch 基础不好的同学，推荐大家优先学习 老师的4门课程。

* 《人工智能-深度学习框架-Pytorch案例实战视频课程》
* 《Python数据可视化 pyecharts实战》
* 《Python数据可视化教程 Seaborn》
* 《Python数据可视化教程 matplotlib实战课程》





# ig_resnext101_32x16-c6f796b0.pth



- File Name：ig_resnext101_32x16-c6f796b0.pth
- 百度网盘：

> 链接：https://pan.baidu.com/s/1iTsc8ztbkQGdoDq_ZNaoAA 
> 提取码：8tc7 