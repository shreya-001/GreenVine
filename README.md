# GreenVine: Early Plant Disease Detection
<hr>

## About Dataset - 
Link to the dataset: https://data.mendeley.com/datasets/89cnxc58kj/1
- Authors collected the dataset of the grapevine leaf images categorizing into two, healthy and unhealty. The images are captured manually using 2 smartphones and 1 tablet.
- The images exhibit resolution of 1920x1080 pixels and 1280x720 pixels by both portrait and landscape orientation.
- The dataset comprises of 1770 images and is structured within the main folder "esca_dataset", which containts 2 subfolders "healthy"(882 images) and "unhealthy"(888 images)    

## Solution - 
When working with deep learning alot of data is required, since the data is only 1770, image augmentation is the way to go.
    `Augmentation is the technique which transforms existing images and will create new images.`

## Image Augmentation - 
1. Each of the images in healthy and unhealty folders are augmented which is then saved to a folder called as "Augmented".
2. Under Augmented Folder I created two new folders called "Healthy_aug" and "Unhealthy_aug".
3. Once the transformation is completed, the original healthy images and augmented healthy images are moved to a new folder called "Healthy_new". 
4. 3rd step is repeated for the unhealthy images.

> With the help of the above steps we were able to increase the size of the dataset.

After the augmentation the distribution between healthy and unhealthy images are 49.8% and 50.2% respectively. 

## Image Pre-processing 
- Before feeding the images to the model it is necessary to preprocess the images, since all the images are of different resolutions we will resize all the images to 256x256. 
- After reshaping the images healthy and unhealthy images are concatenated into one variable. 
- **Image Labelling** - labeled all the healthy images as zeros and unhealthy as ones
- Did numpy flattening to get the 2D array where each row represents an image and each column represents the pixel value.
