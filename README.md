# Plant disease classification

## The project is dedicated to plant disease classification, which is a multiclassification task. 

The model that predicts what disease a plant is affected by (if any) brings several interrelated values to the agriculture industry. It helps to save some part of the harvest by detecting the existence of disease, allowing us to take actions timely and cure the plant. In turn it would reduce the cost which usually arises when a part of the crops are dying. In addition, it saves the human workforce, because there would be no need to manually check if the plant is healthy, and the process would be automated. 

We could potentially estimate the exact financial effect of this project by focusing on the false negatives, since in our case the situation when we do not identify a disease leads to the loss of a plant and of a potential revenue. 

For the key metric of the model we use macro F1 score because it performs better with imbalanced data. It gives equal importance to each class.

For the project [dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset) from Kaggle was used.

## The results

We applied Transfer Learning, in particular:
* MobileNetV2
* VGG16
* ResNet50

We also tried 3 additional experiments with MobileNetV2 and data augmentation.

The best performing model that should be implemented is MobileNetV2 without data augmentation, with f1-score 0.9476.

For more details refer to: [report](https://docs.google.com/document/d/1vMK9aYg-x-QjHLC3myyAG3CdztyPL5iZyizEi1EB3vA/edit)
