# 安装opencv

按照https://blog.csdn.net/mawonly/article/details/87856530 

# 运行baseline

## 运行报错：

(1)提示没有定义train()，修改train_loss = model.train(train_loader, model, criterion, optimizer)；

(2)运行中发现train()在定义时没有传入epoch变量，调用时把这个参数去掉；

(3)但是去掉后还是报错‘train() takes 4 positional arguments but 5 were given’，推测是python语言对类函数定义的问题，将train的定义修改为def train(self,train_loader, model, criterion, optimizer):但是，还是会报错……train_loader, model, criterion, optimizer没有传入，不知道什么原因。

## 运行结果

最后借队长调试好的代码跑了一下，因为使用的是CPU运行速度比较慢，跑了两轮之后结果是0.3897。下一步打算把数据传导Google Drive上，用Colab上的GPU运行。
