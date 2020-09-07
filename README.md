# Korean Movie Review Emotion (KMRE) Dataset

[LREC 2020]: https://lrec2020.lrec-conf.org/en/

We develop a large-scale emotion-labeled dataset, called the Korean Movie Review Emotion (KMRE) dataset. The method for constructing this dataset is described in detail in our paper which is accepted by [LREC 2020].

<pre>
@inproceedings{lee2020korean,
  title={Korean-Specific Emotion Annotation Procedure Using N-Gram-Based Distant Supervision and Korean-Specific-Feature-Based Distant Supervision},
  author={Lee, Young-Jun and Lim, Chae-Gyun and Choi, Ho-Jin},
  booktitle={Proceedings of The 12th Language Resources and Evaluation Conference},
  pages={1603--1610},
  year={2020}
}
</pre>

## Overview

[here]: https://github.com/e9t/nsmc

We construct the KMRE dataset annotated with six types of emotions by applying our presented procedure to the Naver Sentiment Movie Corpus (NSMC) in Korean. The detail of NSMC is described in [here]. Additionally, we constructed the KMRE dataset by exploiting n-gram-based distant supervision and Korean-specific-features-based distant supervision.
  
## Statistics

The statistics of the KMRE dataset is as follows:

|             | # of sentence | Anger | Disgust | Fear | Happiness | Sadness | Surprise |
|:-----------:|:-------------:|:-----:|:-------:|:----:|:---------:|:-------:|:--------:|
|   Training  |    119,995    | 29.88 |   9.84  | 8.42 |   20.36   |  23.93  |   7.57   |
| Development |     29,999    | 29.86 |   9.6   | 8.44 |   20.35   |  24.17  |   7.58   |
|   Testing   |     49,997    | 29.82 |   9.93  | 8.32 |   20.35   |   24.0  |   7.58   |

Table shows the number of sentence per dataset and emotion distributions (\%) of KMRE dataset.

## Features

- The KMRE dataset has six types of emotions except the emotion *neutral*, because there were no neutral reviews in the NSMC
  - Anger, Disgust, Fear, Happiness, Sadness, Surprise
  
  
- Each file was stored in the pickle module

```python
import pickle as pc

with open('data/kmre_train', 'rb') as f:
    kmre_train_data = pc.load(f)
```

## Contact

If you have any questions or comments, please send an email to the contact you want below.

- KAIST E-mail: yj2961@kaist.ac.kr
- Gmail: passing2961@kaist.ac.kr
