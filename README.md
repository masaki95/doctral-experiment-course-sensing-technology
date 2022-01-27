# doctral-experiment-course-sensing-technology
Codes for Yatani-sensei's doctral-experiment-course submission
(Masaki Takeuchi, Wu Bingchang)

Our codes are run in the following order.
1. FetchData.ino
2. bitesensor-speaker.ipynb
3. PlaySound.ino

※The vibration sound from the speaker has been already made by Takeuchi.
(We can't tell you how to create it because of the plan to have the patent)

1. FetchData.ino
 - Run a code to fetch the data from a pressure sensor with the Arduino serial monitor.
 - Copy it and paste and extract the 1000 datas of all users (Wu and takeuchi) and save each .csv files
 - To create no sound vibration modes without any pressure, we made all zero data .csv files.

2. bitesensor-speaker.ipynb
 - Using the tensorflow, we made a classification of pressure sensor datas into three classes (Takeuchi, Wu, zero).
 ※We utilized one pressure sensor only (i.e. one direction), so we made use of sparse softmax cross entropy loss function instead of normal (standardized) softmax one. In order to do it, we had to set up boarderline and converted the raw data into three integers: 0, 1, 2. 
 - Get the results of weights and biases

3. PlaySound.ino 
 - Using the weights and biases, the program finds which user pushes the pressure sensor or not and plays the user's vibration sound from the speaker.
