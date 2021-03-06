Random Forest
=============

对决策树进行改写，在每个节点（有K个可用属性）选择属性时首先随机选择log(1+K)个属性，之后仅从这些属性中选择用于分裂节点的属性。

整体上随机森林由多棵随机属性的决策树构成，通过装袋方法构造。每次构造使用有放回均匀抽样构造样本集并训练决策树，分类时，每棵树都投票并且返回得票最多的类。

AdaBoost
========

AdaBoost是一种提升算法，通过串行的训练多个具有权值的分类器来提高组合分类器的准确率。每次训练首先依据样本权值进行有放回抽样得到样本集，训练结束后对得到分类器在训练集上进行分类，得到错误率和该分类器的权值，并对训练集中的样本权值进行调整，使得后续的分类器训练更加专注于之前分类错误的样本。分类时，每个分类器都投票并根据分类器自身的权值进行加权，最后得到权值最大的类。
