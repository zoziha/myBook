+++
title = 'Ch16-Matplotlib 绘图'
date = 2024-05-26T23:35:19+08:00
draft = false
categories = ["计算机科学"]
+++

在中文期刊发表时，往往需要在绘图中使用中文，并生成高质量图像，这里给出基础示例：

```python
# 绘制多个子图，并使用中文
import matplotlib.pyplot as plt
import scienceplots

with plt.style.context(["science", "no-latex"]):
    plt.rcParams["font.family"] = (
        " Times New Roman, SimSun"  # 设置字体族，中文为SimSun，英文为Times New Roman
    )
    plt.rcParams["mathtext.fontset"] = "stix"  # 设置数学公式字体为stix
    fig, axes = plt.subplots(figsize=(8, 6), ncols=2, nrows=2)

    axes = axes.flatten()

    for i in range(4):
        axes[i].set_xlim(9000, 11000000)
        axes[i].set_ylim(1, 100000)
        axes[i].grid(linestyle="--")

    axes[0].semilogx(
        [10000, 100000, 1000000, 10000000],
        [15.76, 36.64, 568.00, 14050.00],
        label="Index-sort-2D",
        marker="o",
        ls="--",
    )
    axes[0].semilogx(
        [10000, 100000, 1000000, 10000000],
        [21.69, 70.50, 791.20, 34160.00],
        label="Index-sort-3D",
        marker="x",
        ls="--",
    )
    axes[0].semilogx(
        [10000, 100000, 1000000, 10000000],
        [4.54, 41.12, 990.00, 14280.00],
        label="Spatial-hashing-2D",
        marker="s",
    )
    axes[0].semilogx(
        [10000, 100000, 1000000, 10000000],
        [8.33, 79.06, 2367.00, 28670.00],
        label="Spatial-hashing-3D",
        marker="^",
    )
    axes[0].set_xscale("log")
    axes[0].set_yscale("log")
    axes[0].set_xlabel("粒子数/个")
    axes[0].set_ylabel("单步耗时/ms")
    axes[0].set_title("均匀分布")

    axes[1].semilogx(
        [10000, 100000, 1000000, 1000000],
        [2.97, 43.81, 3436.00, 3436.00],
        label="Index-sort-2D",
        marker="o",
        ls="--",
    )
    axes[1].semilogx(
        [10000, 100000, 1000000, 1000000],
        [3.92, 47.99, 2503.00, 2503.00],
        label="Index-sort-3D",
        marker="x",
        ls="--",
    )
    axes[1].semilogx(
        [10000, 100000, 1000000, 1000000],
        [5.13, 54.29, 2512.00, 2512.00],
        label="Spatial-hashing-2D",
        marker="s",
    )
    axes[1].semilogx(
        [10000, 100000, 1000000, 10000000],
        [8.77, 69.27, 1478.00, 22550.00],
        label="Spatial-hashing-3D",
        marker="^",
    )
    axes[1].set_xscale("log")
    axes[1].set_yscale("log")
    axes[1].set_title("正态分布")
    axes[1].set_xlabel("粒子数/个")
    axes[1].set_ylabel("单步耗时/ms")

    axes[2].semilogx(
        [10000, 100000, 1000000, 10000000],
        [343.91, 344.75, 384.42, 2519.46],
        label="Index-sort-2D",
        marker="o",
        ls="--",
    )
    axes[2].semilogx(
        [10000, 100000, 1000000, 10000000],
        [359.96, 361.47, 411.39, 2584.77],
        label="Index-sort-3D",
        marker="x",
        ls="--",
    )
    axes[2].semilogx(
        [10000, 100000, 1000000, 10000000],
        [9.41, 31.18, 253.18, 4116.66],
        label="Spatial-hashing-2D",
        marker="s",
    )
    axes[2].semilogx(
        [10000, 100000, 1000000, 10000000],
        [9.49, 31.98, 282.29, 8533.71],
        label="Spatial-hashing-3D",
        marker="^",
    )
    axes[2].set_xscale("log")
    axes[2].set_yscale("log")
    axes[2].set_xlabel("粒子数/个")
    axes[2].set_ylabel("内存占用/MB")
    axes[2].set_title("均匀分布")

    axes[3].semilogx(
        [10000, 100000, 1000000, 1000000],
        [50.58, 83.49, 618.06, 618.06],
        label="Index-sort-2D",
        marker="o",
        ls="--",
    )
    axes[3].semilogx(
        [10000, 100000, 1000000, 1000000],
        [53.42, 58.51, 198.77, 198.77],
        label="Index-sort-3D",
        marker="x",
        ls="--",
    )
    axes[3].semilogx(
        [10000, 100000, 1000000, 10000000],
        [9.42, 48.87, 1351.06, 17735.29],
        label="Spatial-hashing-2D",
        marker="s",
    )
    axes[3].semilogx(
        [10000, 100000, 1000000, 1000000],
        [9.49, 32.61, 259.72, 259.72],
        label="Spatial-hashing-3D",
        marker="^",
    )
    axes[3].set_xscale("log")
    axes[3].set_yscale("log")
    axes[3].set_title("正态分布")
    axes[3].set_xlabel("粒子数/个")
    axes[3].set_ylabel("内存占用/MB")

    lines, labels = fig.axes[-1].get_legend_handles_labels()
    fig.legend(
        lines,
        labels,
        loc="center",
        facecolor="white",
        framealpha=0.75,
        frameon=True,
        bbox_to_anchor=(0.522, 0.506),
        ncol=2,
    )

    plt.tight_layout()
    plt.savefig("plot2.svg")
    plt.show()
```

借助 Inkscape，将 svg 转为 emf 获得不错的矢量图像。

## 16.1 参考链接

- [Matplotlib cheatsheets](https://matplotlib.org/cheatsheets/)。
