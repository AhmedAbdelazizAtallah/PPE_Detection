# PPE Detection with YOLOv11

Real-time Personal Protective Equipment (PPE) detection system using YOLOv11 and Streamlit.

## Features

- 🖼️ **Image Detection** - Upload images for PPE detection
- 🎥 **Video Processing** - Process recorded videos with synchronized playback
- 🔴 **Live Camera** - Real-time detection from webcam
- ⚙️ **Adjustable Settings** - Confidence threshold, IoU, inference resolution, frame skip

## Demo

The app detects safety equipment including:
- Hard hats / Helmets
- Safety vests / Jackets
- And other PPE items

## Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd PPE-Detection.yolov11-main

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

## Requirements

- Python 3.8+
- See `requirements.txt` for full list

## Project Structure

```
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── models/
│   └── best.pt           # Trained YOLOv11 model
├── src/                   # Source code modules
│   ├── predict.py        # Image prediction
│   ├── predict_video.py  # Video prediction
│   ├── webcam.py         # Webcam handling
│   ├── evaluate.py       # Model evaluation
│   └── training/
│       └── train.py      # Training script
└── tests/                 # Test images and videos (gitignored)
```

## Usage

1. Run `streamlit run app.py`
2. Open browser to `http://localhost:8501`
3. Select tab: Image Upload, Video Upload, or Live Camera
4. Adjust settings in sidebar
5. Upload media or start camera

## Model

The model (`models/best.pt`) is trained on the PPE Detection dataset from Roboflow (10,090 images).

## License

MIT License