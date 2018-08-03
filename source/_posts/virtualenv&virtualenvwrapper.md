---
layout: post
title: python 虚拟环境搭建
tags: 
    - python
    - virtualenv
categories: 
    - python
---

# virtualenv

virtualenv 就是用来为一个应用创建一套“隔离”的 Python 运行环境。建立不同的 python 版本的虚拟环境，每个项目之间实现隔离。

### 安装

```python
pip install virtualenv
```

### 查看版本

```python
virtualenv --version
```

![version](virtualenv//version.jpg)

### 创建虚拟环境

```python
virtualenv testenv
```

![make](virtualenv//makeenv.jpg)

#### 查看环境文件

```python
cd testenv
dir
```

![](virtualenv/cddir.png)

#### 激活虚拟环境

```
cd scripts
activate
```

![activeate](virtualenv/activate.png)

#### 在虚拟环境下安装包

```
pip list
```

![pip](virtualenv/pip.png)

#### 退出虚拟环境

```
deactivate.bat
```

![deactivate](virtualenv/deactivate.png)

## virtualenvwrapper

virtualencwrapper 主要解决每次进入 virtualenv 都需要进入 virtualenv 路径下，这样路径一多，出现管理混乱的痛点。

#### 安装 virtualenvwrapper-win

```
pip install virtualenvwrapper-win
```

配置 WORKON_HOME 环境变量,设置虚拟环境创建的路径，后续创建的虚拟环境都自动在此路径下。

![](virtualenv/wrapper-win.png)

#### 创建虚拟路径

```python
mkvirtualenv testenv
```

```
注：因为前一步设置了WORK_HOME，所有虚拟环境将安装到 E:\virtualevn
```

#### 查看虚拟工作环境

```
workon
```

![workon](virtualenv/workon.png)
出现的文件就是设置的路径下存在的虚拟环境，因之前已经创建了多个虚拟环境。

### 进入虚拟环境

```
workon testenv
```

![](virtualenv/workon_env.png)

#### 退出虚拟环境

```
deactivate
```

![](virtualenv/wrapper_deactivate.png)
