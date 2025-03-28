---
layout: page
permalink: /blogs/PytorchPypiInstall/index.html
title: Pytorch-PypiInstall
---

## 使用pip安装pytorch-cuda版本

这个问题在2025年有了新的意义，因为官方移除了conda的安装方法，笔者之前使用的conda换源方法失效。新版本的pypi安装方法会指定下载地址到官方源。然而，这对国内的科研工作者并不友好。
[移除官方conda源​](github.com/pytorch/pytorch/issues/138506)

经过一上午的搜寻，发现阿里、上交等开源镜像站的pytorch-wheels均已年久失修。好在南京大学开源镜像站仍在维护。（顺带一提，作为南京的高校，使用南京大学开源镜像站速度往往比其他高开源镜像站快很多，夸夸！）
方法很简单：

### 方法1：使用官方的pip

#### Step 1：搜寻官方下载地址

例如最新版2.6.0的下载地址如下：
> pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126


#### Step 2: 生成新下载地址

将其中--index-url替换，注意，只替换标红文字：
> <font color="red">https://download.pytorch.org/whl/</font>cu126 

替换为：
> <font color="red">https://mirror.nju.edu.cn/pytorch/whl/</font>cu126   

### 方法2： 使用conda forge

2025年3月27日，经评论区提醒与本人测试，可以使用conda forge频道安装具体方法如下：
打开conda forge的pytorch网站，然后复制其中的安装命令即可。

[Pytorch | Anaconda.org](https://anaconda.org/conda-forge/pytorch)



<br>