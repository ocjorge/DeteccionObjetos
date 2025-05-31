# 🧠 Detección de Objetos en Video con YOLOv8
# Video Object Detection with YOLOv8

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5%2B-orange)
![Ultralytics](https://img.shields.io/badge/Ultralytics-YOLOv8-red)
![License](https://img.shields.io/badge/license-MIT-green)

A Python script for object detection in videos using YOLOv8 from Ultralytics. This project demonstrates how to process video files, detect objects frame by frame, and save the annotated results.

## Features

- 🎥 Video processing with OpenCV
- � Object detection using YOLOv8 models
- 📁 Automatic output directory management
- 📊 Progress tracking during processing
- ✅ Output verification

## Requirements

- Python 3.8+
- OpenCV (`pip install opencv-python`)
- Ultralytics YOLO (`pip install ultralytics`)

## Usage

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Configure paths in the script:
   - `MODEL_PATH`: Path to your YOLO model (.pt file)
   - `VIDEO_INPUT_PATH`: Path to your input video file
4. Run the script: `python detect_video.py`

## Configuration Options

| Parameter | Default | Description |
|-----------|---------|-------------|
| `CONF_ORIG` | 0.3 | Confidence threshold |
| `IOU_ORIG` | 0.5 | Intersection over Union threshold |
| `OUTPUT_PROJECT_DIR` | `./runs_original_working_structure/detect_video` | Output directory |

## Output Structure

The processed video will be saved in:
./runs_original_working_structure/detect_video/[video_name]_processed_original/

## Example

```python
# Example of running detection
results = model.predict(
    source=VIDEO_INPUT_PATH,
    stream=True,
    save=True,
    conf=0.3,
    iou=0.5
)

## Troubleshooting
If you get file not found errors, verify the paths in the script

Ensure your YOLO model is compatible with Ultralytics YOLOv8

Check OpenCV video codec support if you have issues with video I/O
