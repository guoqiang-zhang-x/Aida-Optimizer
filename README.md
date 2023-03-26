# Aida Optimizer
## 1) Brief description of Aida
Aida optimiser is designed to effectively train DNN models. As an extension of AdaBelief, Aida exploits the layerwise gradient statistics via simple layerwise vector projections per iteration.  One property of Aida is that the histogram of the adaptive stepsizes tends to much more compact (or narrow) than those of AdaBelief and Adam when training a DNN model. See __G. Zhang, K. Niwa, and W. B. Kleijn, "On Exploiting Layerwise Gradient Statistics for Effective Training of Deep Neural Networks", arXiv:2203.13273v3, March, 2022.__ [[paper link]](https://arxiv.org/abs/2203.13273) 

![test](https://github.com/guoqiang-x-zhang/AidaOptimizer/blob/main/imgs/Aida_3stage_overall_mean.eps)

## 2) Introducing layerwise stepsizes into Adam and AdaBelief
As a side product, we also propose LAdaBelief and LAdam as extensions of AdaBelief and Adam. Considering LAdaBelief, it is deisgned by introducing layerwsie adaptive stepsizes into AdaBelief by pre-processing. By doing so, LAdaBelief only needs to store one parameter per neural layer for computing the layerwisee adaptive stepsize while AdaBelief needs to store the same number of parameters as the DNN model. Similarly, LAdam is designed in a similar manner as LAdaBelief. It is found that the two new methods produce comparable performance as Adam and AdaBelief for a number of typical DNN tasks (see the experiemtal part of the above paper).  

