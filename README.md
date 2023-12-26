# K-water Big Data Competition 💧
## Automative Sewage Damage Detection and Classification: Real-time AI & Self-driving Drone

This repository conatains codes descriptions submitted to **K-Water Big Data Competition**. Below are the frameworks used for the project.

<div align="left">
   <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
   <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=Jupyter&logoColor=white"/>
   <img src="https://img.shields.io/badge/Ultralytics-024DA1?style=flat-square&logo=Ultralytics&logoColor=white"/>
   <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=OpenCV&logoColor=white"/>
</div>

## 📄Code Description
### real-time-object-detection.ipynb
This code **connects devices on the same network in real time**. Since the goal of our project is to detect sewage damages in real time, we load **YOLOv8 model that trained with custome dataset**. This code uses CV2 library to capture images with camera so that the loaded model can recognize the breakage of the sewer in real time.

* **How to connect your PC to your smartphone**
  1. Install **'iPCamera - High-End Network Cam'** application on your smartphone
  2. Connect the smartphone and PC to the same network

Once the connection between the two devices is complete, a pop-up window of **YOLOv8 inference** will appear on the PC, and you can verify that the type of damage in the video is appropriate. 

-----

### YOLOv8-training-and-evaluation.ipynb
This code **uses the Ultralytics YOLOv8 model to train a computer vision model** that automatically detects breakages in sewage pipes and **assess the model's performance via mAP**.

1. **Create a yaml file for custom dataset** - After constructing a dataset storing image files and annotation files for each type of sewer pipe breakage using the Roboflow platform, create a yaml file for training the YOLOv8 model. In the `Training`, `Validation`, and `Test` folders, respectively, images and labels folders were organized and saved. 
2. **Model learning** - We import YOLOv8 model that pre-trained with COCO datasets and train it with 6,600 custom datasets. We tested various parameters, including epochs, patience, batch, and imgsz, allowing us to identify the model with optimal performance. 
3. **Performance evaluation** - Object detection and performance evaluation were performed using the validation set and the test set. mAP is used as a performance measurement indicator. 
4. **Checking object detection results** - Perform object detection on the test set and saved the images with the bbox in the set path so that you can check the results.

-----

### automatic-driving-sample.ipynb
The code is designed to enable self-driving cars to actually drive. The car is a 'ROBO KIT (Series)' product of 'Roborobo (https://roborobo.co.kr)', and you need to download the software from Roborobo's official site (https://roborobo.co.kr/download/0) to connect your car to your laptop. Before running the code, you need to install the downloaded software and then install 'RobokitRS' as well. This can simply be done through the `pip install RobokitRS` command on your terminal or your Jupyter notebook cell.

-----

## 🔥awards
🥉3rd place
