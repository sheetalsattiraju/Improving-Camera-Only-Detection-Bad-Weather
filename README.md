# Improving-Camera-Only-Detection-Bad-Weather
CMPE 249 Project
Members: Max Sorin, Samuel Tsao, Sheetal Sattiraju, Lyla Vela

## Research Question: Can adding explicit fog-density information to a camera-only object detector improve detection under poor visibility, and what is the accuracy/computational tradeoff?

## Motivation & Usecase:
Autonomous vehicles rely on external sensors, typically cameras, LiDAR and radar, to detect pedestrians, other vehicles, traffic signs and other objects in their surroundings. However, poor weather conditions, such as fog, rain, and snow, can significantly reduce image visibility and degrade the performance of camera object detection systems. For example, water droplets and road spray can build up on cameras, obstructing visibility. Additionally, fog can erase visual boundaries between an object and its background, preventing the identification of lane markings, signals, other cars, etc. 

In this project, our group will attempt to improve a lightweight model with camera only sensors for object detection using a fog-density value. The primary benefit of this is to reduce the cost of other sensors and to help autonomous driving systems that rely primarily on cameras that may encounter degraded visibility in poor weather conditions. We will compare the model’s detection performance across multiple fog-density levels and evaluation inference latency, accuracy, detection and computational resource usage.

## Models investigated:
- Yolov11n
- Yolo11m
- DETR

## Dataset:
- (Training) Foggy Cityscape: https://www.kaggle.com/datasets/minhducnguyen9705/foggy-cityscapes/data

## Attempts to integrate fog density value information:
1. Fog Density Scalar value added as constant input channel
2. "Squint"
3. FiLM
4. Image-Adaptive YOLO
