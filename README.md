# TensorFlow Object Detection

This repository includes scripts and instructions for setting up and running object detection models using TensorFlow's Object Detection API.

## Prerequisites

Make sure you have Python installed on your system. The scripts are tested on Python 3.8.

## Installation

First, clone the TensorFlow models repository if it doesn't already exist in your workspace:

```bash
git clone --depth 1 https://github.com/tensorflow/models
```

```bash
Install the required packages:
pip install -U --pre tensorflow=="2.11"
pip install tf_slim
pip install pycocotools
```
```bash
Setup the TensorFlow Object Detection API:
sudo apt install -y protobuf-compiler
cd models/research/
protoc object_detection/protos/*.proto --python_out=.
cp object_detection/packages/tf2/setup.py .
python -m pip install .
```

## Usage

To run object detection on a video file, follow these steps:

1. **Model Setup**: Download and set up the pre-trained model. Example model used is 'ssd_mobilenet_v1_coco_2017_11_17'.

2. **Load Model**: Load the TensorFlow model into memory.

3. **Run Inference**: Use the model to detect objects in video frames.

4. **Output**: Save the output frames with bounding boxes and labels to an output video file.

## Example

Here is how you can run inference on a video file:

1. Download your video file to the Colab environment or ensure it is accessible from the script's path.

2. Set the video file path in the script:

   ```python
   cap = cv2.VideoCapture("/content/new-york-city-1044.mp4")
   ```
3. Execute the script to start the detection and save the output:
   
   ```bash
   python object_detection_script.py
   ```
   
