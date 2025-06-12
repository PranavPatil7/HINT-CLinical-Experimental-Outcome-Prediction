# HINT: Hierarchical Interaction Network for Clinical Trial Outcome Prediction





This repository hosts HINT, a deep learning based method for clinical trial outcome prediction. 
The repository can be mainly divided into three parts:
- [`benchmark`](https://github.com/futianfan/clinical-trial-outcome-prediction/tree/main/benchmark) describes the process of curating benchmark dataset named **Trial Outcome Prediction (TOP)** for clinical trial outcome prediction. 
- [`HINT`](https://github.com/futianfan/clinical-trial-outcome-prediction/tree/main/HINT) is the Hierarchical Interaction Network, a deep learning based method. 
- [`data`](https://github.com/futianfan/clinical-trial-outcome-prediction/tree/main/data) stores processed data. 


The following figure illustrates the pipeline of HINT. 

<p align="center"><img src="./HINT/hint.png" alt="logo" width="810px" /></p>



## Table Of Contents 

- [Installation](#installation)
- [Benchmark Data](#benchmark) 
- [HINT: Learn and Inference](#hint) 
- [Tutorial (Jupyter Notebook)](#tutorial)
- [Contact](#contact) 

--- 

<a name="installation"></a>
## ⚙️ Installation

I built conda environment and uses `conda` or `pip` to install the required packages. See [`conda.yml`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/conda.yml) for all the packages. 

```bash
conda create -n predict_drug_clinical_trial python==3.7 
conda activate predict_drug_clinical_trial 
conda install -c rdkit rdkit  
pip install tqdm scikit-learn 
pip install torch
pip install seaborn 
pip install icd10-cm
```

We use following command to activate conda environment. 
```bash
conda activate predict_drug_clinical_trial
```

---


<a name="benchmark"></a>
## 📊 Benchmark Data

To standardize the clinical trial outcome prediction, I created a benchmark dataset for Trial Outcome Prediction named TOP, which incorporate rich data components about clinical trials, including drug, disease and protocol (eligibility criteria). 
All the scripts are in the folder [`benchmark`](https://github.com/futianfan/clinical-trial-outcome-prediction/tree/main/benchmark). 
Please see [`benchmark/README.md`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/benchmark/README.md) for details. 

---


<a name="hint"></a>
## 🤖 HINT: Learn and Inference 

After processing the data, we learn the Hierarchical Interaction Network (HINT) on the following four tasks. The following figure illustrates the pipeline of HINT. All the scripts are available in the folder [`HINT`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/HINT). 
Please see [`HINT/README.md`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/HINT/README.md) for details. 

### Prediction results

We add the prediction results in `./results` for all the three phases. 

### Trained model

The trained HINT models for all the three phases are available in `./save_model`.  

## 📚 Tutorial (jupyter notebook)


- `benchmark`: [`tutorial_benchmark.ipynb`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/benchmark/README.md) describes some key components of the data curation process. 
- `HINT`: [`tutorial_HINT.ipynb`](https://github.com/futianfan/clinical-trial-outcome-prediction/blob/main/HINT/README.md) is a tutorial to learn and evaluate HINT step by step. 

















