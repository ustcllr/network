## 项目介绍：

- 本项目使用numpy实现深层神经网络，其中用到的技术包括向量化，正向和反向传播，mini-batch，正则化输入，还有初始化权重。
- 目前最好成绩是可以在18秒训练一个3层神经网络，使识别率达到97.2。
- 神经网络固定前面L-1层使用RELU，第L层使用Softmax
- 未使用dropout，原因是在小型的神经网络中，它的效果并不好，降低方差的同时增加了偏差，并不能提高识别率。
- 未使用学习率衰减，原因是使用了mini-batch之后很容易拟合，并不会出现梯度消失。
- 未使用batch-norm，因为BN是使曲面在训练过程中不倾斜从而梯度更容易下降。但是使用mini-batch后可以认为训练次数大幅增多，并不需要适应更多大的学习率。另一个原因是，BN的反向传播比较难实现，故放弃。
- 未使用增大数据集，因为使用CNN可以达到类似的效果。
- 项目将训练和识别分成了两个文件，这是为了有一定的流程性。
- 数据集并没有上传，需要在根目录下创建数据集文件夹并在data_support中指定名称。
- 成本函数发生溢出的原因：出现了梯度爆炸，这跟没有进行BN有一定的关系

