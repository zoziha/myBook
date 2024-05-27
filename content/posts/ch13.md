+++
title = 'ch13-初识 R 语言'
date = 2024-05-26T23:35:19+08:00
draft = false
+++

Windows 下载 R 解释器和 RStudio 集成开发环境：

```powershell
winget install Posit.RStudio --source winget
```

`R` 语言与 `Matlab/Octave` 相似，比 `Python` 开箱即用些，但更适合统计分析与绘图。

`R` 语言示例：

```r
age = c(1, 3, 5, 2, 11, 9, 3, 9, 12, 3)
weight = c(4.4, 5.3, 7.2, 5.2, 8.5, 7.3, 6, 10.4, 10.2, 6.1)
mean(weight)
sd(weight)
cor(age,weight)
plot(age,weight)
```

对比 `Python`:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import pearsonr  # 用于计算皮尔逊相关系数

# 定义年龄和体重列表
age = [1, 3, 5, 2, 11, 9, 3, 9, 12, 3]
weight = [4.4, 5.3, 7.2, 5.2, 8.5, 7.3, 6.0, 10.4, 10.2, 6.1]

# 计算体重的平均值
x = np.mean(weight)

# 计算体重的标准差
sd_weight = np.std(weight)

# 计算年龄和体重之间的皮尔逊相关系数
correlation, _ = pearsonr(age, weight)

# 输出平均值和标准差
print(f"体重的平均值：{x}")
print(f"体重的标准差：{sd_weight}")
print(f"年龄与体重的相关系数：{correlation}")

# 绘制散点图
plt.scatter(age, weight)
plt.xlabel("年龄")
plt.ylabel("体重")
plt.title("年龄与体重的关系")
plt.show()
```
