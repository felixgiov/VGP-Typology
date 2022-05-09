Dataset from the paper "The Semantic Typology of Visually Grounded Paraphrases" 
------

### Introduction

Visually grounded paraphrases (VGPs) are different phrasal expressions describing the same visual concept in an image. Identifying VGPs has the potential to improve vision and language tasks such as visual question answering and image captioning in a way similar to which paraphrases have been applied to natural language processing tasks such as question answering (Riezler et al. 2007) and machine translation. Previous studies treat VGP identification as a binary classification task, which classifies a pair of phrases into VGPs or non-VGPs, and ignores various phenomena behind VGPs. In this paper, we propose semantic typology for VGPs, aiming to elucidate the VGP phenomena. The creation of the semantic VGP typology will not only elucidate the phenomena behind VGPs but also open up novel ways of utilizing VGPs for various vision and language tasks, which require semantic understanding.  

![VGP](https://ars.els-cdn.com/content/image/1-s2.0-S1077314221001697-gr1_lrg.jpg)

### Overview of the dataset
We define five classes of VGPs: *equivalence*, *forward entailment*, *reverse entailment*, *alternation*, and *independence*. Data annotated with the class of VGP type can be found in this repository. We used the Flickr 30K Entities Dataset to serve as a basis for getting candidates for paraphrases from where we extract VGPs and annotate them for semantic typology. The annotation was carried out in two stages. 

1. Rule-based annotation  
Some of the easy-to-detect examples were annotated using manually defined rules in order to reduce the cost of manual annotation.

2. Human annotation  
Majority of the annotation was carried out using Amazon Mechanical Turk (AMT).
 
The annotation process yielded 24,992, 5,734 and 6,061 labelled VGPs for training, validation and testing respectively.

### Description of the dataset
The dataset is  divided into three separate csv files for train, validation and test. Each file contains the following information. 
* **image**  
ID of the image in flickr30K dataset that the VGP pair belongs to.
* **phrase(1&2)**  
VGPs obtained after removing stop words from original VGPs.
* **original_phrase(1&2)**  
The original VGPs extracted from the flickr30K entity dataset.
* **original_label**  
Semantic typology class of the VGP pair.  
*forward entailment* : Entailment1, *reverse entailment* : Entailment2.
* **type_label**  
Index of the typology class of VGPs.  
*alternation* : 0, *forward entailment* : 1, *reverse entailment* : 2, *equivalence* : 3, *independence* : 4.

### Citation
If you use this dataset, please cite our paper ["Chenhui Chu, Vinicius Oliveira, Felix Giovanni Virgo, Mayu Otani, Noa Garcia, Yuta Nakashima. The Semantic Typology of Visually Grounded Paraphrases. Computer Vision and Image Understanding, (2021)"](https://www.sciencedirect.com/science/article/pii/S1077314221001697)

Bibtex for citations:

```bibtex
@article{CHU2022103333,
title = {The semantic typology of visually grounded paraphrases},
journal = {Computer Vision and Image Understanding},
volume = {215},
pages = {103333},
year = {2022},
issn = {1077-3142},
doi = {https://doi.org/10.1016/j.cviu.2021.103333},
url = {https://www.sciencedirect.com/science/article/pii/S1077314221001697},
author = {Chenhui Chu and Vinicius Oliveira and Felix Giovanni Virgo and Mayu Otani and Noa Garcia and Yuta Nakashima},
keywords = {Vision and language, Image interpretation, Visual grounded paraphrases, Semantic typology, Dataset},
abstract = {Visually grounded paraphrases (VGPs) are different phrasal expressions describing the same visual concept in an image. Previous studies treat VGP identification as a binary classification task, which ignores various phenomena behind VGPs (i.e., different linguistic interpretation of the same visual concept) such as linguistic paraphrases and VGPs from different aspects. In this paper, we propose semantic typology for VGPs, aiming to elucidate the VGP phenomena and deepen the understanding about how human beings interpret vision with language. We construct a large VGP dataset that annotates the class to which each VGP pair belongs according to our typology. In addition, we present a classification model that fuses language and visual features for VGP classification on our dataset. Experiments indicate that joint language and vision representation learning is important for VGP classification. We further demonstrate that our VGP typology can boost the performance of visually grounded textual entailment.}
}
```
