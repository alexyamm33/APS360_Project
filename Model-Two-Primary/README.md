# Mask Type Classification - Primary model
## Introduction
This real-time mask-type classification model aims to help improve compliance in different settings where different types of masks are required. In addition, it can be used to support disease transmission study by examining whether the degrees of transmission in a public setting is linked to the different types of masks present.

## Data Collection
The current dataset includes 3 classes: cloth, surgical, and N95. Over 4000 images were collected from the internet, and so far 480 bounding boxes have been manually drawn using [LabelImg](https://github.com/tzutalin/labelImg). 400 images were used for training, and 80 were used for testing.

## Model Selection and Training
This model uses transfer learning techniques by taking a pretrained model [ssd_mobilenet_v2](https://arxiv.org/abs/1512.02325) and fine-tuning its parameters to fit the new task. A total of 14k steps are run on Colab, and the metrics are tracked using Tensorboard.

## Results and Reflection
The model is tested with a webcam and shows reasonable accuracy when differenciating the different mask types. It has a precision score of 0.82 and a recall score of 0.84. One issue with the model is that it doesn't perform very well when the subject is too close or too far from the camera. More data will be collected to improve the accuracy and generalizability.

![cloth](samples/cloth_0701.PNG)
![surgical](samples/surgical_0701.PNG)
![n95](samples/n95_0701.PNG)
![prediction vs ground truth](samples/Tensorboard_0630_Detection_14k.PNG)
![loss](samples/Tensorboard_0630_Loss_1_14k.PNG)
![precision](samples/Tensorboard_0630_Precision_14k.PNG)
![recall](samples/Tensorboard_0630_Recall_14k.PNG)

The Colab Notebook, images, and Python scripts used in this model can be found in the following google drive folder: https://drive.google.com/drive/folders/1CqRUFq5GW--6YsqpW3gWHFq3hnTXeLg9?usp=sharing
