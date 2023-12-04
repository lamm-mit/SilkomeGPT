# SilkomeGPT: Generative strategies for modeling, design and analysis of spider silk protein sequences for enhanced mechanical properties
Generative strategies for modeling, design and analysis of silk protein sequences for enhanced mechanical properties

Wei Lu, David L. Kaplan, Markus J. Buehler 

Massachusetts Institute of Technology, 77 Massachusetts Ave., Cambridge, MA 02139, USA 

> Contact email: mbuehler@mit.edu

Abstract: Spider silks are remarkable materials characterized by superb mechanical properties such as strength, extensibility and lightweightedness. Yet, to date, limited models are available to fully explore sequence-property relationships for analysis and design. Here a custom generative large-language model is proposed to enable design of novel spider silk protein sequences to meet complex combinations of target mechanical properties. The model, pretrained on a large set of protein sequences, is fine-tuned on ~1,000 major ampullate spidroin (MaSp) sequences for which associated fiber-level mechanical properties exist, to yield an end-to-end forward and inverse generative approach that is aplied in a multi-agent strategy. Performance is assessed through: (1) a novelty analysis and protein type classification for generated spidroin sequences through Basic Local Alignment Search Tool (BLAST) searches, (2) property evaluation and comparison with similar sequences, (3) comparison of molecular structures, as well as, and (4) a detailed sequence motif analyses. This work generates silk sequences with property combinations that do not exist in nature, and develops a deep understanding of the mechanistic roles of sequence patterns in achieving overarching key mechanical properties (elastic modulus, strength, toughness, failure strain). The model provides an efficient approach to expand the silkome dataset, facilitating further sequence-structure analyses of silks, and establishes a foundation for synthetic silk design and optimization. This work not only shows the capacity of generative transformer models to design complex materials, but also illustrates an effective use of agentic modeling for self-improving design solutions. 

Keywords: biomaterials; deep learning; generative autoregressive transformer; hierarchical; multiscale modeling; spider silk; spidroin

* Pretrained model on Hugging Face 🤗: https://huggingface.co/lamm-mit/SilkomeGPT

* Trained model on Hugging Face 🤗: https://huggingface.co/lamm-mit/SilkomeGPT

![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/bfb2b832-f806-4d5d-9068-0ec982784e93)

We report a generative modeling, design, and analysis technique applied to create novel spider silk protein sequences for enhanced mechanical properties. The model allows us to create property combinations that do not exist in nature and develop a deep understanding of the mechanistic roles of sequence patterns in achieving overarching key mechanical properties (elastic modulus, strength, toughness, failure strain).

![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/8661d281-12a8-4507-b610-939377a1b694)

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

![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/599c30af-7ef0-4950-ae92-13c229a982ea)

## Sample Notebooks
A sample Notebooks is provided ([SilkomeGPT_inference.ipynb](https://github.com/lamm-mit/SilkomeGPT/blob/main/SilkomeGPT_inference.ipynb)) for spidroin sequence prediction and generation 

The trained model can be downloaded from Hugging Face 🤗: https://huggingface.co/lamm-mit/SilkomeGPT

## Sample results (details, see paper)
### Self-consistency Analysis
Protein sequence property comparison    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/ea0f1073-8d69-4d54-8d39-5ac3c9cf76ef)

Motif analysis    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/5357e500-dae8-41a4-b699-9f949d245150)

Molecular structure comparison    
![image](https://github.com/lamm-mit/SilkomeGPT/assets/101393859/2f446c2e-f762-44ad-8b85-6caaeecb7c7f)

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
