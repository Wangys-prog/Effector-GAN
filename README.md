# <Effector-GAN>
   
# Effector-GAN

Effector-GAN: prediction of fungal effector proteins based on pre-trained deep representation learning methods and generative adversarial networks 

Effector-GAN is an open-source Python-based toolkit, which operates depending on the Python environment (Python Version 3.7). 

Before running Effector-GAN, users should make sure all the following packages are installed in their Python environment. 
   

# **The codes can be downloaded from our gitlab (http://47.109.24.44:4747/wangys_biolab/effector-gan)**
  

## **Prerequisites**

### **iFeature**
    
    To obtain iFeature, please download from https://github.com/Superzchen/iFeature/.
    
   **Add iFeature into environment variables (~/.bashrc)** 
   
   ` export PATH=$PATH:/xxxx/xxxx/xxxxx/iFeature`
   
   `source ~/.bashrc`
 
## **Installation**

  **Create an Python3.7 environment using conda:**
    
  `conda create -n Effector-GAN python=3.7`
    
  **Activate conda environment:**
    
  `conda activate Effector-GAN`
  
 **For python3.7 **
 
   **pytorch: https://pytorch.org/get-started/previous-versions/**
   
  **conda install**
   
    **# CUDA 10.0**
    
    conda install pytorch==1.3.1 torchvision==0.4.2 cudatoolkit=10.0 -c pytorch
    
    **# CPU Only**
    
    conda install pytorch==1.3.1 torchvision==0.4.2 cpuonly -c pytorch
    
  **pip install**
  
    **If you have GPU  # CUDA 10.0**
  
    pip install torch==1.3.1 torchvision==0.4.2
  
    **CPU Only python3.7**
    
    pip install torch==1.3.1+cpu torchvision==0.4.2+cpu -f https://download.pytorch.org/whl/torch_stable.html
  
 **other packages** 
   
    pip3 install joblib==1.0.1  
    pip3 install tape_proteins==0.5 
    pip3 install numpy==1.19.2 
    pip3 install pandas==1.2.0 
    pip3 install Bio==1.0.2
    pip3 install sklearn


## **Effector-GAN**

    git clone http://47.109.24.44:4747/wangys_biolab/effector-gan.git
  
    cd effector-gan

## Input parameters

    python Effector_GAN.py -h  
    $ -i  inputfile in FASTA format  
    $ -o  output csv file
 
## Usage

    conda activate Effector-GAN
    
  `python Effector_GAN.py -i independent_test_pos.fasta -o test_result.csv` 
  
### The model will run faster in GPU than CPU  
   
    For the test data (independent_test_pos.fasta), UniRep Embedding will take about 11 minutes in CPU and 0.239 mins in GPU
     `
## WGAN.py

     Synthetic protein feature samples based on generative adversarial networks

## CTST2.py
   
     Effector-GAN uses the leave-one-out cross-validation (LOOCV) method based on K nearest neighbor algorithm (KNN; K=1) classifier to evaluate the optimal synthetic protein feature samples, which are used to augment the original positive training samples

## figure_tsne.py
  
    t-SNE-transformed 2D visualization of real and synthetic protein feature samples obtained from different training iterations

## other tools

    http://lab.malab.cn/~wys/

## **If you use Effector-GAN, please cite:** 
    (1) Wang Y, .Effector-GAN: prediction of fungal effector proteins based on pre-trained deep representation learning methods and generative adversarial networks
    (2) Yansu Wang, Murong Zhou, Quan Zou, Lei Xu. Machine learning for phytopathology: from the molecular scale towards the network scale. Briefings in Bioinformatics. 2021, Doi: 10.1093/bib/bbab037
    (3) Yansu Wang, Lei Xu, Quan Zou, Chen Lin. prPred-DRLF: plant R protein predictor using deep representation learning features. Proteomics. 2021. DOI: 10.1002/pmic.202100161
