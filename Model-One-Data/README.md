# Mask Coverage Classification - Baseline Model
## Background 
The purpose of the model is to classify facial images into two classes. The first class is where the person is wearing the mask correctly, the other is when the person is exposing one of his/her nose mouth jaw-line. 

This model serves as a baseline comparison to the actual model that will be used eventually. Thus, a simple 3 layer CNN will be used. 
## Data Collection
The dataset contains 2 classes, incorrect and correctly worn masks. The data were retrieved from the following links: 

Correctly Worn Masks (CMFD): https://esigelec-my.sharepoint.com/:f:/g/personal/cabani_esigelec_fr/Ev3GdnQSyzxPjyzU5ElHqagBlkRCaKnnCI85iX-d1L4OHA?e=G7uaYV

Incorrectly Worn Masks (IMFD): https://esigelec-my.sharepoint.com/:f:/g/personal/cabani_esigelec_fr/EirjS8ew7-5LnO8I56Uk63wBKebwSlukFBFBaO8N25wn3g?e=Ho1jHG

## Data Cleaning 
A subfolder, containing around 946 images, of both classes is taken, constructing a total dataset of 1892 images. The images are divided into 378 validation images, 378 testing images, and 1136 training images. 
To ensure the model is not biased towards the color of the mask in the images, all images are converted into grayscale. This also makes training the CNN model faster since the input data would only have 1 channel. 

## Training 
<img width="653" alt="Screen Shot 2021-07-02 at 11 09 23 PM" src="https://user-images.githubusercontent.com/53017821/124341471-a5e2b500-db8a-11eb-9f37-3c020e85e118.png">
<img width="552" alt="Screen Shot 2021-07-02 at 11 09 35 PM" src="https://user-images.githubusercontent.com/53017821/124341476-af6c1d00-db8a-11eb-8684-e485434cded0.png">
The training was done for 20 epochs, and it is evident that at the 7th epoch, the model isn't underfitted nor overfitted. 


## Results with Testing Dataset 
With the model at its 7th epoch, a 95.5 percent test accuracy was achieved. However, another small set of images not from the CMFD or IMFD was loaded, and the model achieved only a 75% accuracy. This potentially due to the model being baised towards the style of images in the CMFD and IMFD.
