# Kalman Filters

我学习卡尔曼滤波与贝叶斯滤波的个人仓库，教材是 Roger Labbe 的
[*Kalman and Bayesian Filters in Python*](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)。

## 仓库结构

```
book/        原书全部内容（未修改），来自 upstream commit 04b2bea（2024-07-14）
my-notes/    我自己的笔记、练习和复述
  00-python-refresher.ipynb   Python 快速复健（开始读书前先做这个）
  LEARNING_LOG.md             每次学习的记录 + 费曼复述
```

原则：**`book/` 只读，不改**；所有自己的代码和笔记放在 `my-notes/`。想在书的笔记本上做实验时，先复制一份到 `my-notes/` 再改。

## 环境搭建

```bash
git clone https://github.com/yawe-star/kalman-filters.git
cd kalman-filters
python -m venv .venv && source .venv/bin/activate     # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

- 读书时**从 `book/` 目录里打开**笔记本（书的代码会 `import kf_book`，需要在这个目录下运行）。
- 也可以用 [Google Colab](https://colab.research.google.com/)：打开后先运行
  `!git clone https://github.com/yawe-star/kalman-filters.git && %cd kalman-filters/book && !pip install filterpy`。

## 学习路线

| 阶段 | 内容 | 预计 |
|---|---|---|
| 0 | `my-notes/00-python-refresher.ipynb` | 1–2 小时 |
| 1 · 直觉 | Ch 1 g-h filter，Ch 2 Discrete Bayes | 1 周 |
| 2 · 高斯与一维 KF | Ch 3 Gaussians，Ch 4 一维卡尔曼滤波 | 1 周 |
| 3 · 多维 KF | Ch 5 多元高斯，Ch 6 多维 KF，Ch 7 KF 数学，Ch 8 滤波器设计 | 2–3 周 |
| 4 · 非线性 | Ch 9 概览，Ch 10 UKF，Ch 11 EKF，Ch 12 粒子滤波 | 2–3 周 |
| 5 · 进阶 | Ch 13 平滑，Ch 14 自适应，**Appendix E 集合卡尔曼滤波（EnKF）** | 按需 |

> 和研究方向的联系：把田间观测数据同化进作物模型（如 APSIM），常用的正是 EnKF 和粒子滤波——阶段 4、5 是重点。

## 学习方式

每章：读 → 运行并改参数 → 做书里的练习（先自己写再看答案）→ 在 `LEARNING_LOG.md` 里用自己的话复述 → 提交。

## License

原书内容 © Roger R. Labbe，按 [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/) 授权，见 `book/license.html`。
