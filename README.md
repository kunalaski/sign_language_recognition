# Sign Language Recognition using Convolution Neural Network

## Problem Statement 
The goal of this problem statement is to develop a system that captures the image through the live webcam only if a particular gesture is present and give the text or letter associated with the gesture. The system shall accept input of a static gesture through the webcam, preprocess the image, feed it to the CNN model and display the text as an output. The system only gives output for the ASL fingerspelling. Our problem consists of three tasks to be done in real time:
1. Obtaining video of the user signing (input).
2. Classifying each frame in the video to a letter.
3. Reconstructing and displaying the most likely word from classification scores(output).

From a computer vision perspective, this problem represents a significant challenge due to a number of considerations, including:
1. Environmental concerns (e.g. lighting sensitivity, background, and camera position) 
2. Occlusion (e.g. some or all fingers, or an entire hand can be out of the field of view)
3. Sign boundary detection (when a sign ends and the next begins) 
4. Coarticulation (when a sign is affected by the preceding or succeeding sign)

The system shall recognize the specified letter through the webcam. It shall also form words and sentences using custom gestures. Then after confirming the sentence it will
convert the entire sentence into speech, and also translate the sentence in the specified language and that into speech too. The aim of this problem statement is to close the
communication gap faced by the people with hearing and speech disability. The proposed system is limited to static gestures which can only recognize ASL fingerspelling but can be later updated for ISL, JSL and also dynamic hand gesture and two hand gestures.

## Result and Analysis
The Sign Language Recognition using CNN is implemented as a desktop application. The
title window has two options to start the Sign Language Recognition application or to set
the skin masking

![image](https://user-images.githubusercontent.com/47791109/122280058-6703fc80-cf06-11eb-9b93-3013771f41b5.png)

Skin masking allows the user to set the histogram for skin masking according to the
features of its skin color.

![image](https://user-images.githubusercontent.com/47791109/122280156-8733bb80-cf06-11eb-8f55-4ea8422d7b42.png)

The start button navigates to the sign language recognition section. Which is divided
into five parts; live cam feed, recognized text section, word formation and sentence
formation section and translated text section.

![image](https://user-images.githubusercontent.com/47791109/122280194-94e94100-cf06-11eb-8f55-ae0fced66038.png)

The input is taken from the live cam feed and the result is shown in the recognized
text section. Two custom gestures are used to form words and a sentence. After the
sentence formation is complete the sentence is translated into the specified language.
During each letter recognition, sentence formation and translation the output is also given
in speech format to that text.

![image](https://user-images.githubusercontent.com/47791109/122280279-a9c5d480-cf06-11eb-94de-203e952f016e.png)

The accuracy achieved using Guassian blur threshold using skin masking is 98.79%.
Previously only skin masking and thresholding gave the accuracy of 96.55%. So gaussian
blur with skin masking is better than thresholding because only thresholding fails to
extract different features of the specific hand gesture. The accuracy achieved by gaussian
blur thresholding is better than most of the research papers on American sign language
recognition. Some research papers also had accuracies above 98% but they involved use of
equipment like flex sensors, depth sensors or kinect. The goal of this project was to
recognize American sign language fingerspelling with hardware requirements limited to
only a computer and a webcam.
Below is the classification report of the testing process:

![image](https://user-images.githubusercontent.com/47791109/122280380-c235ef00-cf06-11eb-8134-d9ea25b0a88e.png)

Below is the confusion matrix of our result:

![confusion_matrix](https://user-images.githubusercontent.com/47791109/122280569-f6a9ab00-cf06-11eb-808f-153b59e56089.png)

## Conclusion
Sometimes there is a language barrier between people of different culture, nationality or
ethnicity causing language barrier, but for the people with hearing and speech disability
there is always a communication gap. Sign Language Recognition bridges the gap by
introducing a computer application in the communication path so that the sign language
can be automatically captured, recognized and translated to text for the benefit of deaf and
mute people. This system uses CNN model which achieved 98.79% accuracy. It also
eliminates the problem of background noise. The system pre-processes the image to the
required nature for it to be fed into the model. The system is an approach to ease the
difficulty in communicating with those having speech disabilities. The amount of training
and validation loss observed with the proposed CNN architecture was less.

## Further Work
The proposed system is currently limited to only ASL fingerspelling; thus, it can be
enhanced to work with the sign language of different regions like ISL, JSL,etc. The images
can be modified by adding pictures with different light density. Further training of the
model to achieve efficient detection for two hand gestures. ASL fingerspelling are static
gestures but the system can also be modified to capture dynamic gestures as well through
word level association of sign language is possible. An android application can be
developed which can be used anytime and anywhere.



