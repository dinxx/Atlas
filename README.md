# ATLAS - Constrained Beam Search Based Sequence model for product category classification

This project aims to predict the taxonomy of an image through Attention Sequence model.

## Architecture Blueprint
![alt text](https://github.com/vumaasha/Atlas/blob/master/img/blueprint.png "Architecture")

## How do I use this Project?
![alt text](https://github.com/vumaasha/Atlas/blob/master/img/Path.png "Path")

There are 2 ways you can use this Project:

1. Path 1
    1. [Use Atlas Dataset](../blob/master/dataset/README.md)
    2. [Run the pre-trained model](../blob/master/models/apparel_classification/README.md)

2. Path 2
    1. [Use Custom Dataset](../blob/master/dataset/README.md)
    2. Run model to generate new Taxonomy
      * [Clean Dataset](../blob/master/models/normal_vs_zoomed/README.md)
      * [Run Model](../blob/master/models/apparel_classification/README.md)
      
    
The code has been segregated into 2 parts:
1. Dataset 
    - Data Collection
2. Model
    - Data Cleaning - Segregating Zoomed and Normal images
    - Model - Data Normalization and taxonomy prediction


## 1. Dataset - Data Collection
You will be creating the dataset of images required to run the model.

The folder size containing the images is too large to upload on Github. Instead, we have added a _.json file that contains the image urls. 

To automatically download the images to the destination folder (i.e dataset folder), run the _script.py .

`python _script.py`

## 2. Model
### Data Cleaning - Segregating Zoomed and Normal images
Observe that the downloaded images vary in size and scale. In this section of code, we will be solving the issue related with scale of the image. 

For the model to learn, we will require images of apparel that is normal i.e not zoomed. With zoomed images, it is difficult to identify the apparel as a zoomed image is a close-up snap and the shape associated with the apparel cannot be observed clearly.

Before running the zoomed_vs_normal model, we will first have to generate the h5 file associated with it. 
