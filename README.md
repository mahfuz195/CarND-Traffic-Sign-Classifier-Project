## Project: Build a Traffic Sign Recognition Program

Overview
---
This project classify the German traffic road signs using deep neural networks and convolution neural networks. LaNet arechtecture was used to train and validate model. The dataset is avaiable at [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset). After the training, the model was tested with new random images of German traffic signs from the Internet.

### Dependencies
This project requires Python 3.5 and the following Python libraries installed:

Jupyter,
NumPy,
SciPy,
scikit-learn,
TensorFlow,
PIL,
OpenCV.

Preprocessing
---
The german sign classifier images ar 32x32x3 RGB images. I have modified the images with Grayscale converting to 32x32x1 and then using the normalization.

Image Augmentation
---
I have used the following image augmentation techniques to create more data for the training, validating and testing:
1. Chaning Brightness
2. Random rotation
3. Random scaling
4. Blurring

Model Architecture
---
1. Conv layer (input: 32x32x1, output: 28x28x6)
2. relu
3. Max pooling layer (input: 28x28x6, output: 14x14x6)
4. Conv layer (input: 14x14x6, output: 10x10x16)
5. relu
6. Max pooling layer (input: 10x10x16, output: 5x5x16)
7. Flatten (input: 5x5x16, output: 400)
8. FC layer (input: 400, output: 120)
9. relu
10. Dropout
11. FC layer(input: 120, output: 84)
12. relu
13. Dropout
14. FC layer (input: 84, output: 43)

![GitHub Logo](validation_accuracy.png)
Format: ![Alt Text](url)


A great writeup should include the [rubric points](https://review.udacity.com/#!/rubrics/481/view) as well as your description of how you addressed each point.  You should include a detailed description of the code used in each step (with line-number references and code snippets where necessary), and links to other supporting documents or external references.  You should include images in your writeup to demonstrate how your code works with examples.  

All that said, please be concise!  We're not looking for you to write a book here, just a brief description of how you passed each rubric point, and references to the relevant code :). 

You're not required to use markdown for your writeup.  If you use another method please just submit a pdf of your writeup.

The Project
---
The goals / steps of this project are the following:
* Load the data set
* Explore, summarize and visualize the data set
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report

### Dependencies
This lab requires:

* [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit)

The lab environment can be created with CarND Term1 Starter Kit. Click [here](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) for the details.

### Dataset and Repository

1. Download the data set. The classroom has a link to the data set in the "Project Instructions" content. This is a pickled dataset in which we've already resized the images to 32x32. It contains a training, validation and test set.
2. Clone the project, which contains the Ipython notebook and the writeup template.
```sh
git clone https://github.com/udacity/CarND-Traffic-Sign-Classifier-Project
cd CarND-Traffic-Sign-Classifier-Project
jupyter notebook Traffic_Sign_Classifier.ipynb
```

### Requirements for Submission
Follow the instructions in the `Traffic_Sign_Classifier.ipynb` notebook and write the project report using the writeup template as a guide, `writeup_template.md`. Submit the project code and writeup document.

## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).

