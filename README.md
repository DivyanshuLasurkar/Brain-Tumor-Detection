
# Brain Tumor Detection Using Deep Learning and MLOps

## Project Overview

This project explores the use of deep learning to classify brain MRI images based on the presence or absence of a tumor. It combines a Convolutional Neural Network (CNN) with an MLOps-oriented structure to support model development, prediction, deployment, and monitoring.

The objective is to build a structured machine learning application that goes beyond model training by incorporating practical software engineering and deployment components.

## Dataset Setup

The project uses a Brain MRI image dataset available on Kaggle.

Download the dataset and place the MRI images inside the `data/` directory using the following arrangement:

```text
data/
├── tumor/
└── no_tumor/
```

- `tumor/` contains MRI scans labeled as having a tumor.
- `no_tumor/` contains MRI scans labeled as not having a tumor.

Ensure that the images are placed in their respective folders before running the training pipeline.

## Project Directory Structure

```text
Brain-Tumor-Detection/
│
├── api/
│   └── main.py
│
├── docker/
│   └── Dockerfile.api
│
├── inference/
│   ├── batch_inference.py
│   └── tensorrt_engine.py
│
├── monitoring/
│   └── prometheus.yml
│
├── src/
│   ├── dataset.py
│   ├── model.py
│   ├── train.py
│   └── export_onnx.py
│
├── visualization/
│   └── plots.py
│
├── docker-compose.yml
├── requirements.txt
├── Makefile
└── README.md
```

## Project Workflow

The application follows a modular workflow, connecting data preparation and model development with inference and deployment.

```text
Brain MRI Dataset
        |
        v
Image Preprocessing
        |
        v
CNN Model Training
        |
        v
Model Evaluation
        |
        v
Prediction and Inference
        |
        v
FastAPI Integration
        |
        v
Docker-Based Deployment
        |
        v
Application Monitoring
```

## Workflow Explanation

### 1. Data Collection

MRI images are collected and organized into separate categories to provide labeled inputs for the classification model.

### 2. Data Preprocessing

The input images are prepared through resizing and normalization to ensure consistent dimensions and pixel values during model training.

### 3. Model Training

A Convolutional Neural Network learns visual patterns from the MRI images to distinguish between the two classification categories.

### 4. Model Evaluation

The trained model is assessed using classification metrics and visualizations, including a confusion matrix, to understand its prediction performance.

### 5. Model Inference

The inference module processes new MRI images and generates classification predictions using the trained model.

### 6. API Integration

FastAPI provides an interface for submitting MRI images and receiving model predictions through an API endpoint.

### 7. Containerization

Docker configuration files are included to support packaging and running application components in a consistent environment.

### 8. Monitoring

Prometheus configuration and application instrumentation provide a foundation for tracking service-level metrics and observing application behavior.

## Technologies Used

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Deep Learning | TensorFlow, Keras |
| Image Processing | TensorFlow Image Utilities |
| Machine Learning | Scikit-learn |
| API Development | FastAPI |
| Containerization | Docker, Docker Compose |
| Model Export | ONNX |
| Inference | ONNX Runtime |
| Monitoring | Prometheus |
| Visualization | Matplotlib |

## Project Objective

The main goal is to develop a brain MRI classification workflow while exploring how deep learning models can be organized into reusable, deployable, and monitorable applications.

This project is intended for learning and experimentation and is not a clinically validated medical diagnostic system.
