---
layout: post
title: "How to display Chinese in matplotlib"
date: 2019-12-16
excerpt: "Get rid of annoying error codes when plotting."
tags: [matplotlib, Chinese, font, pandas, dataframe, plotting]
comments: true
---

## Problem

When plotting graphs where Chinese characters are present, the followng issue may happen

`...Glyph 40857 (or other number) missing from current font.`

This annoyed me several times when I deal with China's data. I used to translate the variables into English to avoid this problem, but now I have to a visualization in Chinese, and decide to get rid of this problem forever.

## Solution

### Get a Chinese font

In Windows, the fonts are located in `C:\Windows\Fonts\`, find `SimHei Regular` in the files. Copy it and you have `simhei.ttf` on hand. Or you can simply find one online. 

### Get Matplotlib location

Execute the following commands in your jupyter notebook / any ide

```python
import matplotlib
matplotlib.matplotlib_fname()
```

You will have the absolute path of `matplotlibrc` config file like

```shell
C:\ProgramData\Anaconda3\lib\site-packages\matplotlib\mpl-data\matplotlibrc

```

The fonts folder is located at the same level of `matplotlibrc`, to be more specific

```shell
C:\ProgramData\Anaconda3\lib\site-packages\matplotlib\mpl-data\fonts\ttf\
```

Copy `simehi.ttf` file into this folder.

### Reload fonts

Run the following command once

```python
from matplotlib.font_manager import _rebuild
_rebuild()
```

### Set font dynamically

Add the following code every time before plotting

```python
import matplotlib
# Set default font
matplotlib.rcParams['font.sans-serif'] = ['SimHei'] 
matplotlib.rcParams['font.family'] ='sans-serif'
# solve the problem that minus sign '-' is displayed as square
matplotlib.rcParams['axes.unicode_minus'] = False 
```
