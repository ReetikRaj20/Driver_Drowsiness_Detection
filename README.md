# Driver_Drowsiness_Detection
Driver Drowsiness Detection using SSDMobileNet and OpenCV

I have trained two models using Tensorflow Object detection.
The two models were trained on different datasets taken from the ROBOFLOW universe.

> [!TIP]
>  Open the files in Google Colab or click the links for enhanced code visualization.
### Active_Fatigue.ipynb (https://colab.research.google.com/github/ReetikRaj20/Driver_Drowsiness_Detection/blob/main/Active_Fatique.ipynb)) 
This had the labels **active** and **fatigue**. The model achieved an overall accuracy(mAP @ 0.5:0.95) of 89.27%. 

### Drowsiness_detection.ipynb (https://colab.research.google.com/github/ReetikRaj20/Driver_Drowsiness_Detection/blob/main/Drowsiness_detection.ipynb)
This had the labels ****awake**** and **drowsy**. The model achieved an overall accuracy(mAP @ 0.5:0.95) of 76.67%. 

### (Final)Drowsiness Detection.ipynb 
This file is utilized for real-time object detection, using OpenCV to perform inference through the webcam. Two TensorFlowLite models (detectfatigueactive.tflite and detectdrowsyawake.tflite) are employed along with their corresponding label files (labelmapfatigueactive.txt and labelmapdrowsyawake.txt). Inference is conducted on each frame of the video feed, with bounding boxes annotated based on the predicted labels from both models. An alert sound is activated only if both models consistently detect a drowsy or fatigued state for at least 15 consecutive frames.

