# 2018-TianChi-Double-high-Round-1
2018年天池美年双高初赛代码
#### 数据链接：https://pan.baidu.com/s/1DWdxtHv7EegLRW7HFLwSSQ 密码：34f7
### 0.make_TXT_to_PANDAS.py 将原始txt数据转化为pandas可读数据
### 1.wish_train_label.py 清洗数据的标签
### 2.clean_data_part.py 清晰0得到的数据 默认选择初赛b数据
### bk_up.py 模型训练 大约3小时 默认选择清洗后的初赛b数据

### 运行环境详见附件：windwos10 python3.5 环境
### 内存需求 12g及其以上
### 磁盘需求 5g及其以上

### 线下结果大约为 0.0290x附近

# 思路：
## 数据分为 定量/定性 两个部分
### 定量的数据清洗主要是洗掉 类似 25 25 这样的错位数据 和 替换数据中的一些特殊字符 类似于 圆角/半圆角
### 对于定性的部分，主要是一些指标数据，这部分直接采用 labelencode 编码

## 数据中存在很多文字描述，提取文字中的数值，同时另外一部分的文字信息采取tfidf

### 基本全部运行需要2小时，其中模型特征提取部分比加快，测试部分由于采取了10 flod，因此速度比较慢


### 全部数值特征 --- 第一个版本baseline
### 数值+文本提取的数值 --- 第二个版本baseline
### 数值+文本提取的关键字 --- 第三个版本baseline
### 数值+文本数值+关键字+tfidf --- 第四个版本baseline
