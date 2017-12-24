---
layout: post
title: Applying Deep Learning to Real-world Problems - Medium post summary
---

Applying Deep Learning to Real-world Problems is a [post](https://medium.com/merantix/applying-deep-learning-to-real-world-problems-ba2d86ac5837) in medium by [Rasmus Rothe](https://medium.com/@rasmus.rothe?source=post_header_lockup). It gives 3 lessons from work at Merantix. Here are the summary for the post.

## Weakly labeled data

> As we fine-tune on precisely labeled data, it is possible to pre-train on so-called weakly labeled data. By this we refer to data which labels are not in all cases correct (i.e. 90% of the labels might be correct and 10% wrong). The advantage is that this kind of data can often be obtained without any human involved in labeling but automatically. This makes this data relatively cheap compared to data where a human needs to label every single image. To give an example: during my PhD, I crawled a dataset of 500k face imagesfrom Wikipedia and IMDb. We combine the date of birth of a person in the profile and any hint in the caption of the photos when it was taken. This way we can assign an approximate age to each image. Note that in some cases the year in the caption below the image might have been wrong or the photo might show several people and the face detector selected the wrong face. Thus we cannot guarantee that in all cases the age label is correct. Nonetheless we showed that pre-training on this weakly labeled dataset helped to improve the performance versus just training on a precisely labeled smaller dataset.

## Unbalanced label distribution

- Academic datasets are always balanced (Ex. No of samples for each class are equal)
- Most of real world applications has unbalanced data for example:
  - Medical vision: training data for medical imaging is very skewed. The majority of patients are healthy, while only a small fraction of the patients suffer from a certain disease.
- How to solve this issue:
  - More data (Collect more data of the rare class for example)
  - Change labeling (Ex. Add some labels together)
  - Ignore Sampling (Ignore the samples that has more frequency)
  - Over- or undersample. (Ex. Duplicate the samples of the less class)
  - Weighting the loss (Weight the samples the are less with more than the others)

## Understanding black box models

- Deep learning architecture are hard and complex to understand.
- Some models can be fooled and that's not a good security.
- Picasso Tool:
  - A CNN model visualizer.
  - Good for understanding what is happening or why a specific example fails while other succeed.
  - You can find it here: https://github.com/merantix/picasso

<br/>

<br/>

## References

- https://medium.com/merantix/applying-deep-learning-to-real-world-problems-ba2d86ac5837
- https://github.com/merantix/picasso
- https://medium.com/merantix/picasso-a-free-open-source-visualizer-for-cnns-d8ed3a35cfc5