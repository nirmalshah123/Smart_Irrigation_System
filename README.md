# Smart_Irrigation_System

This real-time system was developed as part of Course Project (EE-712) Embedded Systems at IIT Bombay, India. We used R-Pi as our main micro-controller to control the sensors as well as for inferencing our ML Model.

## Features

- Can measure moisture content present in soil.
- Can measure air temperature as well as air humidity.
- Can capture images through camera sensor, run ML model for crop disease detection.
- In-built LCD display for showcasing different parameters.

## ML Model 
We used 5 layer CNN network, for detecting 38 classes of diseases on leaf images. The model was trained for 5 epoches, and achieved training accuracy of **97.89%**, and got **91.64%** accuracy on validation set.

## Challenges Faced
- DHT22 sensor has a sampling rate of 0.5 Hz i.e. it senses air temperature and humidity every 2 second which is a bit slow.
- Due to computation limitations, the model was not trained on R-pi, and the training was done on the cloud. Also we had to ensure to keep the model simple, due to the memory constraints of the R-pi.
