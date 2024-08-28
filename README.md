# CNN Model of Cars and Motorcyles

## Overview
This project is using the CNN model of machine learning for images.  It takes in two image files, one of motorcycles, and one of cars and creates a model. The model is then optimized.

## Table of Contents
- [Overview](#overview)
- [Data Collection](#data-collection)
  - [Program Logic](#program-logic)
  - [MergeFilesCreatePickel Script](#mergefilescreatepickel-script)
  - [CreateVehicle_yPickle Script](#createvehicle_ypickle-script)
  - [PreprocessingVehiclePickle Script](#preprocessingvehiclepickle-script)
- [Outcomes](#outcomes)
- [Outcomes Location](#outcomes-location)
- [New Libraries Used](#new-libraries-used)
- [Source of Data](#source-of-data)

## Data Collection
Obtained a dataset form Kaggle of images of cars and motorcycles.

## Program Logic
### MergeFilesCreatePickel Script
Two separate files containing car and motorcycle images were pulled into the script.
The two files had their titles stripped from their images and put into two dataframes. Those dataframes had a couple of columns added, one of which specified the values of bike or car that corresponds with the image. The dataframes were merged into one, and a csv was created.

### CreateVehicle_yPickle Script
This notebook pulled in the vehicle_df.csv. The column which had the values of car or bike was made the y target.  This was then made into a pickle file called vehicle.pkl.

### PreprocessingVehiclePickle Script
The notebook here picked up the vehicle.pkl that has the X data. The data was resized to 250x250, and then normalized to 255.  This data was then stored in the preprocessed_vehicles.pkl.

### CreateModelTrain Script
This script took in the preprocessed_vehicles pickle and the vehicle_y pickle.  X was double checked for it's shapes where it turned out that some were in the RGB channel and some were in the grayscale channel.  X was then modified to have all the images become RGB.  A numpy array was created for X, a test/train split done, a model created, trained and then optimized.

## Outcomes
It was found that the model worked best at two epochs.  This gave an accuracy of 92%.

## Outcomes Location
The location is a notebook file in the GitHub Project called Model Performance.

## New Libraries Used
Two libraries were added.  The first one was IO.  This is an input/output library in python.  The other was OS which is an operating system library in python

## Source of Data
The data was pulled from a Kaggle library located at https://www.kaggle.com/datasets/utkarshsaxenadn/car-vs-bike-classification-dataset?resource=download.  It is called the Car vs Bike Classification Dataset.  The collaborators were from 
DeepNets (Owner). The licence is CC0: Public Domain.
