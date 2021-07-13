# Mask Type Classification - Baseline Model
## Background
This model serves as simple baseline model that classifies images of mask-wearing persons into one of three mask categories: "n95", "surgical" or "other". This model is a 3-layer CNN that uses ALEXNET transfer learning.

## The Dataset 
Raw images were obtained from the following sources:

* **SSDMNV2 2020 Model Data (withmask folder)** https://github.com/TheSSJ2612/Real-Time-Medical-Mask-Detection/releases/
* There were very few n95 images, so shutterstock was used to obtain some more n95 data. **Shutterstock** https://www.shutterstock.com/search/n95+mask
The raw data went through cleaning and augmentation. Then they were manually categorized into the types "n95 (and similar)", "surgical", and "other".

*More details about data collection can be read here: https://github.com/alexyamm33/APS360_Project/blob/main/ImageData/MaskType/Data_Collection-Model-Two-Baseline.md*

In the training and testing process of the baseline model, a total of 600 n95 mask images (70% real, 30% artificial), 1600 surgical mask images (real), and 600 other type masks (real) were used in training and testing the baseline model. These images were shuffled randomly using an internally written script and then split into training, validation, and testing datasets at a 60-20-20 ratio.

The model tuning process showed improved learning on greyscale images. The original dataset was converted into 3-channel greyscale prior to being used in training the model.

*Dataset split*

![image](https://user-images.githubusercontent.com/35859024/124389605-f60a6600-dcb5-11eb-9340-f91886013328.png)

*A sample of the training dataset*

![image](https://user-images.githubusercontent.com/35859024/124389356-ad05e200-dcb4-11eb-87ef-4da7319f776a.png)

## Training
This simple 3-layer CNN baseline model with ALEXNET transfer learning was trained over 15 epochs. L2 regularization was used because of its smoother validation accuracy performance.

*Training results*

![image](https://user-images.githubusercontent.com/35859024/124391042-9bc0d380-dcbc-11eb-863b-57026b3a1f2b.png)

*Applying L2 regularization effect*

![image](https://user-images.githubusercontent.com/35859024/125529542-5aad6b3c-bf2d-457f-a52f-314706b0e211.png)

## Performance

One of the biggest flaws of this baseline model is the high training loss (>100%) despite its relatively good training accuracy (>75%) and validation accuracy (~70%). A goal for the team's model is to have a better loss-to-accuracy performance than the baseline.

*Comparing model loss to accuracy*

![image](https://user-images.githubusercontent.com/35859024/125529843-e79860f1-965c-449d-9c6c-95b5f7b05d1b.png)

After tuning hyperparameters, the final ALEXNET baseline model has a 69.5% testing accuracy.

*Test results*

![image](https://user-images.githubusercontent.com/35859024/125530291-f159786c-5a8c-4b8b-896c-fcf3325266f2.png)


