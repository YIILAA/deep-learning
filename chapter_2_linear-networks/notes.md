 # 笔记
 ## softmax- regression
 softmax回归
 - 是一个多类分类模型
 - 使用softmax操作得到每个类别的预测置信度
 - 使用交叉墒衡量预测和label的区别
 
 softmax
 输出匹配概率（非负，和为1）
 
 cross-entropy-loss 交叉墒损失函数
 常用来衡量两个概率的区别
 梯度是 真实概率和预测概率的区别
 
 ## 损失函数
 L2 Loss
 缺点：y^接近y时，梯度减小
 
 L1 Loss
 优点：在不为0时，梯度是一个常数
 缺点：为0时不可导，优化到后期可能不稳定
 
 Huber‘s Robust Loss 
 结合上两种的优点
 
 总结：
 理解损失函数的特性，可以画三条图像
 - 原图
 - 求导后（梯度）
 - 极大似然
 
 ## 图像分类数据集
 
 
 # 代码
 torch.nn.Module.apply(fn), 对每一个层应用该函数
 
 def init_weights(m):
    if type(m) == nn.Linear:
        nn.init.normal_(m.weight, std=0.01)
 net.apply(init_weights);
 
 
 
 
 