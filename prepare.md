## GNN

#### GeniePath: Graph Neural Networks with Adaptive Receptive Paths

图神经网络是利用中心节点的n阶邻居信息作为特征训练的网络，这篇文章提出了一种自适应的中心节点路径，在广度和深度上如何选择邻居节点给出方案。

传统的路径搜索方式：GCN使用傅里叶变换将空间域转换成频域，但是需要在训练前预先做Laplacian正则化，限制了只能在inductive场景下使用。GraphSage将邻居节点的数量固定（max/avg），用LSTM预先选择使用那些邻居节点。GAT使用Attention机制仅选择了中心节点的直接邻居。

实验表明，增加多层hidden  layer，性能不会有影响。


**广度**

$$h_i^{(tmp)}=tanh({W_i^{(t)}}^T\sum_{j \in N(i) \bigcup \{i\} } \alpha(h_i^{(t)}, h_j^{(t)}) \cdot h_j^{(t)})$$

$$\alpha(x,y)=softmax_y(v^Ttanh(W_s^T x+W_d^Ty))$$

**深度**

$$h_i^{(t+1)}=o_i \bigodot tanh(C_i^{(t+1)})$$

$$i_i = \sigma({W_i^{(t)}}^T h_i^{(tmp)})$$
$$f_i = \sigma({W_f^{(t)}}^T h_i^{(tmp)})$$
$$o_i = \sigma({W_o^{(t)}}^T h_i^{(tmp)})$$
$$\tilde{C}=tanh({W_c^{(t)}}^Th_i^{(tmp)})$$
$$C_i^{(t+1)}=f_i \bigodot C_i^{(t)}+ i_i \bigodot \tilde{C}$$

#### Predict then Propagate: Graph Neural Networks meet Personalized PageRank

文章提出GNN仅仅考虑了较浅层邻居节点的传递过程，而当隐层逐渐增大时，GCN会出现Laplacian oversmoothing的现象。[Keyulu Xu et al.](https://arxiv.org/pdf/1806.03536.pdf)提出，当层数增加时，给GCN增加了random  walk极限分布，



#### LanczosNet: Multi-Scale Deep Graph Convolutional Networks



------

Paper

GeniePath: Graph Neural Networks with Adaptive Receptive Paths

Predict then Propagate: Graph Neural Networks meet Personalized PageRank

LanczosNet: Multi-Scale Deep Graph Convolutional Networks

------

候选Paper

Graph Convolutional Networks for Text Classification

Session-based Recommendation with Graph Neural Networks

How Powerful are Graph Neural Networks?

------

基础知识：

GAT



GCN

[Semi-Supervised Classification with Graph Convolutional Networks](http://arxiv.org/pdf/1609.02907.pdf)

[Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering](https://arxiv.org/abs/1606.09375)

GraphSage

[Representation learning on graphs: Methods and applications](https://arxiv.org/abs/1709.05584)

------

Resource

[Euler 系统介绍](https://github.com/alibaba/euler/wiki/%E7%B3%BB%E7%BB%9F%E4%BB%8B%E7%BB%8D)
[GCN blog](http://tkipf.github.io/graph-convolutional-networks/)
[理解GCN](https://www.zhihu.com/question/54504471)

------

对比GeniePath的deepth过程和GRU
