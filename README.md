# Plant disease classification

This README.md file contains information about:
* the goal of the project
* source data
* results that were obtained
* contributors

## The goal of the project was:
* To build a model for plant disease classification (to solve a multiclass classification task).

The model that predicts what disease a plant is affected by (if any) brings several interrelated values to the agriculture industry. It helps to save some part of the harvest by detecting the existence of disease, allowing us to take actions timely and cure the plant. In turn it would reduce the cost which usually arises when a part of the crops are dying. In addition, it saves the human workforce, because there would be no need to manually check if the plant is healthy, and the process would be automated. 

We could potentially estimate the exact financial effect of this project by focusing on the false negatives, since in our case the situation when we do not identify a disease leads to the loss of a plant and of a potential revenue. 

For the key metric of the model we use macro f1-score because it performs better with imbalanced data. It gives equal importance to each class.

## Data
The data is represented by pictures of plants (with 256x256 pixels) and their names and names of their diseases. 

![](https://github.com/annasemenova15/Plant_disease_detection/blob/main/images/eda2.png)

The data is indeed imbalanced, because there are some classes that prevail.

![](https://github.com/annasemenova15/Plant_disease_detection/blob/main/images/eda1.png)
For the project [dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset) from Kaggle was used.

## The results that were obtained

We applied Transfer Learning, in particular:
* MobileNetV2
* ResNet50
* VGG16

Results are provided below:
|  Type of model                                                               | Loss (test data)     | Macro F1 score (test data) |
| :----------------------------------------------------------------------------| :------------------- | :--------------------------| 
| *MobileNetV2 without data augmentation*                                      | *0.1553*             | *0.9476*                   | 
| MobileNetV2 with data augmentation                                           | 0.1557               | 0.9452                     |
| MobileNetV2 experiment 3 (learning rate = 0.001)                             | 0.1884               | 0.9381                     |
| VGG16                                                                        | 0.2692               | 0.9063                     |
| MobileNetV2 experiment 2 (learning rate = 0.00001, dropout = 0.4, epochs = 7)| 0.3543               | 0.8791                     |
| MobileNetV2 experiment 1 (learning rate = 0.00001, dropout = 0.5, epochs = 7)| 0.4561               | 0.8396                     |
| ResNet50                                                                     | 0.6320               | 0.7911                     |

The best performing model that should be implemented is MobileNetV2 without data augmentation, with test f1-score 0.9476.

For more details refer to model detailed: [report](https://docs.google.com/document/d/1iJiMktWUZXydXqZtNnIwS2_R5t52qz3mQrxV4VnlzuE/edit)

## Contributors for this project are students of 2nd year of Business analytics and Big Data Master's program:
- Anna Semenova

![alt text](https://github.com/annasemenova15/Plant_disease_detection/blob/main/images/Anna.png)
- Elizaveta Sivash

![](https://github.com/annasemenova15/Plant_disease_detection/blob/main/images/Elizaveta.png)
- Anastasiia Panchenko

![](https://github.com/annasemenova15/Plant_disease_detection/blob/main/images/Anastasiia.png)
