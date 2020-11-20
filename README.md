
# Mission
Our mission is to provide an excellent development experience by enabling developers
to build new AI/ML applications for a smarter and safer world.

# Axis video analytics example applications
Video analytics ensures that video surveillance systems become smarter,
more accurate, more cost-effective and easier to manage. The most scalable
and flexible video analytics architecture is based on ‘intelligence at the
edge’, that is, processing as much of the video as possible in the network
cameras or video encoders themselves.

This not only uses the least amount of bandwidth but also significantly reduces
the cost and complexity of the network. Open application development platforms
such as Axis Camera Application Platform (ACAP) Facilitate the integration of
compatible third-party solutions, resulting in a quickly growing variety of
applications – general as well as specialized for different industries. The
growing number of video analytics applications creates new end-user benefits
and opens new business possibilities.

# Getting started
This repository contains a set of application examples which aims to enrich the
developers analytics experience. All examples are using Docker framework and has a
README file in its directory which shows overview, example directory structure and
step-by-step instructions on how to run applications on the camera.

## Requirements
To get started following system requirements shall be met:
* Camera: Q1615-MkIII
* Docker version 19.03.5 or higher
* Firmware: 10.2.0
* Docker Daemon installed on the camera

## Supported architectures
The examples support the following architectures.
* armv7hf

## Example applications for video analytics
Below is the list of examples available in the repository.

* [inference-client](./inference-client/)
  * A Python example which implements object detection on a
    video stream and on still images from the camera.
* [object-detector-cpp](./object-detector-cpp/)
  * A C++ example which runs object detection on the camera.
* [opencl-fft](./opencl-fft/)
  * A C++ example which demonstrates how to use OpenCL in ACAP4 to speed up calculations. The application runs Fast Fourier Transform on the camera GPU.
* [opencv-capture-app](./opencv-capture-app/)
  * A C++ example which captures camera frames and properties such as time stamps, zoom, focus etc., through OpenCV.

### DockerHub Images
There are two types of Docker images here: the ToolChain (SDK), and the API. These images can be used as the basis for custom built images for running your applications. The images needed are specified in the docker-compose files. The docker repos for ACAP 4 has limited access to members of [axisecp](https://hub.docker.com/orgs/axisecp) organisation.

The images needed are specified in the docker-compose files. 
* [ACAP4-API](https://hub.docker.com/repository/docker/axisecp/acap4-api) - ACAP 4 API image for C and C++ with all API components (header and library files) included.
* [ACAP4-Toolchain](https://hub.docker.com/repository/docker/axisecp/acap4-toolchain) - The ACAP4 toolchain image contains tools that are useful when developing ACAP applications.
* [python-tfserving](https://hub.docker.com/repository/docker/axisecp/python-tfserving) - Tensorflow serving api and base image for applications written in python
* [larod-inference-server)](https://hub.docker.com/repository/docker/axisecp/larod-inference-server) - Inference server implemented on top of Larod API

### Pre-trained models
* [COCO SSD MobileNet v1 model](https://www.tensorflow.org/lite/models/object_detection/overview#starter_model)


# How to work with Github repository
You can help to make this repo a better one using the following commands.

1. Fork it (git checkout ..)
2. Create your feature branch: git checkout -b <contr/my-new-feature>
3. Commit your changes: git commit -a
4. Push to the branch: git push origin <contr/my-new-feature>
5. Submit a pull request


# License
[Apache 2.0](LICENSE)
