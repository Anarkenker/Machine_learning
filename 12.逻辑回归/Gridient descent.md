
再展示一下成本函数
$$
 J(\vec{w}, b) = \frac{1}{m} \sum_{i=1}^{m}-y^{(i)}\log(f_{\vec{w},b}(\vec{x}^{(i)})) - (1-y^{(i)})\log(1-f_{\vec{w},b}(\vec{x}^{(i)})
$$
再展示一下梯度下降公式：

对于权重向量 $\vec{w}$ 和偏置 $b$，梯度下降的更新规则为：

$$
w_j = w_j - \alpha \frac{\partial J(\vec{w}, b)}{\partial w_j}, \quad \text{对于 } j = 1, 2, \dots, n
$$

$$
b = b - \alpha \frac{\partial J(\vec{w}, b)}{\partial b}
$$

其中，$\alpha$ 是学习率，$\frac{\partial J(\vec{w}, b)}{\partial w_j}$ 和 $\frac{\partial J(\vec{w}, b)}{\partial b}$ 分别是成本函数 $J(\vec{w}, b)$ 对 $w_j$ 和 $b$ 的偏导数。

以下是成本函数 $J(\vec{w}, b)$ 对 $w_j$ 和 $b$ 的偏导数公式：

对 $w_j$ 的偏导数：
$$ \frac{\partial J(\vec{w}, b)}{\partial w_j} = \frac{1}{m} \sum_{i=1}^{m} \left( f_{\vec{w},b}(\vec{x}^{(i)}) - y^{(i)} \right) x_j^{(i)} $$

对 $b$ 的偏导数：
$$ \frac{\partial J(\vec{w}, b)}{\partial b} = \frac{1}{m} \sum_{i=1}^{m} \left( f_{\vec{w},b}(\vec{x}^{(i)}) - y^{(i)} \right) $$

其中：

$f_{\vec{w},b}(\vec{x}^{(i)})$ 是模型的预测值（例如逻辑回归中的 sigmoid 函数）。
$x_j^{(i)}$ 是第 $i$ 个样本的第 $j$ 个特征值。
$y^{(i)}$ 是第 $i$ 个样本的真实标签。