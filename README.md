# 🧠 Deep Learning Image Classification Project
This project is a comprehensive deep learning platform for image classification, utilizing a Convolutional Neural Network (CNN) architecture to achieve high accuracy. The project consists of three primary components: `main.py`, `prediction.py`, and `guifinal.py`, each serving a distinct purpose in the image classification pipeline. The `main.py` file is responsible for training the CNN model, while the `prediction.py` file uses the trained model to make predictions on new images. The `guifinal.py` file provides a graphical interface for loading data, training the model, and making predictions.

## 🚀 Features
- **Data Loading and Preprocessing**: The project includes a robust data loading and preprocessing pipeline, which loads images from a specified folder, resizes them to a uniform size, and normalizes the pixel values.
- **CNN Model Architecture**: The project defines a CNN model architecture using the Keras library, consisting of multiple convolutional and pooling layers, followed by fully connected layers for classification.
- **Model Training and Evaluation**: The project includes a model training and evaluation pipeline, which trains the CNN model using the Adam optimizer and categorical cross-entropy loss, and evaluates its performance on a test set.
- **Graphical Interface**: The project includes a graphical interface built using the Tkinter library, which allows users to load data, train the model, and make predictions on new images.
- **Prediction and Classification**: The project includes a prediction and classification pipeline, which uses the trained CNN model to make predictions on new images and classify them into predefined categories.

## 🛠️ Tech Stack
- **Keras**: A deep learning library for building and training neural networks.
- **OpenCV**: A computer vision library for image processing and feature extraction.
- **NumPy**: A numerical computing library for efficient numerical computations.
- **Matplotlib**: A data visualization library for plotting and visualizing data.
- **Tkinter**: A graphical user interface library for building interactive interfaces.
- **Scikit-learn**: A machine learning library for data preprocessing and feature extraction.

## 📦 Installation
To install the required dependencies, run the following command:

```bash
pip install numpy keras opencv-python matplotlib scikit-learn
```

Additionally, ensure that you have the necessary dependencies installed for the graphical interface, including Tkinter.

## ⚠️ Model File (Split Parts)
Due to GitHub file size limitations, the trained model file `model.h5` has been split into three parts:

```
model_part1
model_part2
model_part3
```

Before running the project, you must merge these parts back into the original `model.h5` file.

## 🔧 Merge Model Parts Using Python
Create a file named `merge_model.py` and add the following code:

```python
parts = ["model_part1", "model_part2", "model_part3"]

with open("model.h5", "wb") as output:
    for part in parts:
        with open(part, "rb") as file:
            output.write(file.read())

print("Model successfully merged into model.h5")
```

Run the script using:

```bash
python merge_model.py
```

After running the script, the `model.h5` file will be recreated and the project can run normally.

## 🔧 Merge Using Command Line (Alternative)

For Linux / macOS / Git Bash:

```bash
cat model_part1 model_part2 model_part3 > model.h5
```

For Windows Command Prompt:

```cmd
copy /b model_part1+model_part2+model_part3 model.h5
```

## 💻 Usage
To use the project, follow these steps:

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Merge the model parts using:

```bash
python merge_model.py
```

4. Run the `main.py` file to train the CNN model.

```bash
python main.py
```

5. Once the model is trained, run the `prediction.py` file to make predictions on new images.

```bash
python prediction.py
```

6. Alternatively, run the `guifinal.py` file to access the graphical interface and load data, train the model, and make predictions.

```bash
python guifinal.py
```

## 📂 Project Structure
```markdown
project/
|---- main.py
|---- prediction.py
|---- guifinal.py
|---- merge_model.py
|---- model_part1
|---- model_part2
|---- model_part3
|---- model.h5
|---- data/
|       |---- train/
|       |---- test/
|---- requirements.txt
```
