

# Automatic Custom License Plate Detection with EasyOCR, TensorFlow and PyTorch

![License Plate Detection Demo](Assets\logo.jpg)

## Project Overview

This project provides a complete solution for training and deploying a custom license plate detection model using TensorFlow and PyTorch. It allows you to detect license plates in images and real-time video streams, extract license plate numbers using Optical Character Recognition (OCR), and export the results for further analysis.

## Table of Contents

- [Automatic Custom License Plate Detection with EasyOCR, TensorFlow and PyTorch](#automatic-custom-license-plate-detection-with-easyocr-tensorflow-and-pytorch)
  - [Project Overview](#project-overview)
  - [Table of Contents](#table-of-contents)
  - [Key Features](#key-features)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
  - [Installation \&  Usage](#installation---usage)
  - [License](#license)

## Key Features

- Detect license plates in static images and real-time video streams.
- Utilize Optical Character Recognition (OCR) with PyTorch and EasyOCR to extract license plate numbers.
- Export detected license plates and associated text for future analysis.
- Pre-trained models and easy integration with TensorFlow Object Detection.
- Real-time license plate detection from a webcam.
- Conversion to TensorFlow.js and TensorFlow Lite formats for deployment.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following prerequisites:

- Python 3.x
- TensorFlow (v2.13.0) and PyTorch
- Git (for cloning the repository)
- Webcam (for real-time detection)



## Installation &  Usage

**Step 1. Clone this repository:**

```sh
git clone https://github.com/nicknochnack/TFODCourse
```

**Step 2. Create a new virtual environment:**

```sh
python -m venv tfod
```

**Step 3. Activate your virtual environment:**

For Linux:

```sh
source tfod/bin/activate
```

For Windows:

```sh
.\tfod\Scripts\activate
```

**Step 4. Install dependencies and add the virtual environment to the Python Kernel:**

```sh
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj
```

**Step 5. Collect images using the Notebook [1. Image Collection.ipynb](https://github.com/nicknochnack/TFODCourse/blob/main/1.%20Image%20Collection.ipynb)**

Make sure to change the kernel to the virtual environment as shown below:

![Change Kernel](https://i.imgur.com/8yac6Xl.png)

**Step 6. Manually divide collected images into two folders "train" and "test".**

The folders and annotations should be split between the following two directories:

- `TFODCourse/Tensorflow/workspace/images/train`
- `TFODCourse/Tensorflow/workspace/images/test`

**Step 7. Begin the training process by opening [2. Training and Detection.ipynb](https://github.com/nicknochnack/TFODCourse/blob/main/2.%20Training%20and%20Detection.ipynb).**

This notebook will guide you through installing TensorFlow Object Detection, making detections, saving, and exporting your model.

**Step 8. Install TensorFlow Object Detection.**

You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK. If not, resolve installation errors by referring to the [Error Guide.md](https://github.com/nicknochnack/TFODCourse/blob/main/README.md) in this folder.

![Installation OK](https://i.imgur.com/FSQFo16.png)

**Step 9. Start training the model.**

During this process, the notebook will install TensorFlow Object Detection. You may choose to train the model from within the notebook. However, training inside a separate terminal on a Windows machine allows you to display live loss metrics.

![Live Loss Metrics](https://i.imgur.com/K0wLO57.png)

**Step 10. Optionally evaluate your model in Tensorboard.**

Once the model has been trained, and you have run the evaluation command under Step 7, navigate to the evaluation folder for your trained model, e.g.,

```sh
cd Tensorflow/workspace/models/my_ssd_mobnet/eval
```

Open Tensorboard with the following command:

```sh
tensorboard --logdir=.
```

Tensorboard will be accessible through your browser, and you will be able to see metrics, including mAP (mean Average Precision) and Recall.
```

Make sure to replace the placeholder URLs with the actual links to your repository and notebooks.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
