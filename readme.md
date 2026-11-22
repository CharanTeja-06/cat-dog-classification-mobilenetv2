
# Cats and Dogs Classification Using Transfer Learning

## Project Overview

This project uses Deep Learning and Transfer Learning to classify images of cats and dogs.

A pre-trained **MobileNetV2** model with ImageNet weights is used for feature extraction. Additional layers are added to perform binary image classification.

## Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- MobileNetV2
- Transfer Learning

## Project Structure

```text
Cats-Dogs-Classification/
│
├── sample_images/
├── Binary_Classification using Transferlearning.ipynb
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
└── .gitattributes
```

## Dataset

The project uses the **Cats and Dogs Light Dataset**.

**Dataset Links:**
- [Cats and Dogs Light Dataset](https://zenodo.org/records/5226945)
- [Kaggle Dogs vs Cats Dataset](https://www.kaggle.com/c/dogs-vs-cats/data)

| Dataset | Images |
|---|---:|
| Training | 1,000 |
| Testing | 400 |
| **Total** | **1,400** |

After downloading and extracting the dataset, maintain the following structure:

```text
cats_dogs_light/
│
├── train/
│   ├── cats/
│   └── dogs/
│
└── test/
    ├── cats/
    └── dogs/
```

## Installation and Setup

**1. Clone the repository**

Clone the repository and open the project folder in VS Code or your preferred IDE.

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Download the dataset**

Download and extract the dataset to your computer.

## Configure Dataset Paths

Before running the project, open `app.py` and update the training and testing dataset paths according to where you downloaded the dataset.

For example:

| Folder | Example Path |
|---|---|
| Training | `D:\Dataset\cats_dogs_light\train` |
| Testing | `D:\Dataset\cats_dogs_light\test` |

**Important:** Replace these example paths with the actual locations on your computer. Also update the image path if you want to test your own image.

## Run the Project

Open the terminal in the project directory and execute:

```bash
python app.py
```

To run the Jupyter Notebook, open `Binary_Classification using Transferlearning.ipynb` and execute the cells sequentially.

## Model Architecture

The project uses MobileNetV2 as a pre-trained feature extractor.

The model consists of:

1. Data Augmentation
2. MobileNetV2 Feature Extraction
3. Global Average Pooling
4. Dense Layer (128 neurons)
5. Dropout Layer
6. Sigmoid Output Layer

## Model Configuration

| Parameter | Value |
|---|---|
| Model | MobileNetV2 |
| Input Size | 160 × 160 |
| Batch Size | 16 |
| Epochs | 10 |
| Optimizer | Adam |
| Learning Rate | 0.0001 |
| Loss Function | Binary Crossentropy |
| Activation | Sigmoid |
| Early Stopping | Patience = 3 |

## Prediction

The model predicts the probability of an image belonging to the dog class.

- Probability ≥ 0.5: Dog
- Probability < 0.5: Cat

## Notes

- Download and extract the dataset before running the project.
- Update the dataset and image paths in `app.py`.
- Ensure the dataset folder structure is correct.
- An internet connection may be required initially to download MobileNetV2 pre-trained weights.

## Author

**Cats and Dogs Classification Using Transfer Learning**

A Deep Learning project built using TensorFlow, Keras, and MobileNetV2.
