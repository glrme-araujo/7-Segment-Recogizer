# 7-Segment-Recogizer

This project was developed with the aim of enhancing and automating the acquisition of data from 7-segment displays. It involves capturing photographs of the equipment's display and processing the area containing the digits. Subsequently, a Convolutional Neural Network (CNN) is employed to digitally recognize the digits in the photo. The CNN has proven to be effective in this task of digit recognition from such images. This innovation has been implemented in the calibration of measurement equipment at the anemometry laboratory located in the Institute of Technological Research (IPT). Throughout the development, the complexity of constructing a neural network, its practical application, and the excellent results achieved were observed, along with the influence of randomness during the training of a prediction model.


## Database 

A database, or data set, is a set of inputs (signals) and outputs (results) information from specific specifications that will be learned by the chosen algorithm. Its objective is to model a neural network, or any other machine learning algorithm, thus generating a model for predicting results. 
A database is used by Sevensegdataset (Connor Monahan, 2020), it is made up of 17279 digits with a proportion of 28x28 pixels. The database presents different positions, formats, angles and color intensity, most of the digits are in 7-segment display, making it a varied database, which will help in the future to model a robust network.

<div aling="center">
<img src = "https://github.com/user-attachments/assets/fbcae7fc-5668-4b8a-89f7-12371fcd0afc"
</div>


## Processing

Image processing follows the following steps: apply gray scale, perform the threshold, and finally, dilate the lines. When receiving the digit, a gray scale layer is applied, which aims to leave the photo without color, only with shades of gray, this facilitates the application of some types of image processing techniques, threshold is one of these techniques .	 Thresholding, also known as thresholding, is an image processing technique that involves the segregation of pixels into two distinct categories, generally black and white, using a threshold value. The selection of this threshold is guided by specific characteristics of the image that you want to highlight or neglect (Python and OpenCV: Exploring Threshold and Filters, 2023). 
Applying this technique, an image is obtained with only black and white tones, leaving the digit very clear and easily identifiable, in addition to removing noise or unwanted traces.  Finally, dilation is performed, which is a morphological operation commonly used in image processing, to enlarge or thicken specific regions of an image. Dilation is often applied to binary images, where pixels have values ​​of 0 (black) or 255 (white). After this processing, the final image is obtained, which will have its aspect ratio changed to a ratio of 28x28 pixels, that is, a 28x28 matrix. The recognition model will be applied to this matrix.

<div aling="center">
<img src = "https://github.com/user-attachments/assets/c4264e56-f96b-422b-8dde-1a2fe2495545"
</div>


## Convolutional Neural Network

The recognition algorithm used in this work is the convolutional neural network [CNN] - which will be responsible for recognizing the digits in the project, it is a robust and reliable machine learning algorithm for this type of problem. In 1962, Hubel and Wiesel carried out research that indicated that some neurons become active together when exposed to lines or curves, which facilitates visual recognition. Then CNN’s filter lines, curves and edges, and, in each subsequent layer, convert this filtering into a more complex image. The first successful application of a CNN was developed by Yann LeCun in 1998, with seven layers between convolutions and fully connected. CNN data inputs are a three-dimensional matrix (height x width x colors), in general 3 color channels are used, which are red, blue, and green, the term used is RGB.
To train a deep learning algorithm, regardless of the type of technique to be applied in a project, it is necessary to have an extensive database and a computer that is compatible with processing. Training an algorithm consists of using known results from certain cases to solve another case with some degree of similarity between them. To obtain good results when training an algorithm, your database, in addition to being extensive, must have a good variety of information, with several different observations. The more diverse the data, the more likely it is to achieve satisfactory results. In addition to diversity, the number of iterations and repetitions (epochs) to be made when training a neural network algorithm is also extremely important. The number of iterations defines how many times the neurons will interact with each other during the training of the algorithm to define the weights, and the number of epochs defines how many times the iterations will be repeated. It is from the epochs that we can see the evolution of the algorithm. each workout performed. 
In this work, the training set containing 80% of the data was used to train the algorithm. 30 epochs and 28 iterations were defined, presenting a good learning curve during the epochs, and indicating that approximately 12 epochs would be enough to reach satisfactory values ​​obtained by the algorithm, both in training and testing, giving us an accuracy of 94%.

<div aling="center">
<img src = "https://github.com/user-attachments/assets/42b1baf4-721d-4ecf-86db-cf65c85d05b5"
</div>





