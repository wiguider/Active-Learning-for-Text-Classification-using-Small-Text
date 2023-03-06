# Active-Learning-for-Text-Classification-using-Small-Text

## What is **Active Learning**?
**Active learning** is a special case of machine learning in which a learning algorithm can interactively query a user to label new data points with the desired outputs. 

**Active learning** involves selecting the most valuable data samples from an unlabeled database for annotation by the user (query)

## Active Learning Step-by-Step:

<p align="center" >
  <img src="https://lh3.googleusercontent.com/drive-viewer/AAOQEOQRxCx2m6-J_ePwYcySydc9G49PtM8K8k0kmN7EeO5SzFx3B3DWkgYOOHXXdqhntWEzA6IbHiwq1gLPbf8Qy-TlelqKeA=w1234-h961" width="400">
  <br>
  (Fig 1. Steps of active learning)
</p>

The steps to use active learning on an unlabelled dataset are: 
1. Manually label a very small subsample of the data;
2. Train the model on this small amount of labelled data;
3. Make predictions on unlabelled data;
4. Select unfamiliar and uncertain samples for training that are most valuable to improve the current model.

<p align="center" >
  <img src="https://lh3.googleusercontent.com/u/2/drive-viewer/AAOQEOROg4eT3g41F_OpaqlGOwNilXvHEj4DcQoSG8WBnCgbuM4LKk8KEWqRRWf4GviP1ARS4D1u9igaeLhXnQqBeH-pUvsvRQ=w1920-h961" width="600">
  <br>
  (Fig 2. Active Learning Iterations)
</p>
