# 基于Spotify数据库对李克勤「弦续」巡回演唱会歌单的数据分析
![](https://img.shields.io/badge/ReadMe-English-blue?link=README.md
) &emsp; ![](https://img.shields.io/badge/ReadMe-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-blue?link=readme.zh.md
)
![](https://img.shields.io/badge/python-brightgreen
) ![](https://img.shields.io/badge/jupyter-notebook-brightgreen
)


## 项目目标
利用从**Spotify Web API**获得的数据，旨在分析李克勤「弦续」巡回演唱会粤港澳三地尾场歌单的选曲。

具体而言，此项目将探讨：
- 歌单中热门金曲与沧海遗珠的平衡程度
- 在这次主题巡回中， 哪张专辑是李生心头好
- 粤港澳三地的歌单有何异同

## 项目动机
李克勤是为数不多能在1980年代到2020年代持续活跃，且保持人气与专辑稳定产出的粤语流行乐坛的代表性歌手。身为粉丝及数据爱好者，我很好奇一位资深艺人如何透过数据驱动的分析来平衡音乐传承和观众期望。

这三场演唱会虽然在不同地区举行，名称也略有不同，但都有统一的主题和管弦/交响乐团合作。这种一致性为比较分析提供了理想的基础。

## 开发工具
- Python
    - Spotipy
    - pandas / NumPy
    - matplotlib
- Jupyter Notebook

## 数据来源
- **Spotify Web API**: 曲目元数据
- 手动获取歌单数据

## 相关档案
- [report_zh.ipynb](report_zh.ipynb): 完整的Jupyter notebook
- 案例数据集已存储在`/dataset`路径文件夹

## 可视化
### 象限图
![](img/23HK.png)
![](img/24GZ.png)
![](img/25OM.png)
### 柱形图
![](img/23HLRDFinal.PNG)
![](img/24HLRDFinal.PNG)
![](img/25HLRDFinal.PNG)


