# Note

## Theoretical Frameworks

### Artificial Intelligence

### Machine Learning

### Deep Learning

## Engineering Practices

### Regularization

- L1/L2/Lp
  - L1: (Lasso Regularization / 稀疏规则算子)
    - 定义: `L1 = sum(|w|)`
    - 作用: L1 norm 可以使权值稀疏, 便于特征提取
  - L2: (Ridge Regularization)
    - 定义: `L2 = sum(w^2) ** 1/2`
    - 作用: L2 norm 可以防止过拟合, 提升模型泛化能力
  - Lp: `Lp = sum(|w|^p) ** (1/p)`

### Over-fitting & Under-fitting

- 原因
  - 数据规模与模型能力不匹配
    - 数据集过小 -> 模型过拟合
      - 方法一: 扩充数据集
      - 方法二: 降低模型复杂度
    - 数据集过大 -> 模型欠拟合
      - 方法一: 提高模型复杂度
  - 训练周期不适合
    - 周期太长 -> 模型过拟合
      - 方法一: 提前停止训练
    - 周期太短 -> 模型欠拟合
      - 方法一: 增加训练周期
  - 特殊情况
    - 方法一: 正则化
    - 方法二: Dropout
    - 方法三: 交叉验证

## Application Scenarios

### Recommendation System

#### 推荐系统冷启动

- 方法
  - 基于非个性化推荐
  - 基于用户信息推荐
  - 使用快速试探策略
  - 使用兴趣迁移策略
  - 使用关系传递策略
