# Papers Related to Semi-Supervised Long-tail Recognition
## Semi-supervised Long-tail Recognition

### CReST: A Class-Rebalancing Self-Training Framework for Imbalanced Semi-Supervised Learning(CVPR-21) [[link](https://arxiv.org/abs/2102.09559)]
* Vanilla models have high precision but low recall on tail classes
* Periodically add samples from unlabeled sets to labeled sets based on inverse class frequency
* Reinitialize and Retrain the network after each generation
* Progressive Distribution Alignment

### Semi-supervised Long-tailed Recognition using Alternate Sampling(ICCV-21 Rejected, ICLR-22 in submission)[[link](https://arxiv.org/abs/2105.00133)]
* One feature extractor f, one class-balanced classifier g, another auxiliary classifier g'
* use f+g to assign pseudo-labels; train f+g' under semi-supervised settings; finetune f+g on labeled data

### Distribution aligning refinery of pseudo-label for imbalanced semi-supervised learning(Neurips-20)[[link](https://arxiv.org/abs/2007.08844)]
* Refining pseudo-labels so that the class distribution of pseudo-labels matches ground-truth class distribution of unlabeled data
* Not sure why this is helpful because the ground-truth class distribution of unlabeled data is also long-tail
* Estimating grount-truth class distribution of unlabeled data but basically it's just using the information of labeled sets

### Unifying Distribution Alignment as a Loss for Imbalanced Semi-supervised Learning(ICLR-22 in submission)[[link](https://openreview.net/forum?id=HHUSDJb_4KJ)
* Better explanation of distribution alignment(Section 2.2)]
* use logit adjustment for both supervised and unsuperivsed branch
* Use ema of pseudo-labels as target distribution for both branches.

## Supervised Long-tail Recognition

### Rethinking the Value of Labels for Improving Class-Imbalanced Learning [[link](https://arxiv.org/abs/2006.07529)]
* semi-supervised learning(additional unlabeled data) can help the imbalance learning
* self-supervised learning(pretraining + finetune) can also help the imbalance learning

### Long-tail learning via logit adjustment [[link](https://arxiv.org/abs/2007.07314)]

### Balanced Meta-Softmax for Long-Tailed Visual Recognition[[link](https://arxiv.org/abs/2007.10740)]
* Introduced Balanced Softmax--multiplying the number of instances to logits then normalize
* A meta sampler: a learnable batch sampler through meta learning

### Learning Imbalanced Datasets with Label-Distribution-Aware Margin Loss [link](https://arxiv.org/abs/1906.07413)
* A modified loss term for imbalance learning

### Decoupling representation and classifier for long-tailed recognition [link](https://arxiv.org/abs/1910.09217)
* train a model(feature extractor + classifier) with different sampling strategies
* Train a balanced classifier: (1) retrain a linear classifier with class-balanced manner, (2) non-parametric nearest class mean classifier, and 
(3) normalizing the classifier weights

## Semi-supervised Learning

### Mean teachers are better role models: Weight-averaged consistency targets improve semi-supervised deep learning results[[link](https://arxiv.org/abs/1703.01780)]
* Use EMA to obtain a teacher model

### FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence [[link](https://arxiv.org/abs/2001.07685)]
### Unsupervised Data Augmentation for Consistency Training [[link](https://arxiv.org/abs/1904.12848)]
* use weak augmentation to obtain artificial labels
* train models with strongly augmented images and artificial labels

### MixMatch: A Holistic Approach to Semi-Supervised Learning [[link](https://arxiv.org/abs/1905.02249)]
* Use mixup to belend labeled and unlabeled set
* Sharpening predictions of unlabeled examples

### ReMixMatch: Semi-Supervised Learning with Distribution Alignment and Augmentation Anchoring [[link](https://arxiv.org/abs/1911.09785)]
* Distribution Alignment




