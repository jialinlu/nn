__1、项目类型__     
该项目主要是做了一个新闻二分类：垃圾和非垃圾（1：垃圾，0：非垃圾）     

__2、模型流程__  
一共有8个主要的步骤：  
`第1步：`特征提取：one-hot向量   
`第2步：`前向传播：one-hot向量 -> 全连接1 -> tanh激活函数 -> 全连接2 -> sigmoid激活函数   
`第3步：`梯度下降：随机小批量梯度下降（mini-batch GD）   
`第4步：`目标函数：二次代价函数/交叉熵函数。   
`第5步：`反向传播：error -> delta2 -> sigmoid激活函数 -> 全连接2  -> delta1 -> tanh激活函数 -> 全连接1。其中，delta2为z2的梯度，delta1为z1的梯度， z2=output1*w2+b2，error = y-y_{p}， z1=x*w2+b1    
`第6步：`参数更新：更新w1、b1、w2、b2四个模型参数。    
`第7步：`模型保存：使用numpy.savez函数保存模型。    
`第8步：`推理预测：使用numpy.load函数加载模型。然后，利用前向传播模型和模型参数，即可以推理出结果。    

__3、知乎详情讲解：__   
`https://zhuanlan.zhihu.com/p/150975232`   
