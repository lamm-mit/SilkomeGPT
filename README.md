# SilkomeGPT: Generative strategies for modeling, design and analysis of spider silk protein sequences for enhanced mechanical properties
Generative strategies for modeling, design and analysis of silk protein sequences for enhanced mechanical properties

Wei Lu, David L. Kaplan, Markus J. Buehler 

Massachusetts Institute of Technology, 77 Massachusetts Ave., Cambridge, MA 02139, USA 

> Contact email: mbuehler@mit.edu

Abstract: Spider silks are remarkable materials characterized by superb mechanical properties such as strength, extensibility and lightweightedness. Yet, to date, limited models are available to fully explore sequence-property relationships for analysis and design. Here a custom generative large-language model is proposed to enable design of novel spider silk protein sequences to meet complex combinations of target mechanical properties. The model, pretrained on a large set of protein sequences, is fine-tuned on ~1,000 major ampullate spidroin (MaSp) sequences for which associated fiber-level mechanical properties exist, to yield an end-to-end forward and inverse generative approach that is aplied in a multi-agent strategy. Performance is assessed through: (1) a novelty analysis and protein type classification for generated spidroin sequences through Basic Local Alignment Search Tool (BLAST) searches, (2) property evaluation and comparison with similar sequences, (3) comparison of molecular structures, as well as, and (4) a detailed sequence motif analyses. This work generates silk sequences with property combinations that do not exist in nature, and develops a deep understanding of the mechanistic roles of sequence patterns in achieving overarching key mechanical properties (elastic modulus, strength, toughness, failure strain). The model provides an efficient approach to expand the silkome dataset, facilitating further sequence-structure analyses of silks, and establishes a foundation for synthetic silk design and optimization. This work not only shows the capacity of generative transformer models to design complex materials, but also illustrates an effective use of agentic modeling for self-improving design solutions. 

Keywords: biomaterials; deep learning; generative autoregressive transformer; hierarchical; multiscale modeling; spider silk; spidroin

![image](https://github.com/lamm-mit/SilkProteomeGPT/assets/101393859/dfbaf33d-d74c-4170-82cb-a3fec389f8d1)

The authors develop a generative modeling, design, and analysis technique applied to create novel spider silk protein sequences for enhanced mechanical properties. They create property combinations that do not exist in nature and develop a deep understanding of the mechanistic roles of sequence patterns in achieving overarching key mechanical properties (elastic modulus, strength, toughness, failure strain).

![image](https://github.com/lamm-mit/SilkomeGPT/assets/96086418/3a04b631-3316-4c85-9474-69766f3b3947)

## Installation
```
conda create -n SilkomeGPT python=3.8
conda activate SilkomeGPT
```
```
git clone https://github.com/lamm-mit/SilkomeGPT/
cd SilkomeGPT
```
Then, install SilkomeGPT:
```
pip install -e .
```
Start Jupyter Lab (or Jupyter Notebook):
```
jupyter-lab --no-browser
```
```
jupyter notebook
```

## Schematic of the model implemented
(a) Summary of the autoregressive decoder-only transformer model architecture, with rotary positional embedding.    
(b) Overview of modeling approach. A query including the task and relevant context is used to create the responses, with interactions among all elements considered via graph-forming attention mechanisms. Tasks included in this work include the petraining “sequence” task, as well as a “calculate” and a “generate” task. The “calculate” task predicts a set of mechanical properties based on a given sequence, and the “generate” task yields a silk sequence with associated mechanical properties (details see paper). 
![image](https://github.com/lamm-mit/SilkomeGPT/assets/96086418/8ee503a5-7c92-48c2-a284-de6e8ca8fa30)

## Sample Notebooks
The sample Notebooks is provided ([Model_inference_V2.ipynb](https://github.com/lamm-mit/SilkomeGPT/blob/73ac8a98c48ee6285f1529b7e0c1debc885086b4/Model_inference_V2.ipynb)) for pidroin sequence prediction and generation    
The inference model can be downloaded from this [link](https://www.dropbox.com/scl/fi/julfytszav7yx4go9b6ai/GPTNeoLAMM_medium_FineTuned_SolSilk_local_works_NEWDATA_F74690ac860b1b87585458a4d620b3686af07d4d.zip?rlkey=i25pn4jkpgpoel9bnymboy9ij&dl=0)    
The datafile is provided ([ALL_SEQ.csv](https://github.com/lamm-mit/SilkomeGPT/blob/73ac8a98c48ee6285f1529b7e0c1debc885086b4/ALL_SEQ.csv))    

## Sample results (details, see paper)
### Self-consistency Analysis
Protein sequence property comparison    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/96086418/037cc865-c7dc-4b26-be15-33c3a7a2d81c)

Motif analysis    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/96086418/8abd2d97-970b-4e73-8b90-727d12bfdd86)

Molecular structure comparison    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/96086418/c40c6d54-05ce-4eb8-a93d-e7696fd7f1fb)

## Citation
To cite this work:
```
@article{WeiKaplanBuehler_2023,
    title   = {Generative Modeling, Design, and Analysis of Spider Silk Protein Sequences for Enhanced Mechanical Properties},
    author  = {W. Lu, D. L., Kaplan, M.J. Buehler},
    journal = {Adv. Funct. Mater.},
    year    = {2023},
    volume  = {},
    pages   = {},
    url     = {https://doi.org/10.1002/adfm.202311324}
}
```
