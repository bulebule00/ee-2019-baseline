# ee-2019-baseline
面向金融领域的事件主体抽取（ccks2019，https://biendata.com/competition/ccks_2019_4/ ），一个baseline

## 模型
用BiLSTM做实体标注，用指针结构标注实体。

实际上这个

## 用法
`python el.py`即可。gtx 1060上4分钟训练一个epoch，6分钟完成验证，所以每个epoch的总时间是10分钟左右。

## 结果
5个epoch左右线下划分的验证集的F1应该就能到达0.61～0.62了，实测最后F1能跑到0.65+（f1: 0.6576, precision: 0.7285, recall: 0.5993），自动保存F1最优的模型。

训练有随机性，建议多重跑几次，选择最优模型。

## 环境
Python 2.7 + Keras 2.2.4 + Tensorflow 1.8，其中关系最大的应该是Python 2.7了，如果你用Python 3，需要修改几行代码，至于修改哪几行，自己想办法，我不是你的debugger。

欢迎入坑Keras。人生苦短，我用Keras～

## 声明
欢迎测试、修改使用，但这是我比较早的模型，文件里边有些做法在我最新版已经被抛弃，所以以后如果发现有什么不合理的地方，不要怪我故意将大家引入歧途就行了。

欢迎跟我交流讨论，但请尽量交流一些有意义的问题，而不是debug。（如果Keras不熟悉，请先自学一个星期Keras。）

<strong>特别强调</strong>：baseline的初衷是供参赛选手测试使用，如果你已经错过了参赛日期，但想要训练数据，请自行想办法向主办方索取。我不负责提供数据下载服务。

## 链接
- https://kexue.fm
- https://keras.io
