# Active-Learning-for-Text-Classification-using-Small-Text

## What is **Active Learning**?
**Active learning** is an approach in machine learning that aims to improve the prediction model by iteratively selecting the most informative unlabeled data points for inclusion in the training set. 
This is done by training a predictor and using it to choose examples that will increase the chances of finding better configurations and improving the model's accuracy. The process is repeated until a specified stopping criterion is met. 
**Active learning** is particularly useful in situations where labeled data is scarce, expensive, or requires domain expertise. 
It solves this problem by selecting unlabeled data points that are considered informative according to a query strategy and then having them labeled by an expert. [[1](https://arxiv.org/pdf/1905.10336.pdf), [2](https://arxiv.org/pdf/2107.10314.pdf)]

## Active Learning Process:

<p align="center" >
  <img src="https://lh3.googleusercontent.com/drive-viewer/AAOQEORNch-F36ROGEBY6eFr1LhxK96tJqtFRvZUwpZ-iEdIeDBrjSp4n5CV3o5kGeDFKwILgxleVo9PpbTuBB_2SSO7LF3liw=w1920-h961" width="400">
  <br>
  (Fig 1. Steps of active learning)
</p>

The steps to use active learning on an unlabelled dataset are: 
1. **Annotating**: Manually annotate a subsample of the data;
2. **Training**: Train the model on this labelled data;
3. **Predicting**: Use the trained model to make predictions on unlabelled data;
4. **Querying**: Select the most informative unlabeled data points according to the chosen query strategy.

## Active Learning Loop:
<p align="center" >
  <img src="https://lh3.googleusercontent.com/u/2/drive-viewer/AAOQEOROg4eT3g41F_OpaqlGOwNilXvHEj4DcQoSG8WBnCgbuM4LKk8KEWqRRWf4GviP1ARS4D1u9igaeLhXnQqBeH-pUvsvRQ=w1920-h961" width="600">
  <br>
  (Fig 2. Evolution of The Dataset at each Iteration)
</p>

The active learning loop consists of the following steps:

1. **Training a predictor**: A prediction model is initially trained on a small subset of labeled data.

2. **Selecting unlabeled data points**: The predictor is used to score and rank the remaining unlabeled data points based on their informativeness.

3. **Querying for labels**: The most informative data points are selected for labeling by an expert. These data points are chosen based on a query strategy that maximizes the expected reduction in prediction error.

3. **Incorporating labeled data**: The newly labeled data points are added to the labeled training set, and a new predictor is trained using all labeled data points.

4. **Evaluating stopping criterion**: The model's performance is evaluated on a validation set, and the active learning process is repeated until a specified stopping criterion is met.

5. **Stopping criterion**: The stopping criterion can be based on various factors, such as a fixed number of iterations, the performance of the model on the validation set, or a threshold for the amount of improvement achieved in model performance.

By iteratively selecting the most informative unlabeled data points for labeling and incorporating them into the training set, active learning aims to achieve high model performance with less labeled data than would be required by traditional supervised learning approaches.

## About the Small-Text Library:

**Small-Text** provides state-of-the-art Active Learning for Text Classification. Several pre-implemented Query Strategies, Initialization Strategies, and Stopping Critera are provided, which can be easily mixed and matched to build active learning experiments or applications.

###  Small-Text Features
 - Provides unified interfaces for Active Learning so that you can easily mix and match query strategies with classifiers provided by [sklearn](https://scikit-learn.org/), [Pytorch](https://pytorch.org/), or [transformers](https://github.com/huggingface/transformers).
 - Supports GPU-based [Pytorch](https://pytorch.org/) models and integrates [transformers](https://github.com/huggingface/transformers) so that you can use state-of-the-art Text Classification models for Active Learning.
 - GPU is supported but not required. In case of a CPU-only use case, a lightweight installation only requires a minimal set of dependencies.
 - Multiple scientifically evaluated components are pre-implemented and ready to use (Query Strategies, Initialization Strategies, and Stopping Criteria).

## About this project:

This project consists of a notebook illustrating a simple example of how to perform **Active Learning** for text classification with [small-text](https://github.com/webis-de/small-text/tree/v1.3.0) using [sklearn](https://scikit-learn.org/) models and the [rotten tomatoes dataset](https://huggingface.co/datasets/rotten_tomatoes).
