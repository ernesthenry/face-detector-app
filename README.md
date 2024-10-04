# Face Detector API

This project provides a scalable REST API for detecting faces in images using **DeepFace** and **Ray Serve** for deployment. The API accepts image URLs and returns the bounding box coordinates of any detected faces.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [API Usage](#api-usage)
- [Project Structure](#project-structure)
- [License](#license)

## Introduction

This project demonstrates how to build a face detection API using **FastAPI** for the backend, and **Ray Serve** for scaling the model deployment. **DeepFace** is used as the face detection library, leveraging the MTCNN backend for accurate face extraction.

The app fetches an image from a provided URL, detects the faces in the image, and returns the bounding box coordinates of each detected face in the response.

## Prerequisites

Make sure you have the following installed on your machine:

- Python 3.7+
- Ray 2.0+ (for Ray Serve)
- FastAPI
- Uvicorn (for serving FastAPI)
- DeepFace
- PIL (Pillow)
- Requests

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd <repository-name>

2. **Create a virtual environment (optional but recommended):**
```

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

```
3. **Install the required dependencies:**

```
pip install -r requirements.txt
Ensure that Ray, FastAPI, DeepFace, and Uvicorn are installed.
```

**Alternatively, you can manually install dependencies:**
```
pip install fastapi uvicorn ray deepface pillow requests

```
**Running the Application**
- Start Ray Cluster
- Ray Serve needs to be initialized before deploying the API. Start the Ray cluster:

```
ray start --head

```
**Run the FastAPI Application**
- You can run the FastAPI app using Ray Serve with the following command:

```
serve run main:facedetector_app


```