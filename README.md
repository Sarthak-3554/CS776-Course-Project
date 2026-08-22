
This project contains three Python notebooks implementing different deep learning approaches for training and inference tasks. Each notebook focuses on a specific model and use case:

1. YOLOv8 – Used for object detection and classification
2. YOLO+DINO – YOLO is used for object detection and DINO for Inference
3. YOLO+VAE (Variational Autoencoder) – A generative model used for learning latent representations and generating/reconstructing data.

These notebooks demonstrate the complete workflow including data loading, preprocessing, model training, and inference.

---------------------------------------------------------------------

Project Files:
- dino-training-inference-group-16.ipynb  
  Implements DINO training and feature extraction.

- yolov8-finetuning-and-inference-group16.ipynb  
  Fine-tunes a YOLOv8 model and performs object detection.

- vae-training-inference-group16.ipynb  
  Trains a Variational Autoencoder and generates/reconstructs samples.

---------------------------------------------------------------------

Requirements:
Install the required Python libraries before running the notebooks:

pip install torch torchvision ultralytics numpy matplotlib opencv-python

Optional (recommended):
- CUDA-enabled GPU for faster training
- Jupyter Notebook / JupyterLab environment

---------------------------------------------------------------------

General Workflow:
Each notebook follows a similar pipeline:

1. Import Libraries  
   Required libraries such as PyTorch, NumPy, OpenCV, etc.

2. Data Loading  
   Load dataset from local directories or configured paths.

3. Preprocessing  
   Apply transformations such as resizing, normalization, and augmentation.

4. Model Initialization  
   Define or load a pretrained model depending on the task.

5. Training  
   Train the model using defined hyperparameters (epochs, learning rate, batch size).

6. Evaluation / Inference  
   Run predictions or generate outputs using the trained model.

7. Visualization  
   Display results such as predictions, reconstructed images, or feature maps.

---------------------------------------------------------------------

DINO Notebook Details:
- Uses self-supervised learning (no labeled data required)
- Learns visual representations from images
- Can be used for downstream tasks like clustering or classification

Steps:
- Load dataset
- Apply augmentations
- Train DINO model
- Extract embeddings/features
- Perform inference or visualization

---------------------------------------------------------------------

YOLOv8 Notebook Details:
- Uses Ultralytics YOLOv8 framework
- Supports object detection tasks
- Fine-tunes pretrained weights on custom dataset

Steps:
- Prepare dataset and YAML configuration file
- Load pretrained YOLOv8 model
- Train using model.train(...)
- Validate model performance
- Run inference using model.predict(...)

Outputs:
- Bounding boxes
- Class labels
- Confidence scores

---------------------------------------------------------------------

VAE Notebook Details:
- Implements encoder-decoder architecture
- Learns latent space representation of input data
- Generates or reconstructs images

Steps:
- Load and preprocess dataset
- Define encoder and decoder networks
- Train using reconstruction + KL divergence loss
- Sample from latent space
- Visualize generated and reconstructed images

---------------------------------------------------------------------

Outputs:
Across all notebooks, the following outputs are generated:
- Trained model weights/checkpoints
- Prediction results (images or detections)
- Generated samples (for VAE)
- Training logs and visualizations (loss curves, outputs)

---------------------------------------------------------------------

Configuration Notes:
- Update dataset paths before running notebooks
- Modify hyperparameters as needed:
  - Learning rate
  - Batch size
  - Number of epochs
- Ensure correct file structure for datasets (especially for YOLO)

---------------------------------------------------------------------

Hardware Recommendations:
- GPU (NVIDIA with CUDA) strongly recommended
- Minimum 8GB RAM suggested
- Training on CPU is possible but slow

---------------------------------------------------------------------

Project Structure:
project/
│
├── dino-training-inference-group-16.ipynb
├── yolov8-finetuning-and-inference-group16.ipynb
├── vae-training-inference-group16.ipynb
└── README.txt

---------------------------------------------------------------------

Summary:
This project provides a compact implementation of three important deep learning paradigms:
- Self-supervised learning (DINO)
- Supervised object detection (YOLOv8)
- Generative modeling (VAE)

It can be used for learning, experimentation, and extending to real-world applications.