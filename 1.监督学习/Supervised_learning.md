# 监督学习

通过给定正确答案进行学习， 最终实现学习算法学会只接受输入而无需输出标签， 并且给出输出的合理预测的过程。

- Input: 训练数据集， 由特征和标签组成。
- Output: 学习算法， 通过训练数据集进行训练， 使得学习算法能够对新的输入数据进行预测。
### 目标: 学习算法能够对新的输入数据进行预测， 使得预测结果与真实标签尽可能接近。
- 训练数据集(Training dataset): 包含特征和标签的样本数据集。
- 特征(Feature): 输入数据的属性或变量。
  - 输入数据(Input data): 由特征和标签组成的数据。
  - 标签(Label): 输入数据的正确答案或目标值。
- 学习算法(Learning algorithm): 用于学习函数的算法。

# 监督学习的算法

## 1. 回归算法 （Regression algorithm）
- 回归算法 (Regression algorithm): 用于预测连续值(连续变量)的算法。
- 目的是让其学习从无限多种可能的数字中预测数字。
  
### 举一个例子 ：
- 给定一个关于每平米房价与房子大小的数据集， 通过回归算法来预测房子的价格。
- 例如：
  - 房子大小: $100$ 平米， 每平米房价: $10000$ 元， 房子价格: $1000000$元。
  - 房子大小: $200$ 平米， 每平米房价: $8000$ 元， 房子价格: $1600000$ 元。
- 通过回归算法，我们可以根据房子的大小和每平米的房价来预测房子的总价格。
  
## 2. 分类算法 （Classification algorithm）
- 分类算法(Classification algorithm): 用于预测离散值(离散变量)的算法。
- 以乳腺癌作为分类问题的例子
  - 用$1$和$0$表示良性和恶性。
  - $1$表示良性，$0$表示恶性。
  - 训练数据集：
  - 特征：肿块大小、肿块形状、肿块边缘等。
  - 标签：良性或恶性。
  - 通过分类算法，我们可以根据肿块的特征来预测肿块是良性还是恶性。
    - 例如：
    - 肿块大小: $2.5$ cm， 标签: 良性。
    - 肿块大小: $3.5$ cm， 标签: 良性。
    - 肿块大小: $4.5$ cm， 标签: 恶性。
   ` 这里我们只输入一个数据 `
   
这与回归不同， 回归的目的是为了从无数多个数字中预测一个数字， 而分类的目的是为了从有限的几个类别中预测一个类别。在这里输出只有 $0$ 与 $1$ ，而不是一个数字。

- 总结一下 ：分类算法就是通过训练数据集来学习一个函数， 使得这个函数能够根据输入数据的特征来预测输出数据的标签。输出的可以输出一个类别， 也可以输出多个类别。可以是数字也可以是别的类别。

### 如果我们想要输入多个数据进行分析

1. 继续引用上面的例子:
    - 肿块大小: $2.5$ cm， 标签: 良性。
    - 肿块大小: $3.5$ cm， 标签: 良性。
    - 肿块大小: $4.5$ cm， 标签: 恶性。
    - 肿块大小: $5.5$ cm， 标签: 恶性。
  - 如果我们在输入病人的年龄这一个数据于是我们可以得到一张图
  - ![](..\image\监督学习\1a5e3adba2d7e638cd289f8a9bef413.png)
  ### 学习算法可能要做的就是找到一些边界确定是否是良性肿瘤还是恶性肿瘤。
  ### 学习算法找到的边界就是我们所说的分类器。
  
  实际上 $Input$ 还有很多别的数据但是思想是一样的
