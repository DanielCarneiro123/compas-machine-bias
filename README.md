# Compas Machine Bias

## Case Study Description
COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) is an algorithmic system used in the US criminal justice system to predict the risk of criminal recidivism. It
has gained notoriety for accusations of racial bias, as studies show that black people tend to receive
unfairly higher risk assessments when compared to white people with similar criminal histories. This
case raises ethical questions about the use of AI in decisions that affect people’s freedom, involving
issues such as fairness, transparency, accountability and algorithmic discrimination.

## Purpose
The aim of this project is to:
- Understand and quantify bias in the COMPAS dataset.
- Apply fairness metrics to evaluate the algorithm's performance.
- Develop recommendations for mitigating algorithmic bias.

## Features
- **Data Analysis**: Comprehensive analysis of the ProPublica's COMPAS dataset.
- **Fairness Metrics**: Implementation of measures like equalized odds, and disparate impact.
- **Bias Mitigation**: Methods to address and reduce bias, such as reweighting and threshold adjustments.

## Installation

1. Clone the repository:
   ```bash
   git clone git@github.com:DanielCarneiro123/compas-machine-bias.git
   cd compas-machine-bias
   ```

2. Create a Python Environment
   ```bash
    conda create --name compas-env python==3.11.10
    conda activate compas-env
    ```

3. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

**Some issues may occur because of aequitas(check [aequitas](https://github.com/dssg/aequitas) to see possible fix) so we recommend running our colab notebook.**

1. Run [notebook](https://colab.research.google.com/drive/1DY4txRU9GU8O-uXQ3-f85tm3JgqhOoF-?usp=sharing)

## Usage
1. Run the Jupyter notebooks to explore the data and perform analyses:
   ```bash
   jupyter notebook
   ```

## Results
Key findings from the analysis:
- Significant disparities in prediction accuracy and error rates across racial groups.

Refer to the [report](https://pt.overleaf.com/read/cmbrzsfqfjzv#b5270f) and notebook for insights.

## References

- [ProPublica Machine Bias](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)
- [It's Compaslicated](https://arxiv.org/pdf/2106.05498)
- [AIF360](https://aif360.res.ibm.com/)
- [FairLearn](https://fairlearn.org/)
- [Aequitas](https://github.com/dssg/aequitas)
- [report](https://pt.overleaf.com/read/cmbrzsfqfjzv#b5270f)

## Contact
For questions or suggestions, feel free to reach out:
- [Daniel Carneiro](https://github.com/DanielCarneiro123) (up202108832@up.pt)
- [Athos Freitas](https://github.com/athoscf) (up202108792@up.pt)
- [Gonçalo Costa](https://github.com/goncalobcosta) (up202108814@up.pt)
- [José Santos](https://github.com/Sereno1710) (up202108729@up.pt)
- [Luís Du](https://github.com/LuisDu902) (up202105385@up.pt)

