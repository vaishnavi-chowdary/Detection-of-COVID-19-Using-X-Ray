# DETECTION OF COVID-19 USING X-RAY

Project Summary: To build a public open dataset of chest X-ray and CT images of patients which are positive or suspected of COVID-19 or other viral and bacterial pneumonias . Data is collected from public sources as well as through indirect collection from hospitals and physicians. 

## View current [images](images) and [metadata](metadata.csv) and [a dataloader example](https://colab.research.google.com/github/vaishnavi-chowdary/Detection-of-COVID-19-Using-X-Ray/blob/master/COVID_19_Dataset_Test.ipynb)

Current stats of PA, AP, and AP Supine views. Labels 0=No or 1=Yes. Data loader is [here](https://github.com/mlmed/torchxrayvision/blob/master/torchxrayvision/datasets.py#L867)
``` 
COVID19_Dataset num_samples=481 views=['PA', 'AP']
{'ARDS': {0.0: 465, 1.0: 16},
 'Bacterial': {0.0: 445, 1.0: 36},
 'COVID-19': {0.0: 162, 1.0: 319},
 'Chlamydophila': {0.0: 480, 1.0: 1},
 'E.Coli': {0.0: 481},
 'Fungal': {0.0: 459, 1.0: 22},
 'Influenza': {0.0: 478, 1.0: 3},
 'Klebsiella': {0.0: 474, 1.0: 7},
 'Legionella': {0.0: 474, 1.0: 7},
 'Lipoid': {0.0: 473, 1.0: 8},
 'MERS': {0.0: 481},
 'Mycoplasma': {0.0: 476, 1.0: 5},
 'No Finding': {0.0: 467, 1.0: 14},
 'Pneumocystis': {0.0: 459, 1.0: 22},
 'Pneumonia': {0.0: 36, 1.0: 445},
 'SARS': {0.0: 465, 1.0: 16},
 'Streptococcus': {0.0: 467, 1.0: 14},
 'Varicella': {0.0: 476, 1.0: 5},
 'Viral': {0.0: 138, 1.0: 343}}

COVID19_Dataset num_samples=173 views=['AP Supine']
{'ARDS': {0.0: 170, 1.0: 3},
 'Bacterial': {0.0: 169, 1.0: 4},
 'COVID-19': {0.0: 41, 1.0: 132},
 'Chlamydophila': {0.0: 173},
 'E.Coli': {0.0: 169, 1.0: 4},
 'Fungal': {0.0: 171, 1.0: 2},
 'Influenza': {0.0: 173},
 'Klebsiella': {0.0: 173},
 'Legionella': {0.0: 173},
 'Lipoid': {0.0: 173},
 'MERS': {0.0: 173},
 'Mycoplasma': {0.0: 173},
 'No Finding': {0.0: 170, 1.0: 3},
 'Pneumocystis': {0.0: 171, 1.0: 2},
 'Pneumonia': {0.0: 26, 1.0: 147},
 'SARS': {0.0: 173},
 'Streptococcus': {0.0: 173},
 'Varicella': {0.0: 173},
 'Viral': {0.0: 41, 1.0: 132}}

 ```
 
There is a searchable database of COVID-19 papers [here](https://www.who.int/emergencies/diseases/novel-coronavirus-2019/global-research-on-novel-coronavirus-2019-ncov), and a non-searchable one (requires download) [here](https://pages.semanticscholar.org/coronavirus-research).
 
- See [SCHEMA.md](SCHEMA.md) for more information on the metadata schema.

*Formats:* For chest X-ray dcm, jpg, or png are used. 

## Background Information

In the context of a COVID-19 pandemic, we want to improve prognostic predictions to triage and manage patient care. Data is the first step to developing any diagnostic/prognostic tool. While there exist large public datasets of more typical chest X-rays from the NIH [Wang 2017], Spain [Bustos 2019], Stanford [Irvin 2019], MIT [Johnson 2019] and Indiana University [Demner-Fushman 2016], there is no collection of COVID-19 chest X-rays or CT scans designed to be used for computational analysis.

The 2019 novel coronavirus (COVID-19) presents several unique features. While the diagnosis is confirmed using polymerase chain reaction (PCR), infected patients with pneumonia may present on chest X-ray and computed tomography (CT) images with a pattern that is only moderately characteristic for the human eye . In late January, a Chinese team published a paper detailing the clinical and paraclinical features of COVID-19. They reported that patients present abnormalities in chest CT images with most having bilateral involvement [Huang 2020](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(20)30183-5/fulltext).  


## Motive

The goal is to use these images to develop AI based approaches to predict and understand the infection

The tasks are as follows using chest X-ray or CT (preference for X-ray) as input to predict these tasks:

- Healthy vs Pneumonia (prototype already implemented [Chester](https://mlmed.org/tools/xray/) with ~74% AUC, validation study [here](https://arxiv.org/abs/2002.02497))

- Prognostic/severity predictions (survival, need for intubation, need for supplemental oxygen)

## COVID-19 image data collection
(https://www.youtube.com/watch?v=ineWmqfelEQ))

# Motivation
 CODING BLOCKS(Detecting COVID-19 from X-Ray| Training a Convolutional Neural Network | Deep Learning)
