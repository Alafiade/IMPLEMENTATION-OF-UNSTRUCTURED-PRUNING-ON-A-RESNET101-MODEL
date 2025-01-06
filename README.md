# IMPLEMENTATION-OF-UNSTRUCTURED-PRUNING-ON-A-RESNET101-MODEL

## Overview 
This project implements an unstructured pruning technique, specifically **magnitude-based pruning** on a ResNet-101 model. The goal is to reduce the model size while maintaining its performance. The model was initially trained for  20epochs, followed by pruning 20% of the weights and fine-tuning the pruned model.

## Model Training
The ResNet-101 model was trained on a dataset for 20 epochs. Here are the training results:

- **Epoch 1**:
  - Training Loss: 0.9187
  - Training Accuracy: 0.8621
  - Validation Loss: 0.0384
  - Validation Accuracy: 0.9876

- **Epoch 20**:
  - Training Loss: 0.0159
  - Training Accuracy: 0.9940
  - Validation Loss: 0.0096
  - Validation Accuracy: 0.9982
 
**Performance Over Epochs**
-The model shows a consistent decrease in both training and validation loss over the epochs.
-The validation accuracy reaches a high of 99.82% by the end of training, suggesting excellent generalization to unseen data.

**Pruned Model Training Results**
Summary of Metrics
Epochs: 15
Final Training Loss: 0.0231
Final Training Accuracy: 99.29%
Final Validation Loss: 0.0115
Final Validation Accuracy: 99.65%

**Performance Over Epochs**
-The pruned model also shows a decrease in both training and validation loss, though not as pronounced in the unpruned model.
-The final validation accuracy is slightly lower than that of the unpruned model but remains very high at 99.65%.
**Observations**
-The initial training loss is higher (0.0721) compared to the unpruned model's first epoch but decreases steadily.
-The pruned model achieved early stopping after the 14th epoch, indicating that it reached optimal performance before completing all planned epochs.

**Key Points**
- The unnpruned model took longer to train compared to the pruned model which indicates that the pruning led to a more efficient training process without significant loss in performance.
- The unpruned model achieved slightly better final metrics, but the pruned model still performed exceptionally well indicating the pruning technique did not severely impact its ability to generalize.
- An early stopping mechanism was triggered in the pruned model, suggesting that it  reached an optimal point where further training would not produce significant improvements.
