---
toc: true
layout: post
description: An AI app to automatically break down the nutrition information from every day foods
categories: [food,nutrition,desktop apps]
title: AI Nutrition Advisor
hide: false
comments: true
---

## Background

While pizza, pancakes, and burgers are super tasty, their nutritional information can be really scary. How scary? It's hard to tell by looking at it, but with the AI nutritional advisor you can tell by just taking a photo. This desktop app allows you to take a picture of a food and understand what it is as well as its nutritional content. *This project was developed by Amar Shah,Nehal Rawat, Nihar Sidhu, Shreya Subramanian, and Thomas Chen as our semester-long project in CS 4701: Practicum in Artificial Intelligence*
The Github repo containing this project can be found here: *https://github.com/nehalrawat/AI-Nutrition-Project*

## Front End

This Desktop Application is simple and runs in a python window giving options to *select an image* from your local files and then to *classify* it using the pre-trained weights of a Convolutional Neural Network. After hitting classify, a window pops up showing the name of the food item, essential information like *Calories, Fat Content, Cholesterol, Sodium, Carbohydrates, and Protein,* and how that food contributes to a suggested diet. The information is pulled from a local cache of health information for each class.

## Convolutional Neural Network

This application leverages a convolutional neural network based on the VGG16 model that was pre-trained on the ImageNet data set. We took the existing model and did fine-tuning training on 10 classes of food images with 100 images each to produce a set of weights. These weights are used when classifying an uploaded image that is passed through the network with a forward pass and outputs the highest probability match from the last layer of the network. The high probability classification match is then passed back to the front-end where it is displayed to the user with its name and nutritional information. 
