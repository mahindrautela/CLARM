# CLARM 
 Note: Read the details of the project are given below. The code is available on **LANL's github** at https://github.com/lanl/clarm.
### Conditional Latent Autoregressive Recurrent Model for spatiotemporal learning
##### CLARM is a unsupervised deep learning approach to learn spatiotemporal dynamics. CLARM consists of a CVAE and LSTM combined together in an autoregressive loop to learn spatial and temporal dynamics independently. Here, CVAE learns spatial correlations of the high dimensional objects in a low-dimensional latent space distribution and a RNN like Long Short-Term Memory (LSTM) learn the temporal dynamics within the latent space. Using CVAE part, new realistic samples can generated by conditionally sampling the latent space followed by decoding. Using LSTM part, the future states can be forecasted given few initial states as inputs. The proposed model addresses challenges faced by existing models in learning spatiotemporal dynamics, such as expensive computations in ConvLSTM and DCGAN, mixed spatial features and temporal dynamics in 3DCNN/4DCNN, computational complexity, lack of scalability, and robustness issues in GNNs, linear representation of data in the latent space through PCA-LSTM, and explainability concerns in the latent space with like AE-LSTM.

<p align="center">
  <img src="images/clarm.PNG" width="450" height="260" />
</p>

##### The CLARM is used to learn spatialtemporal evolution of 6D phase space of charged beams in particle accelerators. The model can generate phase space projections at various accelerator modules by sampling and decoding the latent space representation. The model also forecasts 6D phase space of charged particles in downstream modules from limited phase space information at upstream locations. This repository contains codes accompanying the [paper](https://arxiv.org/abs/2403.13858). The dataset accompying the paper is available at Zenodo.  <a href="https://doi.org/10.5281/zenodo.10819001"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10819001.svg" alt="DOI"></a>

<p align="center">
  <img src="images/clarm_lansce.png" width="450" height="260" />
</p>

##### **Latent space visualization:**

<p align="center">
  <img src="images/latent.PNG" width="500" height="450" />
</p>

##### **Generative ability of CLARM**:

<p align="center">
  <img src="images/gen_pc_pca_metrics_mod_1.png" width="650" height="375" />
</p>

##### **Forecasting ability of CLARM**:

<p align="center">
  <img src="images/forecasting_log.gif" width="550" height="200" />
</p>

For more information:  
1. Arxiv [Link](https://arxiv.org/abs/2403.13858) of the paper: A conditional latent autoregressive recurrent model for generation and forecasting beam dynamics in particle accelerators.
2. HPSim, an advanced, open-source tool developed at LANL, enables rapid, online simulations of multiple-particle beam dynamics. The basic source code of HPSim is available [here](https://github.com/apphys/hpsim) (now inactive repository). The dataset is collected from the new version of HPSim, which is available with LANL (not opensourced).
3. The dataset accompying the paper is available at Zenodo.  <a href="https://doi.org/10.5281/zenodo.10819001"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10819001.svg" alt="DOI"></a>.
4. Please cite the paper if you are using data, code or paper.
   
```
@article{rautela2024conditional,
  title={A conditional latent autoregressive recurrent model for generation and forecasting of beam dynamics in particle accelerators},
  author={Rautela, Mahindra and Williams, Alan and Scheinker, Alexander},
  journal={Scientific Reports},
  volume={14},
  number={1},
  pages={18157},
  year={2024},
  publisher={Nature Publishing Group UK London}
}
```
