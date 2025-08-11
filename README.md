
# ENDI_text_lines_extraction

This repository contains a comprehensive pipeline for detecting, segmenting, and processing Egyptian National ID cards. The system can handle both front and back sides of ID cards with orentation correction and text lines detection and extraction capabilities.

## Project Overview

This project implements a multi-stage pipeline for ID card processing:
- **ID card segmentation model** (Instance segmentation model).
- **Card rotation (alignment) correction model** (classification model).
- **ID text lines detection model** (object detection model).

## Project Structure

### Core Files
- **`Full Pipeline.ipynb`** - Complete end-to-end pipeline notebook for trails on testing cases.
- **`Models Development.ipynb`** - Development and training notebook for the models.
- **`project_documentation.pdf`** - Comprehensive project documentation and technical details.
- **`requirments.txt.txt`** - Python dependencies required for the project.

### Model Resources
- **`resources/`** - Directory containing trained model weights
  - `back_line_det_best.pt` - Best model for detecting back lines on ID cards
  - `front_line_det_best.pt` - Best model for detecting front lines on ID cards
  - `id_seg_best.pt` - Best model for ID card segmentation
  - `rot_cls_best.pt` - Best model for rotation classification

### YOLO Models
- **`yolo_models/`** - Directory containing base YOLO model files
  - `yolo11n-cls.pt` - YOLO11n classification model
  - `yolo11n-seg.pt` - YOLO11n segmentation model
  - `yolo11n.pt` - YOLO11n detection model

### Test Data
- **`test_cases/`** - Sample images for testing the pipeline
  - `back_1.jpeg`, `back_2.jpg` - Back side test images
  - `front_1.jpg`, `front_2.jpg` - Front side test images

### Data Archive
- **`data.rar`** - Compressed dataset used for training the models
  - **Important**: Extract this file if you plan to run `Models Development.ipynb` for training
  - The extracted data will be used for model training and validation

## 🛠️ Installation Requirements

### Prerequisites
- Python 3.8 or higher
- CUDA-compatible GPU (recommended for optimal performance)

### Python Dependencies

Install the required packages using pip:

```bash
pip install -r requirments.txt
```

**Note**: The requirements file contains:
- `ultralytics` - For YOLO model inference and training

### Additional Recommended Packages

For enhanced functionality, consider installing:

```bash
pip install torch torchvision
pip install opencv-python
pip install pillow
pip install matplotlib
pip install pandas
pip install numpy
```
