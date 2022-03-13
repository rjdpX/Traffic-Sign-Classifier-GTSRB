
# Traffic Sign Classifier using GTSRB dataset

<img src = "https://production-media.paperswithcode.com/datasets/GTSRB-0000000633-9ce3c5f6_Dki5Rsf.jpg" height = 400 width = 500>

Traffic sign classification is a systemic process of recognizing traffic signals which includes recognizing the merge signs, speed limit signs, stop signs  etc. allowing a self driving car to better optimize perform in such given scenarios and help navigate through obstacles if any.

The most challenging part in any machine learning project is data creation and cleansing wherein for this project, we will be working on a German traffic sign dataset and process will comprise of

    1. Loading the data
    2. Building the model
    3. Training the model
    4. Evaluating the model using different metrics
    5. Generating the classification report
    6. Visualizing the predicted v/s actual test output

Before diving further, we’ll look into the dataset and understand how it’s being structured.

### GTSRB | German Traffic Sign Recognition Benchmark

    -   Contains 43 classes of traffic signs
    -   Split into 39,209 training images
    -   and 12,630 test images
    -   Images having varying light conditions and rich backgrounds

The traffic sign classification is a two-step process which includes:

    • Localization
    • Recognition

Localization is where the machine would be able to see and actually localize the traffic sign in the given state and Recognition relates to recognize the ROI in the image and classify it to which class it belongs.
## Workflow

In this project, we have first analyzed the data before proceeding further. We’ll also futher looked into a sample set of images to get a better insight of the images present in the dataset.
-   After this, we fetched the training data from “Train/...” taking reference from ‘train.csv”. It is good to note that similar task has been performed for fetching test data.
-   After fetching, we performed preprocessing which includes shuffling the data, splitting the data into training set and validation set in the ratio of 0.3. We’ve also scaled down the image data and type casting has been performed to float32 inorder to reduce computational requirement.
-   The next step involves creating the model for performing training and testing operation.
      
    -   We’ve used two convolutions of 16 and 32 neurons each, having relu activation. Then, we added a layer of MaxPool and a BatchNorm.  
    -   Then, we used one convolution layer of 16 neurons followed by two subsequent layers of covolution of 128 neurons, each having activation of relu function, ending this stack by using a layer of MaxPooling and BatchNormalization.
          
    -   After performing multiple convolutions, we’ve used dense layer of 512 neurons and 43 neurons post performing flattening them and introduced dropout and BatchNorm between the dense layers.

Note: In every convolution layer, we’ve used kernel size of (3X3) and for MaxPooling, we have used pool size of (2X2).
-   Next step, involves compiling the model, training the model with the training set and validation set along with inclusion of some augmentations in the process to generalize the model properly.
-   We thereby, complete the project after evaluating the model using different metrics from sklearn and also observed the prediced and actual class ids on a few test images as shown below.

## Challenges

While working on this project, I have faced challenges on creating the model, and deciding which layers to use to attain greater accuracy. I had tune values for different hyperparameters like the learning rate, batch size and epochs, and sometimes end up in changing few of the layers itself in the model, also referred few of the sources from Kaggle to see how others have selected the layers and the hyperparameters. 

However, I was able to achieve quite satisfactory result and thereby using this experience I am now able to perform more such computer vision projects with utmost accuracy.

[See the project](https://github.com/rjdpX/Traffic-Sign-Classifier-GTSRB/blob/master/Custom_Traffic_Sign_Classifier.ipynb)


## Authors
Connect with Rajdeep:

- [@rjdpX](https://github.com/rjdpX/rjdpX)

- [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rajdeepforreal/)

- [![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](https://mail.google.com/mail/u/0/?tab=rm&ogbl#inbox)
