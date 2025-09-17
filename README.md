# Acne-Detection-using-Deep-Learning

# Acne Detection using Deep Learning

## Project Overview

This repository implements acne detection using deep learning techniques.  
The goal is to detect acne from images using object detection / segmentation (or classification + localisation) methods so as to automate acne diagnosis or documentation.

The project includes notebooks for model training, evaluation, and inference.  
A pretrained YOLOv8 model (`yolov8n.pt`) is provided for rapid experimentation or deployment.

---

## Features

- Training using a YOLOv8-based model  
- Datasets configured via YAML specification (`data.yaml`)  
- Support for inference on new images / batches  
- Experiment tracking via notebooks  
- Pretrained model checkpoint included  

---

## Architecture

- **Model:** YOLOv8 (nano version) for object detection of acne lesions  
- **Training Framework:** Ultralytics YOLOv8 (or similar)  
- **Data:** Input images + bounding box annotation for acne lesions  
- **Evaluation metrics:** mAP, precision, recall, etc. (to be detailed)  

---

## Usage

### Prerequisites

Make sure you have:

- Python 3.7+  
- A GPU if you want reasonable speed for training/inference (optional but recommended)  
- Enough VRAM to load model and images  

### Setup

Clone the repo:

```bash
git clone https://github.com/mukeshch77/Acne-Detection-using-Deep-Learning.git
cd Acne-Detection-using-Deep-Learning
```

### Install dependencies (example via pip):

```bash
pip install -r requirements.txt
```
Note: If there’s no requirements.txt, install core packages manually:
ultralytics, torch, opencv-python, pandas, etc.

### Running Training / Inference

- Training: Use notebook main.ipynb or 100Epoch.ipynb to train the model.

- Data config: Modify data.yaml to point to your training / validation image directories and classes.

- Pretrained model: yolov8n.pt is included; you can load it for inference or fine-tune further.

  ## Files and Structure

| File/Filename   | Description |
|-----------------|-------------|
| `main.ipynb`    | Notebook demonstrating training / evaluation pipeline |
| `100Epoch.ipynb`| Notebook running training over 100 epochs (experimental) |
| `data.yaml`     | Data configuration (train/val paths, class names) |
| `yolov8n.pt`    | Pretrained model checkpoint |
| `LICENSE`       | MIT License text |
| `README.md`     | This file |

## Model

- Model architecture: **YOLOv8 nano**  
- Trained on acne detection dataset (images + bounding box annotations)  
- Checkpoint file `yolov8n.pt` provided for usage or further fine-tuning  

---

## Dataset

- The dataset is defined in `data.yaml`, which includes paths to training and validation images, and class labels.  
- If using your own dataset, ensure the directory structure and annotation format is compatible with YOLOv8 (e.g. `.txt` annotation files, or COCO / YOLO formats).  

## License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for more details.

---

### MIT License 

Copyright (c) 2025 Mukesh Choudhary  

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:  

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.  

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.  
