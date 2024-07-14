# NVIDIA CUDA Enabled Docker on GCP

This repository contains Dockerfiles and Python scripts to check the availability and proper setup of GPUs for PyTorch and TensorFlow on Google Cloud Platform (GCP). It ensures that CUDA is available and prints the versions of Python and the respective deep learning libraries.

## Features

- Dockerized environment for both PyTorch and TensorFlow.
- Checks for CUDA-enabled GPUs.
- Prints Python, PyTorch, and TensorFlow versions.
- Supports NVIDIA A100, T4, P4, P100, and V100 GPUs.

## Usage

### Building and Running the Docker Containers

#### PyTorch

1. Build the Docker image for PyTorch:
    ```sh
    docker build -t my-pytorch-app -f Dockerfile.pytorch .
    ```

2. Run the Docker container for PyTorch:
    ```sh
    docker run --gpus all --rm my-pytorch-app
    ```

#### TensorFlow

1. Build the Docker image for TensorFlow:
    ```sh
    docker build -t my-tensorflow-app -f Dockerfile.tensorflow .
    ```

2. Run the Docker container for TensorFlow:
    ```sh
    docker run --gpus all --rm my-tensorflow-app
    ```

## Contents

- `Dockerfile.pytorch`: Dockerfile to set up a PyTorch environment with CUDA support.
- `Dockerfile.tensorflow`: Dockerfile to set up a TensorFlow environment with CUDA support.
- `app.py`: Python script to check GPU availability and print Python, PyTorch, and TensorFlow versions.
- `requirements.txt`: File to list Python dependencies for the application.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
