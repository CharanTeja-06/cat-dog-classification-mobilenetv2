🐱🐶 Cats & Dogs Classification
Transfer Learning with MobileNetV2

<p align="center">
<img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/TensorFlow-DeepLearning-orange?logo=tensorflow&logoColor=white" />
<img src="https://img.shields.io/badge/Model-MobileNetV2-green" />
<img src="https://img.shields.io/badge/Task-Binary%20Classification-purple" />
</p>

📌 About the Project

A deep learning project that classifies images into Cats 🐱 or Dogs 🐶 using Transfer Learning.

The project uses a pre-trained MobileNetV2 model with ImageNet weights as a feature extractor, along with custom classification layers.

🛠️ Tech Stack
Python
TensorFlow & Keras
NumPy
MobileNetV2
Transfer Learning
📂 Project Structure
text
Cats-Dogs-Classification/
│
├── sample_images/
├── Binary_Classification using Transferlearning.ipynb
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
└── .gitattributes

📊 Dataset

Cats and Dogs Light Dataset

Training: 1,000 images
Testing: 400 images
Total: 1,400 images

Download Dataset:

Cats and Dogs Light – Download
Kaggle – Dogs vs Cats

Dataset folder structure:

text
cats_dogs_light/
├── train/
│   ├── cats/
│   └── dogs/
└── test/
    ├── cats/
    └── dogs/

⚙️ Installation & Setup

1. Clone the repository

Clone the project and open it in VS Code or your preferred IDE.

2. Install dependencies

bash
pip install -r requirements.txt


3. Download and extract the dataset

Download the dataset using the link above and extract it to your computer.

4. Update dataset paths

Open app.py and replace the existing training and testing paths with your own dataset locations.

For example:

Folder	Example Path
Train	D:\Dataset\cats_dogs_light\train
Test	D:\Dataset\cats_dogs_light\test
⚠️ Important: Update the paths according to where you downloaded the dataset. Also update the image path if you want to test your own image.
▶️ Run the Project

Run the application from your project directory:

bash
python app.py


To use the Jupyter Notebook, open:

Binary_Classification using Transferlearning.ipynb

Run all cells sequentially to train and evaluate the model.

🧠 Model Configuration
Parameter	Value
Architecture	MobileNetV2
Input Size	160 × 160
Batch Size	16
Epochs	10
Optimizer	Adam
Learning Rate	0.0001
Loss	Binary Crossentropy
Output Activation	Sigmoid
Early Stopping	Patience = 3
Model Workflow

<pre>
Input Image
↓
Data Augmentation
↓
MobileNetV2
↓
Feature Extraction
↓
Global Average Pooling
↓
Dense + Dropout
↓
Sigmoid Output
↓
Cat 🐱 / Dog 🐶
</pre>

🔍 Prediction

The model uses a probability threshold of 0.5:

Probability ≥ 0.5 → 🐶 Dog
Probability < 0.5 → 🐱 Cat
📌 Notes
Ensure the dataset folder structure is correct.
Update local paths before running the application.
Internet access may be required to download MobileNetV2 ImageNet weights for the first time.
Training time depends on your system.

<p align="center">
<b>Made with ❤️ using TensorFlow & MobileNetV2</b>
<br/>
⭐ If you like this project, consider giving it a star!
</p>
