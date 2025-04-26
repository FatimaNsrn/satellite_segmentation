# satellite_segmentation
Satellite Image Segmentation with SAM and U-Net

This project performs semantic segmentation on satellite images using the Segment Anything Model (SAM) to generate masks automatically, and then trains a U-Net model based on these masks.

Project Structure

notebook/: Jupyter Notebook files for data preparation, training, and evaluation.

data/:

train/: Training images and masks

valid/: Validation images

test/: Test images (without masks)

class_dict.csv: Class mapping

metadata.csv: Metadata for images


outputs/:

images/: Images extracted for training

masks/: Masks generated using SAM



Steps

1. Mask Generation:

We used Meta's Segment Anything Model (SAM) to generate segmentation masks from satellite images automatically.



2. Dataset Preparation:

Saved the images and masks under outputs/ folders for training.



3. Model Training:

Trained a simple U-Net model on the generated dataset.

Loss Function: CrossEntropyLoss

Optimizer: Adam

Input Size: 512x512

Output Classes: 7 classes

Requirements

Python 3.8+

PyTorch

torchvision

numpy

opencv-python

matplotlib

segment-anything


Install the requirements:

pip install torch torchvision numpy opencv-python matplotlib

Results

Training Loss after 10 epochs: ~1.1

Example predictions show reasonable segmentation but can be improved with:

Longer training

Better masks

Model fine-tuning
