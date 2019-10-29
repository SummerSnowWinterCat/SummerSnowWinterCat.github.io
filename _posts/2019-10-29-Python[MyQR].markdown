---
layout: post
title: "Python MyQR試し"
date: 2019-10-29 22:07:00 +0900
categories:
---

# Python MyQR

1.install MyQR

```python
pip install MyQR
pip3 install MyQR
```

2.create py file

```python
from MyQR import myqr
import os # this  import is os path support 
		myqr.run(words='-->Text input!<--', # input link or text
             version=1, # 设置容错率为最高默认边长是取决于你输入的信息的长度和使用的纠错等级；													而默认纠错等级是最高级的H
    				 level='H', # 控制纠错水平，范围是L、M、Q、H，从左到右依次升高
   					 picture='-->IMG location<--',
   					 colorized=True,#可以使产生的图片由黑白(False)变为彩色(True)的	
             contrast=1.0,#用以调节图片的对比度，1.0 表示原始图片，更小的值表示更低对比度，更     														大反之。默认为1.0
             brightness=1.0,#用来调节图片的亮度，其余用法和取值与 -con 相同
             save_name='-->save img path<--', #格式 jpg bmp png gif
             save_dir=os.getcwd() # save path control
)
```

3.run py.file

