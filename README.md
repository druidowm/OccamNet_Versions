# Overview
 This a compilation of implementations of and papers regarding OccamNet.
 
 OccamNet was first described in the paper [Interpretable Neuroevolutionary Models for Learning Non-Differentiable Functions and Programs](https://arxiv.org/abs/2007.10784v1) which has since been revised to [Fast Neural Models for Symbolic Regression at Scale](https://arxiv.org/abs/2007.10784).


 # Which OccamNet Version Should I Use?

 Good question! Below are some questions which can help you narrow down which version of OccamNet to use.

## Do you need a Pytorch implementation?

If the answer is no, we reccomend using our Jax repository, occamnet_equinox (not yet publicly released, coming soon). This version includes all functionality of other implementations (except for two regularization terms), and is considerably faster than our Pytorch implementations. Additionally, because we use Equinox, it is object oriented just like our Pytorch versions. It also has an sklearn interface for ease of use.

Otherwise, to choose a Pytorch repository, see the questions below.

## Do you need to fit constants, implicit functions, or ensemble datasets?

If the answer is yes, we reccomend using using the [OccamNet Social-Science repository](https://github.com/druidowm/OccamNet_SocialSci). This repository allows constant fitting and implicit function fitting, and unlike other Pytorch repositories, it also allows for fitting ensemble datasets. The only downside of this repository is that like all OccamNet Pytorch implementations that allow constant fitting, it is slow.

## Do you want a fast Pytorch implementation which scales well on a GPU?

If so, we reccomend using using the [OccamNet_Public/optimized](https://github.com/druidowm/OccamNet_Public/tree/main/optimized) implementation. This repository is fast and scales well on a GPU, but it does not allow for constant fitting, implicit function fitting, or fitting ensemble datasets.

# OccamNet Implementations
For completeness, this list includes older repositories which we no longer suggest using.

* [occam-net](https://github.com/AllanSCosta/occam-net) — This is our original repository. All of the code from this repository has since been incorporated into `OccamNet_Public`, which we reccomend using instead. This repository is written in [Pytorch](https://pytorch.org).

* [OccamNet_Public](https://github.com/druidowm/OccamNet_Public) — This is our main repository, which includes the original code from `occam-net` as well as several other implementations and tests. In particular, this repository includes OccamNet implementations which are Object Oriented and allow for constant fitting and implicit function fitting. It also includes an OccamNet implementation which is Object Oriented and runs efficiently on GPUs. This repository is written in [Pytorch](https://pytorch.org).

* [OccamNet_SocialSci](https://github.com/druidowm/OccamNet_SocialSci) — This is our repository which uses OccamNet for discovering models in Social Science datasets. It includes an improved implementation of OccamNet which allows constant fitting and implicit function fitting, and which unlike other Pytorch repositories also allows for fitting ensemble datasets. This implementation is written in [Pytorch](https://pytorch.org).

* occamnet-equinox — __COMING SOON, NOT YET RELEASED__ — This is our Jax implementation of OccamNet, which we reccomend for new users. It includes all of the functionality of other implementations (except for two regularization terms), and is considerably faster than our Pytorch implementations. Additionally, because we use Equinox, it is object oriented just like our Pytorch versions. It also has an sklearn interface for ease of use. This implementation is written in [Jax](https://jax.readthedocs.io/en/latest/) using [Equinox](https://docs.kidger.site/equinox/).

# OccamNet Papers
* [Interpretable Neuroevolutionary Models for Learning Non-Differentiable Functions and Programs](https://arxiv.org/abs/2007.10784v1) — The original paper describing OccamNet.

* [Fast Neural Models for Symbolic Regression at Scale](https://arxiv.org/abs/2007.10784) — An updated version of the original paper with additional functionality and testing.

* [AI-Assisted Discovery of Quantitative and Formal Models in Social Science](https://arxiv.org/abs/2210.00563) — A paper using OccamNet to discover models from Social Science data.
