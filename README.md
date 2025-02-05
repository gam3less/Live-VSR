# Live Lipreader using AV-Hubert on Raspberry Pi 4B
# *THIS REPO IS A WORK IN PROGRESS AND IS NOT READY YET*

This repository contains the code and instructions to create a live lipreader using the AV-Hubert model, running on a Raspberry Pi 4B. The system captures live video, processes the lip movements, and predicts the spoken words in real-time.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Performance Considerations](#performance-considerations)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction

Lipreading is the task of interpreting spoken language by visually analyzing the movements of a speaker's lips. This project leverages the AV-Hubert model, a state-of-the-art audio-visual speech recognition model, to perform lipreading in real-time on a Raspberry Pi 4B.

## Features

- Real-time lipreading using the AV-Hubert model.
- Optimized for Raspberry Pi 4B with limited computational resources.
- Easy-to-use interface for capturing and processing live video.
- Pre-trained AV-Hubert model for accurate lipreading.

## Requirements

To run this project, you will need the following:

- **Hardware:**
  - Raspberry Pi 4B (4GB or 8GB recommended)
  - Raspberry Pi Camera Module or USB Webcam
  - MicroSD card (16GB or larger)
  - Power supply for Raspberry Pi

- **Software:**
  - Raspberry Pi OS (64-bit recommended)
  - Python 3.9.x
  - OpenCV
  - PyTorch (with ARM support)
  - AV-Hubert model weights (pre-trained)

## Installation

1. **Set up Raspberry Pi:**
   - Flash the Raspberry Pi OS onto the MicroSD card.
   - Connect the Raspberry Pi Camera Module or USB Webcam.
   - Boot up the Raspberry Pi and ensure the camera is working.

2. **Install dependencies:**
   ```bash
   sudo apt-get update
   sudo apt-get install python3-pip python3-opencv libopenblas-dev libatlas-base-dev libblas-dev liblapack-dev libatlas3-base
   pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/arm64
   pip3 install opencv-python av-huggingface
   ```

3. **Clone the repository:**
   ```bash
   git clone 
   cd 
   ```

4. **Download AV-Hubert model weights:**
   - Download the pre-trained AV-Hubert model weights and place them in the `models/` directory.
   - You can find the model weights [here](https://github.com/facebookresearch/av_hubert).

5. **Test the setup:**
   ```bash
   python3 test_camera.py
   ```
   Ensure that the camera feed is working correctly.

## Usage

1. **Run the live lipreader:**
   ```bash
   python3 live_lipreader.py
   ```

2. **Adjust settings:**
   - You can modify the `live_lipreader.py` script to adjust the frame rate, resolution, and other parameters to optimize performance on your Raspberry Pi.

3. **View the output:**
   - The system will display the live video feed with the predicted text overlay in real-time.

## Performance Considerations

- **Frame Rate:** Lowering the frame rate can help reduce the computational load, but may affect the accuracy of lipreading.
- **Resolution:** Reducing the video resolution can also improve performance, but may impact the model's ability to detect lip movements accurately.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have any suggestions or improvements.


## Acknowledgments

- [AV-Hubert](https://github.com/facebookresearch/av_hubert) by Facebook Research for the pre-trained models.
- [Raspberry Pi Foundation](https://www.raspberrypi.org/) for the Raspberry Pi hardware.
- [OpenCV](https://opencv.org/) for video processing.
- [Liam] () for coding most of this project.

---

This project is a proof-of-concept and may require further optimization for practical use. Enjoy experimenting with live lipreading on your Raspberry Pi!
