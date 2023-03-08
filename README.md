# Active-Learning-for-Text-Classification-using-Small-Text

## What is **Active Learning**?
**Active learning** is an approach in machine learning that aims to improve the prediction model by iteratively selecting the most informative unlabeled data points for inclusion in the training set. 
This is done by training a predictor and using it to choose examples that will increase the chances of finding better configurations and improving the model's accuracy. The process is repeated until a specified stopping criterion is met. 
**Active learning** is particularly useful in situations where labeled data is scarce, expensive, or requires domain expertise. 
It solves this problem by selecting unlabeled data points that are considered informative according to a query strategy and then having them labeled by an expert. [[1]](https://arxiv.org/pdf/1905.10336.pdf)
 [[2]](https://arxiv.org/pdf/2107.10314.pdf)

## Active Learning Process:

<p align="center" >
  <img src="https://lh3.googleusercontent.com/drive-viewer/AAOQEOQRxCx2m6-J_ePwYcySydc9G49PtM8K8k0kmN7EeO5SzFx3B3DWkgYOOHXXdqhntWEzA6IbHiwq1gLPbf8Qy-TlelqKeA=w1234-h961" width="400">
  <br>
  (Fig 1. Steps of active learning)
</p>

The steps to use active learning on an unlabelled dataset are: 
1. Manually annotate a subsample of the data;
2. Train the model on this labelled data;
3. Use the trained model to make predictions on unlabelled data;
4. Select the most informative unlabeled data points according to the chosen query strategy.

## Active Learning Loop:
<p align="center" >
  <img src="https://lh3.googleusercontent.com/u/2/drive-viewer/AAOQEOROg4eT3g41F_OpaqlGOwNilXvHEj4DcQoSG8WBnCgbuM4LKk8KEWqRRWf4GviP1ARS4D1u9igaeLhXnQqBeH-pUvsvRQ=w1920-h961" width="600">
  <br>
  (Fig 2. Active Learning Iterations)
</p>
