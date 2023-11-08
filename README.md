# WikiTiLo: Can Vision-Language Models Be a Good Guesser? Exploring VLMs for Times and Location Reasoning 

[paper](https://arxiv.org/abs/2307.06166)

Can Vision-Language Models(VLM), which are pre-trained with large-scale image-text resources, inference the shooting location and time of a photo like human capability?

To address this question, we propose a two-stage RECOGNITION & REASONING probing task applied to discriminative and generative VLMs to uncover whether VLMs can recognize times and location relevant features based on visual cues and further reason about it.

For this task, we construct a new dataset, WikiTiLo(**Wiki**Common **Ti**mes and **Lo**cation), which comprises images captured over a broad time range and is geographically balanced to mitigate cultural bias. The dataset has been carefully curated to ensure that each image contains distinct visual cues that align with human expert knowledge.

We evaluated three discriminative VLMs and two generative VLMs on WikiTiLo. Experiments show that visual encoders in discriminative VLMs can generate context-agnostic visual features that help identify times/locations, but generative VLMs fail to reason based on the visual cues. Here is the results table of performance without training(0-shot) for RECOGNITION and REASONING, compared to the Frequency baseline and human baseline.
![image](https://github.com/gengyuanmax/WikiTiLo/blob/main/images/results.png)

## Dataset
![image](https://github.com/gengyuanmax/WikiTiLo/blob/main/images/samples.png)

The WikiTiLo dataset[(download from huggingface repo)](https://huggingface.co/datasets/gengyuanmax/WikiTiLo) consists of 6296 images with annotation of the specific time and country where images are taken. There are some samples from WikiTiLo above. The dataset covers 30 countries in 8 regions, and the years from 1826 to 2021. we split 80% of the entire dataset as the training set, 10% as the validation set, and 10% as the test set. In the following charts, we demonstrate all the countries and regions in WikiTiLo, and the distribution of the location and time labels.

<img src="https://github.com/gengyuanmax/WikiTiLo/blob/main/images/countries.png" width="500px">
<img src="https://github.com/gengyuanmax/WikiTiLo/blob/main/images/distribution.png" width="500px">


## Citation
```
@misc{zhang2023visionlanguage,
      title={Can Vision-Language Models be a Good Guesser? Exploring VLMs for Times and Location Reasoning}, 
      author={Gengyuan Zhang and Yurui Zhang and Kerui Zhang and Volker Tresp},
      year={2023},
      eprint={2307.06166},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
