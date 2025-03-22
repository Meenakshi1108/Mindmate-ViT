# Mindmate-ViT

This project uses a fine-tuned Vision Transformer (ViT) model to detect and classify facial emotions in real-time through your webcam.

## Features

- Real-time facial detection using OpenCV
- Emotion classification into 7 categories: ANGRY, EXCITED, FEAR, HAPPY, NEUTRAL, NOT_INTERESTED, SAD
- Live video feed with emotion labels and face bounding boxes

## Requirements

- Python 3.7+
- PyTorch
- OpenCV
- Transformers
- Pillow

## Installation

1. Clone this repository:
   ```
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install required packages:
   ```
   pip install torch opencv-python transformers pillow
   ```

3. Create a `datasets` folder:
   ```
   mkdir datasets
   ```

4. Download the fine-tuned model or train your own:
   - Place the fine-tuned model in a folder named `fine_tuned_vit_emotion`
   - If you don't have a pre-trained model, you'll need to fine-tune the base ViT model with your own dataset

## Dataset Structure

To analyze your own images, organize them in the `datasets` folder with the following structure:

```
datasets/
├── train/
│   ├── angry/
│   │   ├── img001.jpg
│   │   ├── img002.jpg
│   │   └── ...
│   ├── excited/
│   │   └── ...
│   └── ...
├── val/
│   └── ...
└── test/
    └── ...
```

Each emotion category should have its own folder containing relevant images.

## Usage

Run the main script to start the real-time emotion detection:

```
python MindMate_ViT.py
```

The webcam will activate, and the program will detect faces and display the predicted emotions in real-time.

- Press 'q' to quit the application

## Model Information

This project uses a Vision Transformer (ViT) model fine-tuned for emotion detection. The base feature extractor is from "trpakov/vit-face-expression".

