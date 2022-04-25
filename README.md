# DML-sys

分布式机器学习系统

- FedAvg

## FedAvg

启动参数说明

|参数名|含义|区间|备注|
|:---:|:---:|:---:|:---:|
|g|加速设备|0<=|选取加速设备|
|nc|worker数目| 0< |每一个worker分配相同的数据，数据在计算过程中不发生变化|
|cf|worker选取数目|0-1|与worker相乘，得到每次迭代所涉及的client数目|
|e|epoch| 0< |worker进行本地梯度计算过程中的迭代次数|
|b|batch_size|-|本地批处理大小|
|mn|模型选择|mnist_2nn,mnist_cnn|训练模型选择-全连接和卷积|
|lr|学习速率|-||
|vf|验证频率|0<|验证模型准确率|
|sf|存储频率|0<|全局模型存储频率|
|ncomm|汇聚次数|0<|梯度汇聚次数（全局模型迭代次数）|
|sp|存储路径|-||
|iid|数据是否独立分布|0/1|0-数据随机分布，1-数据按标签顺序分布|

## 相关论文

[1] Mcmahan H B , Moore E , Ramage D , et al. Communication-Efficient Learning of Deep Networks from Decentralized Data[J]. 2016.