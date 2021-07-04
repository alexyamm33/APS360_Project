# Mask Type Classification - Baseline Model
## Background
This model serves as simple baseline model that classifies images of mask-wearing persons into one of three mask categories: "n95", "surgical" or "other".

## The Dataset 
Raw images were obtained from the following sources:

* **SSDMNV2 2020 Model Data (withmask folder)** https://github.com/TheSSJ2612/Real-Time-Medical-Mask-Detection/releases/
* There were very few n95 images, so shutterstock was used to obtain some more n95 data. **Shutterstock** https://www.shutterstock.com/search/n95+mask
The raw data went through cleaning and augmentation. Then they were manually categorized into the types "n95 (and similar)", "surgical", and "other".

*More details about data collection can be read here: https://github.com/alexyamm33/APS360_Project/blob/main/ImageData/MaskType/Data_Collection-Model-Two-Baseline.md*

In the training and testing process of the baseline model, a total of 600 n95 mask images (70% real, 30% artificial), 1600 surgical mask images (real), and 600 other type masks (real) were used in training and testing the baseline model. These images were shuffled randomly using an internally written script and then split into training, validation, and testing datasets at a 60-20-20 ratio.

The model tuning process showed improved learning on greyscale images. The original dataset was converted into 3-channel greyscale prior to being used in training the model.

![image](https://user-images.githubusercontent.com/35859024/124389605-f60a6600-dcb5-11eb-9340-f91886013328.png)

![image](https://user-images.githubusercontent.com/35859024/124389356-ad05e200-dcb4-11eb-87ef-4da7319f776a.png)

## Training
(todo)

## Performance
(todo)
![image](https://user-images.githubusercontent.com/35859024/124390010-b17fca00-dcb7-11eb-85ba-b9fe1b5a16d1.png)
As seen above, one of the biggest flaws of this baseline model is the high training loss despite its relatively good training accuracy (>75%) and validation accuracy (~70%).

A goal for the team's model is to have a better loss-to-accuracy performance than the baseline.
