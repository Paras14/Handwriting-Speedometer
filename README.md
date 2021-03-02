How does it work

The project tells how fast can you write, in terms of WPM or Words per minute.
What it basically does is it gives you  15 seconds(can be increased also) to write something as fast as you can then snaps a picture of the page you are writing on after 15 seconds( and it does all of it automatically, you do not have to stop writing and click a photo of it, also it does not matter if your palm is in the picture or not, the algorithm just looks for Handwritten text). Remember you will need someone or some sort of mechanism to so that your smartphone is kept in place while you are writing, always pointing towards the page you are writing on. It then sends the picture to your computer via IP CAM, the picture is first saved and then sent to Amazon’s Textract API, which determines how many handwritten words are there in the picture.
Number of words written in the given amount of time is used to determine the speed at which they were written. It also asks you if you want to know which of the text it detected as words, if you choose to check out those words it will display the image captured with yellow boxes drawn on each word.

The time duration of 15 seconds can be changed in the code for as per your requirement.


APPLICATIONS

This Handwriting Speedometer can be used as a tool to measure you handwriting speed and to help students have a competition among themselves.
I feel like this project can be used to help struggling students, who have very slow handwriting speed and are often not able to complete their examination in time (Something that I have personally have struggled with in the past).

SETTING UP THIS PROJECT
For setting up this project you need to have the .ipynb file and an AWS account, with Rekognition API enable and BOTO3 downloaded and setup in your system.



SCOPE  OF IMPROVMENT IN THIS PROJECT

Currently this project uses Amazon Textract API of AWS, what it means is that the image goes through the model trained by Engineers at Amazon to predict how many words are there in the image sent, this limits it to be used only while we are connected to the internet. Also it highly dependent on the internet speed, to send the photo and receive important information.
What can be done instead is to train a model comprising of various, CNNs and RNNs layers to determine the number of handwritten words in the image. So that the calculations can be done locally on the system itself using that model. Although training a model is no joke you need tons and tons of data to train it, here data means images Handwritten text, and not just feeding them straight after clicking, the images need to be resized and labeled first by humans.
We would need at least 3000-4000 images to get a good accuracy.