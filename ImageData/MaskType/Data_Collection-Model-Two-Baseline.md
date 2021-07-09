# Data collection (Mask Type Classification - Baseline Model)
A detailing of the image data that was used to train, validate, and test the classification models used to identify the type of mask being worn.

Raw images were used from the following sources:
* **SSDMNV2 2020 Model Data (withmask folder)** https://github.com/TheSSJ2612/Real-Time-Medical-Mask-Detection/releases/
There were very few n95 images, so shutterstock was used to obtain some more n95 data.
* **Shutterstock** https://www.shutterstock.com/search/n95+mask

The types of masks were split into three categories:
* *n95*: any mask that looks like n95 or of a similar type, including 3m 9001v
* *surgical*: any mask whose shape matches surgical masks and is not made up of cloth
* *other*: any mask that does not belong into the above categories, including cloth masks and bandanas

The raw data was sorted manually (labeled manually) into the category of mask. Cleaning of the data was performed, including discarding images of people not wearing any masks, images that were too blurry, images where too much of the face and mask were cropped out, images where the type of mask being worn was too confusing to a human (chances of error in manual labeling would be high, thereby potentially confusing the model), and cropping out images such that there was only one human wearing one kind of mask in the image. Augmentation methods were used to increase dataset size, including rotating, shifting pixels, and flipping across the vertical axis of symmetry. 

A total of 600 n95 mask images (70% real, 30% artificial), 1500 surgical mask images (real), and 1660 other type masks (real) were obtained. In order to have a balanced dataset, 600 images were selected randomly and used from the surgical and other categories. The data was shuffled randomly using an internally written script and then split into training, validation, and testing datasets at a 60-20-20 ratio.

Since files were greater than 25MB, they were uploaded to google drive instead of GitHub.
They can be accessed at the links below:
* n95's and similar: https://drive.google.com/file/d/1JOh-U3g6E93KirrRim3PAQCqoQN9yaAk/view?usp=sharing
* surgical masks: https://drive.google.com/file/d/1JjyhENNeqKmykIsBSpW7ZJJ-qGgR4MLL/view?usp=sharing
* other (non N95 and similar, non surgical): https://drive.google.com/file/d/1-tYM8rdizsqPWZI0ISh-NFg-RisZhxuJ/view?usp=sharing
