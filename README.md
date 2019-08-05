# RippleNet

This repository is the implementation of RippleNet ([arXiv](https://arxiv.org/abs/1803.03467)):
> RippleNet: Propagating User Preferences on the Knowledge Graph for Recommender Systems  
Hongwei Wang, Fuzheng Zhang, Jialin Wang, Miao Zhao, Wenjie Li, Xing Xie, Minyi Guo  
The 27th ACM International Conference on Information and Knowledge Management (CIKM 2018)

![](https://github.com/hwwang55/RippleNet/blob/master/framework.jpg)

RippleNet is a deep end-to-end model that naturally incorporates the knowledge graph into recommender systems.
Ripple Network overcomes the limitations of existing embedding-based and path-based KG-aware recommendation methods by introducing preference propagation, which automatically propagates users' potential preferences and explores their hierarchical interests in the KG.

A PyTorch re-implementation of RippleNet by Qibin Chen et al. is [here](https://github.com/qibinc/RippleNet-PyTorch).


### Files in the folder

- `data/`
  - `book/`
    - `BX-Book-Ratings.csv`: raw rating file of Book-Crossing dataset;
    - `item_index2entity_id.txt`: the mapping from item indices in the raw rating file to entity IDs in the KG;
    - `kg.txt`: knowledge graph file;
  - `movie/`
    - `item_index2entity_id.txt`: the mapping from item indices in the raw rating file to entity IDs in the KG;
    - `kg_part1.txt` and `kg_part2.txt`: knowledge graph file;
    - `ratrings.dat`: raw rating file of MovieLens-1M;
- `src/`: implementations of RippleNet.



### Required packages
The code has been tested running under Python 3.6.5, with the following packages installed (along with their dependencies):
- tensorflow-gpu == 1.4.0
- numpy == 1.14.5
- sklearn == 0.19.1


### Running the code
```
$ cd src
$ python preprocess.py --dataset movie (or --dataset book)
$ python main.py --dataset movie (note: use -h to check optional arguments)
```

###相关博客
1、https://blog.csdn.net/qq_40006058/article/details/89742816 知识图谱与推荐系统之RippleNet 
2、https://blog.csdn.net/Accepted_Lam/article/details/89258616  ripple net模型: 知识图谱结合推荐系统
3、https://blog.csdn.net/weixin_34357267/article/details/87167388  推荐系统遇上深度学习(二十六)--知识图谱与推荐系统结合之DKN模型原理及实现...
