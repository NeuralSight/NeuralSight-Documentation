---
title: Installation & Project SetUp
weight: 15
---


{{% notice note %}}
* **Item Name**: NeuralSight AI
* **Item Version**: V 1.0.0
* **Authors**: Paul N. Mwaura & Stephen Kamau
* **Support Forum**: https://neurallabs.africa
* **Contact Us**: info@neurallabs.africa
* **License**: GPL-3 License
{{% /notice %}}


The following steps are here to help you initialize your new website. If you don't know Hugo at allFirst of all, 
Thank you so much for your amazing project. You are awesome!
You are entitled to contribute and get free code updates to this product + exceptional support from the author directly.
You will learn more about NeuralSight AI by following this [Neural Labs Africa](https://neurallabs.africa/).


### Table of contents:
* Getting Started
* NeuralSight AI Intro
* Set Up Locally
* Install Dependencies
* Generating CSV File
* Data Pre_Processing for YOLO
* Data Modelling
* Copyright and License

## Introduction

First of all, Thank you so much for your amazing project. You are awesome!
You are entitled to contribute and get free code updates to this product + exceptional support from the author directly.

This documentation is to help you regarding each step of setting up and running it locally. Please go through the 
documentation carefully to understand how to setup properly. Python knowledge is required to setup and contribute to this project.
You may learn basics of [Python Documentation here](https://www.python.org/) and [Python Tutorial here](https://www.learnpython.org/).

## Requirements
You will need the following softwares to get started.

Code Editing Software (eg: Visual Studio Code, Pycharm Community version or Notepad)
Google Colab for free access to cloud GPU

{{% notice note %}}
Be careful while installing dependencies. If not installed properly, the code may break completely. We would recommend setting up a virtual environment.
No support is provided for older libraries not included in the dependencies.
{{% /notice %}}

## Getting Started
### Easy to Use
NeuralSight is an Intelligent tool that offers a great opportunity to enhance and augment radiology services thereby relieving the bottleneck in medical imaging diagnosis. NeuralSight provides a high-level web-interface equipped with advanced annotation tools and project management features. NeuralSight was designed from the ground up to enhance the radiology workflow and reduce backlogs in the workflow.

### Focus on What Matters
NeuralSight™ provides automated interpretation of radiology exams like CXRs, CTs and MRI scans to identify pathologies and diseases such as Pneumothorax, Cardiomegaly, Benign breast Tumour, Malignant breast Cancer, Atelectasis, Infiltration, Emphysema, Mass/Nodule, Pleural Thickening, Effusion, Consolidation, Tuberculosis, Pneumonia, Prostate and Lung cancer.

### Our Impact
To provide a thorough and actionable innovation artificial intelligence solutions that will help the healthcare sector achieve its objectives. reduces workload and thereby eases such costs and provides a friendly pricing model to patients. Offering affordable health care services will ensure that everyone, even those in marginalised communities, are able to receive healthcare services. AI to solve the overwhelming UN Strategic Development Goal 3 Good Health and Wellbeing has the potential to ensure that Africa improves its healthcare system.

### The Tool
NEURALSIGHT system is a combination of YOLOv5 trained model and a set of endpoints that allows users to detect 14 Chest X-ray pathologies. The model is trained using a VinBig dataset of X-ray images and annotations of the 14 pathologies of interest. The model is able to predict bounding boxes and class probabilities for each object (pathology) in an image. The endpoints allow users to perform tasks such as logging in and uploading images for prediction, as well as viewing and downloading the prediction results and reports. The model is already trained hence the users only require to upload their XRAY images and be able to get response as the prediction and reports. The model has been evaluated on a test dataset and has shown to have good performance in terms of metrics such as average precision and mean average precision. The model is deployed using FastAPI, which is a lightweight web framework for building web applications and APIs, and is easily integrated with other technologies.

## Data
### Dataset Description
For this dataset, the main aim was to come up with an object classifying system for common thoracic lung diseases and localizing critical findings. This is an object detection and classification problem. The images are in png file with difference dimensions i.e 1024, 216 and 512. In this project, Images that were used were the one with 512 dimensions.

### Dataset information
The dataset comprises 67914 annotated and those not annotated images where there was only 4394 unique patients images that were annotated for posterior-anterior (PA) Xrays scans in PNG format. All images were labeled by a panel of experienced radiologists for the presence of 14 critical radiographic findings as listed below:


```
Pathologies:
0 - Aortic enlargement
1 - Atelectasis
2 - Calcification
3 - Cardiomegaly
4 - Consolidation
5 - ILD
6 - Infiltration
7 - Lung Opacity
8 - Nodule/Mass
9 - Other lesion
10 - Pleural effusion
11 - Pleural thickening
12 - Pneumothorax
13 - Pulmonary fibrosis

The "No finding" observation (14) was intended to capture the absence of all
findings above but in this case it was ignored.
```

### Data preprocessing
The Model (YOLOv5) requires specific data preprocessing steps in order to work effectively. In this case, we were to process our information to meets this standard. The following is a detailed workflow documentation of the data preprocessing steps that were taken in this particular case:
The main difference between GroupKFold and other cross-validation techniques like train_test_split is that it helped takes into account pathologies or labels for each class in the sample split equally. i.e, Since some pathologies had more class Distribution than others, It helped us ensure that the samples from one class label of pathology do not end up in the same group and are equally Distributed in both groups. For this project, since the data is split into 5 folds, 1/5 (or 20%) of the data will be used as the test set, while 4/5 (or 80%) will be used as the training set.

### Preparation of dataset Structure for modelling.
To structure the images and labels for YOLOv5 training, We created the following 4 directories where the training and validation information was to reside.

```
1. `/WORKING_DIR/PROJECT_DIR/labels/train` - This directory will store the labels (annotations) for the training images.
 
2. `/WORKING_DIR/PROJECT_DIR/labels/val` - This directory will store the labels (annotations) for the validation images.
 
3. `/WORKING_DIR/PROJECT_DIR/images/train` - This directory will store the training images.
 
4. `/WORKING_DIR/PROJECT_DIR/images/val` - This directory will store the validation images.
```
Once the directories were created, We then moved or copy the images and their corresponding labels to the appropriate directories. The labels for each image should have the same file name as the image, and should be placed in the appropriate label directory

```
(either `/WORKING_DIR/PROJECT_DIR/labels/train` or
`/WORKING_DIR/PROJECT_DIR/labels/val`).
```

The labels were also in their own format. Each image had a single text file as labels. The format of labels for YOLOv5 model used was a plain text file with the same name as the corresponding image file, and with a `.txt` extension. The file should contain one line for each object in the image, with the following format:

# NeuralSight Intro
***Let's discover NeuralSight in less than 5 minutes.***

{{% notice note %}}
#### Getting Started
Get started by setting up your environment. Or try our demo with neurallabs.africa.
Please read more about NeuralSight here. NeuralSight Github Repository.
{{% /notice %}}

#### What you'll need
Python version 3.5 or above:
- When installing Python, you are recommended to check all checkboxes related to dependencies.

## Set Up Locally
Clone the repository to your local machine.

```
git clone https://github.com/NeuralSight/NeuralSight_AI.git
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.
```
cd  NeuralSight_AI
```

### Install Dependencies
The cd command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.
Install all the dependencies using the requirements.txt file.
```
pip install -r requirements.txt
```
The command installs all necessary dependencies you need to run NeuralSight.

## Generating CSV File
Add Medical files to the workspace for preprocessing:

```
python preprocess.py
```

### Create your final preprocessed csv dataset -
Create a file at NeuralSight_AI/training/process.py:

```
#import some modules
from tqdm.notebook import tqdm
from glob import glob
 
import shutil, os
import cv2
import pandas as pd
import numpy as np
from cleaning import create_data
 
 
import warnings
warnings.filterwarnings("ignore");
 
import dotenv
dotenv.load_dotenv()
 
DATA_DIR = os.getenv("DATA_DIRECTORY")
TRAIN_DIR = os.getenv("TRAIN_DIR")
WANDB_API_KEY = os.getenv("WANDB_API_KEY")
 
 
#check if the file exists
if not os.path.isfile(f'{DATA_DIR}/train.csv'):
    print(f"No SUch Directory in the path Passed  : PATH SEND :: {DATA_DIR}/train.csv")
    print("Exiting....")
    exit(0)
# read the data
df = pd.read_csv(f'{DATA_DIR}/train.csv')
 
df1 = df[["image_id","x_min","y_min","x_max","y_max","class_id", "height", "width", "class_name"]].dropna()
df1['path'] = df1['image_id'].apply(lambda x: f"{DATA_DIR}/train/{x}.png")
 
# get class id
class_dict = {v:k for k,v in dict(df1[['class_name', "class_id"]].values).items()}
 
 
# save  df1 in order to use it for plotting
df1.to_csv("train_clean.csv", index=False)
 
 
check_df = create_data(df1)
# class names available
classes = list(check_df['class_name'].unique())
 
# Yolo normaly requires bbox to be normalized between 0 and 1.
# Since we have have height and width for a particular image, we gonna just divide bbox against either widht or height.
# We then extract the widht and height of the bbox from the above calibrations
 
 
df = check_df.copy()
 
df['x_min'] = df.apply(lambda x: (x.x_min)/x.width, axis =1)
df['y_min'] = df.apply(lambda x: (x.y_min)/x.height, axis =1)
 
df['x_max'] = df.apply(lambda x: (x.x_max)/x.width, axis =1)
df['y_max'] = df.apply(lambda x: (x.y_max)/x.height, axis =1)
df['x_mid'] = df.apply(lambda x: (x.x_max+x.x_min)/2, axis =1)
df['y_mid'] = df.apply(lambda x: (x.y_max+x.y_min)/2, axis =1)
df['w'] = df.apply(lambda x: (x.x_max-x.x_min), axis =1)
df['h'] = df.apply(lambda x: (x.y_max-x.y_min), axis =1)
 
df['area'] = df['w']*df['h']
 
 
selected_classes = (df['class_name'].value_counts(normalize=True).T[df['class_name'].value_counts(normalize=True).T >0.0001])
SELECTED_CLASS_NAMES  = list(selected_classes.index)
 
# Get a dataframe with selected classes
selected_df = df[df['class_name'].isin(SELECTED_CLASS_NAMES)]
 
 
# only which have below 40 bbox instances
img_ids = list((df['image_id'].value_counts(normalize=False).T[df['image_id'].value_counts(normalize=False).T <=40]).index)
 
 
# pd.DataFrame(base_details)
 
TRAIN =[]
# for img_id in selected_df['image_id'].unique():
for img_id in selected_df[selected_df['image_id'].isin(img_ids)]['image_id'].unique():
    curr_df = selected_df[selected_df['image_id'] ==img_id].reset_index(drop=True)
    base_details = dict(curr_df.loc[0][['image_id',"path",'width', 'height']])
    information =[]
    for indx in range(curr_df.shape[0]):
        other_details = dict(curr_df.loc[indx][['class_name', "x_min", "y_min","x_max","y_max", "x_mid", "y_mid", "w", "h", "area" ]])
        information.append(other_details)
 
    TRAIN.append([base_details['image_id'],base_details['path'] ,base_details['width'],base_details['height'],information])
 
 
final_data = pd.DataFrame(TRAIN, columns =['image_id',"path", "width", "height", "information"])
from pprint import pprint
print(final_data.head())
# save this data for feature usage.
final_data.to_csv("processed.csv", index=False)

```

## Data Pre_Processing for YOLO
Add Medical files to the workspace for preprocessing:

```
python preprocess.py
```
Data Pre_Processing for YOLO -
Create a file at NeuralSight_AI/training/process.py:

- Dropping images with `No findings` label: The first step in preprocessing the data was to drop all images with their label information that had a label called "No findings" because the label had no any bounding box information which were needed for model training. This was done to ensure that the model only focuses on images that contain the other 13 Chest X-ray pathologies of interest.
- Removing overlapping bounding boxes which occurs in the same class using Non-maximum suppression methods: In order to improve the performance of the model, non-maximum suppression was used to remove overlapping bounding boxes which occurs in the same class label. This technique helps to reduce the number of false positives by removing bounding boxes that have a high overlap with other boxes of the same class. The method worked as follows.
- Non-maximum suppression(NMS) function is used for removing overlapping bounding boxes. The function takes in two inputs: "boxes" and "overlapThresh". The "boxes" is a list of bounding boxes in the format of (x1, y1, x2, y2) where (x1, y1) is the top-left corner and (x2, y2) is the bottom-right corner. "overlapThresh" is a threshold value for the overlap ratio of bounding boxes.
- The function first checks if the input "boxes" is an empty list. If it is, it returns an empty list. If there are boxes, the function extracts the x and y coordinates of the top-left corner and bottom-right corner of each box. It then computes the area of each bounding box and sorts the boxes based on the bottom-right y-coordinate. Next, the function iterates through each box and compares it with the other boxes to calculate the ratio of overlap. If the overlap ratio is greater than the threshold, the function removes that box from the list of boxes to be returned. Finally, the function returns the remaining boxes as integers.
- Bounding Box information Normalization: The bounding box information were normalized to standard values between 0 and 1 against the width and height of the image. This ensures that the bounding box coordinates are consistent regardless of the size of the input image that a user will feed to the model. It allows us to work on any image size available.
- Calculating the height and width of the bounding box since they are one of the crucial features that must be fed to the model during training, they are used to identify where what is the size of the box.
- Training and Validation. Before Training, We split the data input two in order to validate the model after training. We used `GroupKFold method to split`. This method is a variation of the KFold method for cross-validation. It is used to split the data into `k` number of folds, where `k` in this case, we used k= 5 which means the data will be split into 5 folds.

```
from tqdm.notebook import tqdm
from glob import glob
import shutil, os
import cv2
import pandas as pd
import numpy as np
from cleaning import create_data
 
import warnings
warnings.filterwarnings("ignore");
 
import dotenv
dotenv.load_dotenv()
 
DATA_DIR = os.getenv("DATA_DIRECTORY")
TRAIN_DIR = os.getenv("TRAIN_DIR")
WANDB_API_KEY = os.getenv("WANDB_API_KEY")
 
 
#check if the file exists
if not os.path.isfile(f'{DATA_DIR}/train.csv'):
    print(f"No SUch Directory in the path Passed  : PATH SEND :: {DATA_DIR}/train.csv")
    print("Exiting....")
    exit(0)
# read the data
df = pd.read_csv(f'{DATA_DIR}/train.csv')
 
df1 = df[["image_id","x_min","y_min","x_max","y_max","class_id", "height", "width", "class_name"]].dropna()
df1['path'] = df1['image_id'].apply(lambda x: f"{DATA_DIR}/train/{x}.png")
 
# get class id
class_dict = {v:k for k,v in dict(df1[['class_name', "class_id"]].values).items()}
 
 
# save  df1 in order to use it for plotting
df1.to_csv("train_clean.csv", index=False)
 
 
check_df = create_data(df1)
# class names available
classes = list(check_df['class_name'].unique())
 
 
 
# Yolo normaly requires bbox to be normalized between 0 and 1.
# Since we have have height and width for a particular image, we gonna just divide bbox against either widht or height.
# We then extract the widht and height of the bbox from the above calibrations
 
 
df = check_df.copy()
 
df['x_min'] = df.apply(lambda x: (x.x_min)/x.width, axis =1)
df['y_min'] = df.apply(lambda x: (x.y_min)/x.height, axis =1)
 
df['x_max'] = df.apply(lambda x: (x.x_max)/x.width, axis =1)
df['y_max'] = df.apply(lambda x: (x.y_max)/x.height, axis =1)
df['x_mid'] = df.apply(lambda x: (x.x_max+x.x_min)/2, axis =1)
df['y_mid'] = df.apply(lambda x: (x.y_max+x.y_min)/2, axis =1)
df['w'] = df.apply(lambda x: (x.x_max-x.x_min), axis =1)
df['h'] = df.apply(lambda x: (x.y_max-x.y_min), axis =1)
 
df['area'] = df['w']*df['h']
 
 
selected_classes = (df['class_name'].value_counts(normalize=True).T[df['class_name'].value_counts(normalize=True).T >0.0001])
SELECTED_CLASS_NAMES  = list(selected_classes.index)
 
# Get a dataframe with selected classes
selected_df = df[df['class_name'].isin(SELECTED_CLASS_NAMES)]
 
 
# only which have below 40 bbox instances
img_ids = list((df['image_id'].value_counts(normalize=False).T[df['image_id'].value_counts(normalize=False).T <=40]).index)
 
 
# pd.DataFrame(base_details)
 
TRAIN =[]
# for img_id in selected_df['image_id'].unique():
for img_id in selected_df[selected_df['image_id'].isin(img_ids)]['image_id'].unique():
    curr_df = selected_df[selected_df['image_id'] ==img_id].reset_index(drop=True)
    base_details = dict(curr_df.loc[0][['image_id',"path",'width', 'height']])
    information =[]
    for indx in range(curr_df.shape[0]):
        other_details = dict(curr_df.loc[indx][['class_name', "x_min", "y_min","x_max","y_max", "x_mid", "y_mid", "w", "h", "area" ]])
        information.append(other_details)
 
    TRAIN.append([base_details['image_id'],base_details['path'] ,base_details['width'],base_details['height'],information])
 
 
final_data = pd.DataFrame(TRAIN, columns =['image_id',"path", "width", "height", "information"])
from pprint import pprint
print(final_data.head())
# save this data for feature usage.
final_data.to_csv("processed.csv", index=False)
```

### Preparation of dataset Structure for modelling -
To structure the images and labels for YOLOv5 training, We created the following 4 directories where the training and validation information was to reside.

``` 
1. `/WORKING_DIR/PROJECT_DIR/labels/train` - This directory will store the labels (annotations) for the training images.
2. `/WORKING_DIR/PROJECT_DIR/labels/val` - This directory will store the labels (annotations) for the validation images.
3. `/WORKING_DIR/PROJECT_DIR/images/train` - This directory will store the training images.
4. `/WORKING_DIR/PROJECT_DIR/images/val` - This directory will store the validation images.
```

Once the directories were created, We then moved or copy the images and their corresponding labels to the appropriate directories. The labels for each image should have the same file name as the image, and should be placed in the appropriate labels directory (either `/WORKING_DIR/PROJECT_DIR/labels/train` or `/WORKING_DIR/PROJECT_DIR/labels/val`). The labels were also in their own format. Each image had a single text file as labels. The format of labels for YOLOv5 model used was a plain text file with the same name as the corresponding image file, and with a `.txt` extension. The file should contain one line for each object in the image, with the following format:

``` 
class_id x_center y_center width height 
```

where:

**class_id:** An integer representing the class of the object. This should correspond to the class labels in your dataset.
**x_center:** The x-coordinate of the center of the bounding box, as a fraction of the image width.
**y_center:** The y-coordinate of the center of the bounding box, as a fraction of the image height.
**width:** The width of the bounding box, as a fraction of the image width.
**height:** The height of the bounding box, as a fraction of the image height.

>>Each object should be split in a new line. Here's an example of a label file for an image with two objects, a Pneumothorax and a Cardiomegaly:

``` 
12 0.5 0.5 0.2 0.2
3 0.7 0.7 0.1 0.1
```

This means that there is one Pneumothorax object with class label 12, center coordinates (0.5,0.5), width and height as 0.2 and one Cardiomegaly object with class label 3, center coordinates (0.7,0.7), width and height as 0.1

### Data Information Pointer -
A YAML file was created which contained all information about the training and validation dataset. The file had the following information.

``` 
yaml
names:
    - Cardiomegaly
    - Pleural effusion
    - Pleural thickening
    - Aortic enlargement
    - Pulmonary fibrosis
    - ILD
    - Nodule/Mass
    - Other lesion
    - Lung Opacity
    - Infiltration
    - Consolidation
    - Calcification
    - Atelectasis
    - Pneumothorax

**nc:** 14
**train:** /kaggle/working/train.txt
**val:** /kaggle/working/val.txt
```

***where:***
- train and val is a text file with all directories for images used for training and validation respectively
- nc is the number of classes
- names contains all class names


## Support Desk
Project support will be updated in due course. Please be patient.

Please visit our ***profile page*** or ask question `info@neurallabs.africa`

***Support for the project includes:***
* Responding to questions or problems regarding the the project as a whole and its features
* Fixing bugs and reported issues
* Providing updates to ensure compatibility with new software versions

***Item support does not include:***
* Customization and installation services
* Support for third party software and plug-ins

***Before seeking support, please...***
* Make sure your question is a valid Theme Issue and not a customization request.
* Make sure you have read through the documentation and any related video guides before asking support on how to accomplish a task.
* Make sure to double-check the theme FAQs.
* Almost 80% of the time we find that the solution to people's issues can be solved with a simple "Google Search". You might want to try that before seeking support. You might be able to fix the issue yourself much quicker than we can respond to your request.

## Version History (Changelog)
You can find the version history (changelog.txt) file on the main repository or you can contact out support team for assistance page.

Once again, thank you so much for purchasing this theme. As I said at the beginning, I'd be glad to help you if you have any questions relating to this theme. No guarantees, but I'll do my best to assist. If you have a more general question relating to the themes on ThemeForest, you might consider visiting the forums and asking your question in the "Item Discussion" section.

### Changelog
``` 
-----------------------------------------------------------------------------------------
Version 1.0 - Dec 7th, 2023
-----------------------------------------------------------------------------------------
- Updated version as a result of clinical trials.
 
-----------------------------------------------------------------------------------------
Version 0.1 - May 7th, 2022
-----------------------------------------------------------------------------------------
Pilot project version.
```








## Copyright and license
{{% notice note %}}
Code released under the [GPL 3.0 License](https://neuralsight.github.io/NeuralSight-Company-Charter-and-Documentation/#).

For more information about copyright and license check [Open Source License](https://neuralsight.github.io/NeuralSight-Company-Charter-and-Documentation/#).
{{% /notice %}}