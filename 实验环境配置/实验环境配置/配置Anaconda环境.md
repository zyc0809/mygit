### 配置Anaconda环境

#### 1.从开始菜单进入Anaconda Prompt

默认是进入到base环境下

#### 2.新建环境

```python
conda create -n myenv python=3.6	#新建虚拟环境
conda create -n env_name list of packages	# -n表示名字、list of packages表示新环境中需要安装的工具包
```

####  3.列出所有虚拟环境

```python
conda env list	#或conda info -e
所有的虚拟环境保存在以下文件夹：	C:\Users\lenovo\Anaconda3\envs
```

#### 4.进入到相应的环境中

```python
conda activate myenv	#myenv为环境的名字
```

#### 5.进入到环境之后，查看该环境中的工具包

```python
pip list	#pip指令安装的包
conda list	#conda指令安装的包
```

#### 6.离开环境：

```python
deactivate
```

#### 7.删除环境

```python
conda env remove -n myenv	#myenv为环境的名字
```

#### 8.采用jupyter notebook进入到上述环境

##### 1.为该环境添加kernel

```python
pip install --user ipykernel
```

##### 2.将该环境添加到Jupyter中

```python
python -m ipykernel install --user --name=myenv		#myenv为环境名
```

##### 3.打开Jupyter Notebook：

```
jupyter lab
```

##### 4.在jupyter notebook中新建文件时会提示用哪一个kernel(环境)

![](F:\神经网络笔记\实验环境配置\images\3.png)

如上所示有两个环境一个是默认的python3，另一个是自己创建的环境tensorflow1.6

### 清华镜像安装tensorflow：

```python
pip install tensorflow_gpu==2.0 -i https://pypi.tuna.tsinghua.edu.cn/simple	#tensorflow_gpu==2.0为包名

conda install --channel https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/ cudnn=7.6.5	#cudnn=7.6.5为包名
```

### jupyter notebook操作指示：

#### 1、Tab键自动补全；

####  2、Shift+双击Tab，提示帮助；

#### 3、魔术命令

绘制图形：%matplotlib inline

显示当前目录：%pwd

%timeit [x**3 for x in range(1000)]	：显示代码的执行时间

### PyCharm中配置上述创建的环境

#### 1.setting->Python Interpreter

![](F:\神经网络笔记\实验环境配置\images\1.png)

#### 2.选择已经创建的环境

要选中所属环境的python.exe文件

![](F:\神经网络笔记\实验环境配置\images\2.png)