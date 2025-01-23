# Floranet


Floranet is a deep learning notebook focused on classifying flowers from the Oxford Flower Dataset. By leveraging 
transfer learning with VGG16, DenseNet121, and InceptionV3, Floranet explores techniques like layer freezing and data 
augmentation to achieve high classification accuracy with minimal error. In this `README.md` file you will find quick
instructions on how to run the notebook correctly in your local development environment.

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Dataset Download and Preparation](#dataset-download-and-preparation)
3. [Code Execution Guide](#code-execution)
4. [Skip Training Option](#skip-options)
5. [Libraries Used](#libraries-used)
6. [File Structure](#file-structure)

---

## Prerequisites

- **Python**: version 3.11 or higher
- **Environment**: code tested on Google Colab and local environments.

Make sure to install the required libraries before running the code. You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
```

> **Recommendation:** For an optimal experience, we recommend using a Google Colab environment. 
> When utilizing Colab, all required dependencies will already be pre-installed

---

## Dataset Download and Preparation

The dataset used in this project consists of images of flowers and their corresponding labels. The code automatically 
downloads and preprocesses the dataset. No manual intervention is required. A deep dive on how the code handles the
process is as follows:

1. The following resources are retrieved:
    - [Flower Images](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/102flowers.tgz)
    - [Segmented Images](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/102segmentations.tgz)
    - [Image Labels](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/imagelabels.mat)

2. The resources are extracted into the `Data` folder:
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

## Skip Options

If you want to skip the (long) training process and directly use pre-trained models:
1. [Download the pre-trained models](https://drive.google.com/file/d/13Vy6ADjVWiDwFA8tuon6MI7cLiuunOfe/view?usp=share_link), 
which are available exclusively for members of Università degli Studi di Milano-Bicocca.
2. Unzip the `Floranet Models.zip` file, and paste its content into the `Models` directory. If the folder doesn't already exist, create it.
The directory structure should align with the example provided in the [File Structure](#file-structure) section.

Additionally, you may skip the generation of the results.csv file by completing the following steps:

- [Download the results.csv file](https://github.com/andreamoleri/Floranet/blob/main/Models/results.csv), which is available
to everyone on my personal GitHub repository.
- Paste the file into the `Models` directory. If the folder doesn't already exist, create it.
The directory structure should align with the example provided in the [File Structure](#file-structure) section.
---

## Libraries Used

The project relies on the following main libraries:

- **Pathlib** | 1.0.1
- **Requests** | 2.31.0
- **Pandas** | 2.0.3
- **Seaborn** | 0.13.2
- **Matplotlib** | 3.10.0
- **Tensorflow** | 2.16.2
- **Numpy** | 1.26.4
- **Scipy** | 1.11.1
- **Pillow** | 11.0.0
- **Scikit-learn** | 1.5.2
- **iPython** | 8.15.0
- **Protobuf** | 4.23.4

> **Note:** The code has been tested with these library versions. Compatibility with other versions is not guaranteed.

---

## File Structure

```
Project Directory
|
|-- Data/                      # Contains processed datasets
|   |-- images/                # Contains Original images
|   |-- segmented_images/      # Contains Segmented images
|   |-- imagelabels.mat        # Image labels
|   |-- train_set.csv          # Training data
|   |-- valid_set.csv          # Validation data
|   |-- test_set.csv           # Test data
|
|-- Export/                    # Contains KeyNote presentations
|
|-- Images/                    # Contains images used by the LaTeX report
|
|-- Models/                    # Contains models and reports
|   |-- model_densenet1/       # Contains 1st DenseNet experiment
|   |-- model_densenet2/       # Contains 2nd DenseNet experiment
|   |-- model_densenet3/       # Contains 3rd DenseNet experiment
|   |-- model_densenet4/       # Contains 4th DenseNet experiment
|   |-- model_inception1/      # Contains 1st Inception experiment
|   |-- model_inception2/      # Contains 2nd Inception experiment
|   |-- model_inception3/      # Contains 3rd Inception experiment
|   |-- model_inception4/      # Contains 4th Inception experiment 
|   |-- model_vgg1/            # Contains 1st VGG experiment
|   |-- model_vgg2/            # Contains 2nd VGG experiment
|   |-- model_vgg3/            # Contains 3rd VGG experiment
|   |-- model_vggg4/           # Contains 4th VGG experiment 
|   |-- results.csv            # Contains experiment results dataframe
|
|-- Report/
|   |-- Floranet.tex           # LaTeX Report of the project
|   |-- Floranet.pdf           # PDF Report of the project
|
|-- Floranet.ipynb             # Main notebook
|-- requirements.txt           # List of required libraries
|-- README.md                  # The file you're reading right now
```

---

For any issues or questions, please contact us at a.moleri@campus.unimib.it and f.armani1@campus.unimib.it.
