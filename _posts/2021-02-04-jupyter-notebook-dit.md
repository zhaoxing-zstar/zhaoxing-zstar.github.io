---
layout: post
title: "Jupyter Notebook更改默认工作路径"
subtitle: ''
date: 2021-02-04
author: "Zstar"
header-style: text
header-img: "img/post-bg-js-module.jpg"
tags:
  - Jupyter
---


### 下载Anaconda3

首先从官网下载Anaconda3的Individual Edition，下载好后打开Anaconda3 Prompt，输入:
jupyter notebook --generate-config:

```
jupyter notebook --generate-config
```
---
### 打开配置文件

输入完后，会显示文件产生的路径，按路径找到jupyter_notebook_config.py，用txt或者pycharm打开，
按`ctrl+F`搜索notebook_dir，找到后填入想要设置的路径并保存（注意顺便Uncomment这一行，就是删掉前面的`#`号,加路径时最好前面加上`r`转义
![notebook_dir](/img/jupyter/notebook_dir.png)

---
### 修改JupyterNotebook快捷方式的目标属性

右击JupyterNotebook快捷方式，选择[属性]，删除[目标]属性中的[%USERPROFILE%]，点击[确定]

![change_prop](/img/jupyter/change_prop.png)

修改完成，再打开Anaconda Prompt输入jupyter notebook打开工作路径就发生变化了。
