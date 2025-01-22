# Floranet


Floranet is a deep learning notebook focused on classifying flowers from the Oxford Flower Dataset. By leveraging 
transfer learning with VGG16, DenseNet121, and InceptionV3, Floranet explores techniques like layer freezing and data 
augmentation to achieve high classification accuracy with minimal error. 

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Dataset Download and Preparation](#dataset-download-and-preparation)
3. [Code Execution Guide](#code-execution-guide)
4. [Skip Training Option](#skip-training-option)
5. [Libraries Used](#libraries-used)
6. [File Structure](#file-structure)
7. [Results](#results)

---

## Prerequisites

- **Python**: version 3.11 or higher
- **Environment**: code tested on Google Colab and local environments.

Make sure to install the required libraries before running the code. You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
```

**Note:** the best way to access this code is to set up a Colab environment. If you choose this option, all the 
necessary dependencies will already be installed.

---

## Dataset Download and Preparation

The dataset used in this project consists of images of flowers and their corresponding labels. The code automatically 
downloads and preprocesses the dataset. No manual intervention is required. A deep dive on how the code handles the
process is as follows:

1. Download the dataset and related files:
    - [Flower Images](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/102flowers.tgz)
    - [Segmented Images](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/102segmentations.tgz)
    - [Image Labels](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/imagelabels.mat)

2. The data is extracted into the `Data` folder:
    - Images are stored in `Data/images`
    - Segmented images are stored in `Data/segmented_images`
    - Labels are processed and saved in `Data/train_set.csv`, `Data/valid_set.csv`, and `Data/test_set.csv`

---

## Code Execution

1. Clone or download the repository containing the code.
2. Ensure all prerequisites are installed.
3. Run the notebook or script sequentially.
4. Trained models and results will be saved in the `Models` directory.

---

## Skip Training Option

If you want to skip the training process and directly use pre-trained models:
- [Download the pre-trained models](https://drive.google.com/file/d/13Vy6ADjVWiDwFA8tuon6MI7cLiuunOfe/view?usp=share_link), 
which are available exclusively for members of Università degli Studi di Milano-Bicocca
- Unzip the `Floranet Models.zip` file, and paste its content into the `Models` directory

- Note: the results file (`results.csv`) generation can also be automatically skipped generated or updated based on the available models.

---

## Libraries Used

The project relies on the following main libraries:

- **TensorFlow**: 2.10.0
- **scikit-learn**: 1.2.2
- **Pandas**: 1.5.3
- **NumPy**: 1.23.5
- **Matplotlib**: 3.7.1
- **Requests**: 2.31.0

> **Note:** The code has been tested with these library versions. Compatibility with other versions is not guaranteed.

---

## File Structure

```
Project Directory
|
|-- Data/                      # Contains processed datasets
|   |-- images/                # Original images
|   |-- segmented_images/      # Segmented images
|   |-- train_set.csv          # Training data
|   |-- valid_set.csv          # Validation data
|   |-- test_set.csv           # Test data
|
|-- Models/                    # Contains saved models and results
|   |-- [ModelName]/           # Individual model directories
|-- Notebook.ipynb             # Main notebook
|-- requirements.txt           # List of required libraries
```

---

## Results

Evaluation results are summarized in `Models/results.csv`. Key metrics include:

- Training, validation, and test accuracies
- Classification reports with precision, recall, and F1-scores
- Training durations for each model

Example of a results summary:

| Model Name | Train Accuracy | Val Accuracy | Test Accuracy | Duration |
|------------|----------------|--------------|---------------|----------|
| VGG16      | 92.1%          | 88.7%        | 87.3%         | 2h 15m   |
| DenseNet   | 91.5%          | 89.2%        | 88.1%         | 2h 30m   |

For more details, refer to the `results.csv` file.

---

For any issues or questions, please contact [your-email@example.com].
