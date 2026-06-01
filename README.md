# 吉林大学23软件数据挖掘期末作业：天猫复购预测

这是数据挖掘课期末作业整理出来的版本，题目选的是天池日常学习赛「[天猫复购预测-挑战 Baseline](https://tianchi.aliyun.com/competition/entrance/231576/information)」。

简单来说，就是根据用户之前的浏览、加购、购买和收藏记录，预测用户之后会不会再次购买某个商户的商品。

## 成绩记录

| 指标             |             结果 |
| ---------------- | ---------------: |
| 天池榜单最佳 AUC | `0.695094883992` |
| 天池榜单排名记录 |             `62` |

## 文件结构

```text
.
|-- data/
|   `-- README.md
|-- notebook/
|   `-- main.ipynb
|-- environment.yml
|-- requirements.txt
`-- README.md
```

## 数据准备

仓库里不放竞赛原始数据。需要先从天池页面下载数据，然后放到 `data/` 目录下。CSV 文件名保持天池原始命名：

```text
data/
|-- user_info_format1.csv
|-- user_log_format1.csv
|-- train_format1.csv
`-- test_format1.csv
```

## 环境安装

依赖统一写在 `requirements.txt` 里，`environment.yml` 只是方便用 Conda 创建环境。

推荐用 Conda：

```bash
conda env create -f environment.yml
conda activate tmall-repurchase
```

也可以直接用 pip：

```bash
python -m pip install -r requirements.txt
```

## 运行方式

启动 JupyterLab：

```bash
jupyter lab
```

打开并按顺序运行：

```text
notebook/main.ipynb
```

运行完成后，提交文件会生成在：

```text
submissions/submission.csv
```

## 说明

- Notebook 的执行输出已经清理过。
- `data/`、`submissions/` 和生成的模型文件不会提交到 Git。
