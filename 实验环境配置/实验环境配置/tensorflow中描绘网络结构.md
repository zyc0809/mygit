## tensorflow中描绘网络结构

### 1.打开命令行，进入到E盘

因为E盘根据以下代码存储了网络结构图文件，默认jupyter文件夹在E盘中

```python
writer = tf.summary.FileWriter('logs/',sess.graph)
```

### 2.输入以下命令

```python
E:\>tensorboard --logdir=E:\Jupyter\logs
```

### 3.生成一个http连接

复制该连接并用谷歌浏览器打开

