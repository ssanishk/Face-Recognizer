# **Face Recognizer**

This is my attempt at building a face recognizer with very limited training images. This approach mainly relies on pre-trained models ([link](https://github.com/ssanishk/Face-Recognizer/tree/master/Models)) which are used to detect the face and extract features which are stored in list. The test images go through the same process where the face encoding have been compared with the list that has been generated.

## **Method Used**

The major bottleneck in the process of using Deep learning for face recognition is the lack of an abundant training set. We'll have to develop an accurate model using very few (less than 5). 

The process used is roughly described by the below image

![Method Used](https://github.com/ssanishk/Face-Recognizer/Images/model.png)

## **Dataset**

There is no particular dataset that has to be used. Since we are using pre-trained weights, all we need is a single image of the person of interest who you wish to add to the database. 
However, I had experimented with this particular [dataset](https://www.kaggle.com/danupnelson/14-celebrity-faces-dataset) 
If you want to play around with a larger dataset having more classes to check accuracy and other parameters, use Labelled Faces in the Wild (LFW) dataset.

## **Limitation**

At present this architecture only works when both the training and testing image contains a single face only. This handicap can be overcome easily by building a pipeline which first consists of a face detector which further channels the different cropped images to face recognizer.

## **Sample Result**

Sample output for a test image. 
The label appears at the bottom of the image (Rather dull, I know )

![](https://github.com/ssanishk/Face-Recognizer/Images/result.png)


