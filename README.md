# Coffee-Donuts-Visual-Recognition
Wake Up with Coffee and Donuts Visual Recognition - Hands on Lab

## Introduction

This hands on lab uses breakfast images, Watson Studio and Watson Visual Recognition to detect your favorite donuts, coffee mugs and bags of eye-opening coffee.

![Watson Studio screenshot](screenshots/WatsonStudio-VisualRecognitionModelTestResults.png)

## Learning objectives

After completing this tutorial you will be able to:

* Create a Visual Recognition model in Watson Studio running in IBM Cloud
* Capture images of Coffee Mugs, Coffee Bags and Donuts and zip them into a class (provided)
* Train a model to identify objects in the images
* Score the identified objects

## Prerequisites

This tutorial can be completed using an IBM Cloud Lite account.

* Create an [IBM Cloud account](http://ibm.biz/osseucoffeelab)
* Log into [IBM Cloud](https://cloud.ibm.com/login)

## Estimated time

You can complete this task in no more than 20 minutes.

# Hands on Lab Overview

The outline below provides a high level overview of the steps included in the lab instructions.

## Step 1 - Capturing Images

In this lab, we have created three zip files of pictures. The lab will use these images to identify
coffee mugs, bags of coffee beans and donuts. These images will be used as our training set.

- Grab them all [here](classes)
- Images of bags of Coffee Beans - [CoffeeBag.zip](classes/CoffeeBag.zip)
- Images of Coffee Mugs - [CoffeeMug.zip](classes/CoffeeMug.zip)
- Images of Donuts - [Donut.zip](classes/Donut.zip)

## Step 2 - Watson Studio

In this section, we will create a Watson Studio account, create a Project and Watson Visual Recognition model to identify images in several classes.

- Create a Watson Studio account - follow these [instructions](STUDIO.md)
- Create a Project
- Create a Visual Recognition model - follow these [instructions](VISRECO.md)
- Upload three zip files to Cloud Object Storage
- Create a class *Coffee Bag* - drag a zipfile
- Create another class *Coffee Mug* - drag a zipfile
- Create another class *Donut* - drag a zipfile
- Train your model - wait a few minutes

## Step 3 - Test your model
In this section you will use sample images to confirm your model.
- Test your model - follow these [instructions](VRMTEST.md)

## Step 4 - Implement this model in your Application

- Embed your model into an application using these code snippets

Let's get started - [Set up Watson Studio](STUDIO.md)

*Quick links :*
[Home](/README.md) - [Watson Studio](STUDIO.md) - [Visual Recognition Model](VISRECO.md) - [Test and Deploy](VRMTEST.md)
