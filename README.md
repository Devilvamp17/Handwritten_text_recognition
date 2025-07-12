# ✍️ Handwritten Text Recognition (HTR)

This repository contains a deep learning-based system for **Handwritten Text Recognition (HTR)** using **CNN architectures** such as **LeNet-5** and **AlexNet**, trained on the **EMNIST** dataset.  
The system classifies grayscale images of individual handwritten characters or digits using PyTorch/Keras.

---

## 🚀 Features

- 🧱 LeNet-5 and AlexNet-based image classification
- 🧠 Trained on EMNIST dataset for handwritten character recognition
- 📦 Includes pre-trained model (`emnist_cnn_model.h5`)
- 📊 Notebook-based training and evaluation workflow
- 📁 Easy-to-extend for other handwritten character datasets

---

## 📁 Repository Structure

```
Handwritten_text_recognition/
├── 102303242_Arnav_Goyal.ipynb     # Custom training notebook
├── alexnet.ipynb                   # AlexNet architecture and training
├── lenet-5.ipynb                   # LeNet-5 architecture and training
├── emnist_cnn_model.h5             # Saved trained CNN model (Keras)
└── README.md                       # Project documentation
```

---

## 🧠 Model Architectures

### ✅ LeNet-5

A classic CNN architecture for digit recognition:
- 2 convolutional layers
- 2 pooling layers
- 2 fully connected layers
- Output softmax layer

### ✅ AlexNet

A deeper CNN with:
- 5 convolutional layers with ReLU activations
- Max-pooling and dropout layers
- 3 fully connected layers
- High-capacity classification

---

## 🗃️ Dataset

The system is trained on the **EMNIST** dataset (Extended MNIST), which provides handwritten characters and digits in grayscale:

- 28×28 pixel grayscale images
- Includes both digits and letters
- Multi-class classification setup

You can download EMNIST from: https://www.nist.gov/itl/products-and-services/emnist-dataset

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone https://github.com/Devilvamp17/Handwritten_text_recognition.git
cd Handwritten_text_recognition
```

2. Open any notebook in Jupyter and run it, or install requirements manually if needed:

```bash
pip install tensorflow keras numpy matplotlib
```

---

## 🏋️‍♂️ Training

Open any of the provided notebooks (`lenet-5.ipynb`, `alexnet.ipynb`) and execute the cells.  
Training will:

- Load the EMNIST dataset
- Normalize and reshape data
- Train the CNN
- Save the model to `.h5`

---

## 🔍 Inference

Once trained, you can use the saved model to classify handwritten images:

```python
from keras.models import load_model
model = load_model("emnist_cnn_model.h5")
pred = model.predict(image.reshape(1, 28, 28, 1))
```

---

## 🧪 Evaluation

- Accuracy and loss plotted in notebooks
- Confusion matrix and per-class accuracy available
- Easily extendable to compute precision, recall, F1

---

## 🔮 Future Improvements

- 🔁 Integrate CRNN with CTC for full line recognition
- 🧪 Add support for full-sentence inference
- 🧼 Add preprocessing (binarization, noise reduction)
- 🌐 Deploy using Streamlit or FastAPI

---

## 👨‍💻 Author

Developed by [Arnav Goyal](https://github.com/Devilvamp17)

---

🎉 Feel free to fork, contribute, or raise issues. Happy coding!
