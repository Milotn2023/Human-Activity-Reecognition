# Human Activity Recognition using SisFall Dataset

## Project Overview
This project focuses on Human Activity Recognition (HAR) using the SisFall dataset. The dataset contains sensor data collected from accelerometers and gyroscopes to identify various human activities and falls. The goal is to develop models and systems that can accurately recognize and classify human activities, especially falls, which are critical for health monitoring and elderly care.

## Implementation
The project includes a comprehensive Python implementation (`Fall_Detection_System_v2_(1).ipynb`) that demonstrates:

### Machine Learning Models
- **Traditional Models**: Logistic Regression, Random Forest, K-Nearest Neighbors, Decision Tree
- **Deep Learning Models**: 
  - CNN (Convolutional Neural Network) + MLP
  - LSTM (Long Short-Term Memory) + MLP
  - MLP (Multi-Layer Perceptron)
  - PCNN-Transformer (Parallel CNN with Transformer)
  - Autoencoder

### Key Features
- **Data Preprocessing**: Windowing, normalization, feature extraction
- **Class Balancing**: Handles imbalanced dataset with class weights
- **Model Evaluation**: Comprehensive metrics including accuracy, precision, recall, F1-score, ROC curves
- **Visualization**: Learning curves, confusion matrices, performance plots
- **Hyperparameter Tuning**: Grid search for optimal parameters

### Technical Specifications
- **Window Size**: 200 samples per window
- **Sampling Rate**: 200 Hz
- **Input Features**: 9 sensor channels (3 accelerometers + 3 gyroscopes from 3 sensors)
- **Output**: Binary classification (Fall/No Fall)

## Dataset Description: SisFall
The SisFall dataset was created by A. Sucerquia, J.D. López, and J.F. Vargas-Bonilla from the Faculty of Engineering, Universidad de Antioquia (UDEA), Colombia.

- **Version:** February 2016 - Version 1.0
- **Number of files:** 4,510 files, each containing data for a single activity.
- **Subjects:** Adults (19-30 years old) and Elderly (60-75 years old).
- **Activities:** Includes Activities of Daily Living (ADL) and Falls.
- **Sensors:** Data collected from three sensors (2 accelerometers and 1 gyroscope) at 200 Hz.

### Activities of Daily Living (ADL)
| Code | Activity Description                                      | Trials | Duration |
|-------|----------------------------------------------------------|--------|----------|
| D01   | Walking slowly                                           | 1      | 100s     |
| D02   | Walking quickly                                          | 1      | 100s     |
| D03   | Jogging slowly                                          | 1      | 100s     |
| D04   | Jogging quickly                                         | 1      | 100s     |
| D05   | Walking upstairs and downstairs slowly                  | 5      | 25s      |
| D06   | Walking upstairs and downstairs quickly                 | 5      | 25s      |
| D07   | Slowly sit in a half height chair, wait a moment, and up slowly | 5      | 12s      |
| D08   | Quickly sit in a half height chair, wait a moment, and up quickly | 5      | 12s      |
| D09   | Slowly sit in a low height chair, wait a moment, and up slowly | 5      | 12s      |
| D10   | Quickly sit in a low height chair, wait a moment, and up quickly | 5      | 12s      |
| D11   | Sitting a moment, trying to get up, and collapse into a chair | 5      | 12s      |
| D12   | Sitting a moment, lying slowly, wait a moment, and sit again | 5      | 12s      |
| D13   | Sitting a moment, lying quickly, wait a moment, and sit again | 5      | 12s      |
| D14   | Being on one’s back change to lateral position, wait a moment, and change to one’s back | 5      | 12s      |
| D15   | Standing, slowly bending at knees, and getting up       | 5      | 12s      |
| D16   | Standing, slowly bending without bending knees, and getting up | 5      | 12s      |
| D17   | Standing, get into a car, remain seated and get out of the car | 5      | 25s      |
| D18   | Stumble while walking                                    | 5      | 12s      |
| D19   | Gently jump without falling (trying to reach a high object) | 5      | 12s      |

### Falls
| Code | Fall Description                                        | Trials | Duration |
|-------|--------------------------------------------------------|--------|----------|
| F01   | Fall forward while walking caused by a slip            | 5      | 15s      |
| F02   | Fall backward while walking caused by a slip           | 5      | 15s      |
| F03   | Lateral fall while walking caused by a slip            | 5      | 15s      |
| F04   | Fall forward while walking caused by a trip            | 5      | 15s      |
| F05   | Fall forward while jogging caused by a trip            | 5      | 15s      |
| F06   | Vertical fall while walking caused by fainting         | 5      | 15s      |
| F07   | Fall while walking, with use of hands in a table to dampen fall, caused by fainting | 5      | 15s      |
| F08   | Fall forward when trying to get up                      | 5      | 15s      |
| F09   | Lateral fall when trying to get up                      | 5      | 15s      |
| F10   | Fall forward when trying to sit down                    | 5      | 15s      |
| F11   | Fall backward when trying to sit down                   | 5      | 15s      |
| F12   | Lateral fall when trying to sit down                    | 5      | 15s      |
| F13   | Fall forward while sitting, caused by fainting or falling asleep | 5      | 15s      |
| F14   | Fall backward while sitting, caused by fainting or falling asleep | 5      | 15s      |
| F15   | Lateral fall while sitting, caused by fainting or falling asleep | 5      | 15s      |

### Subjects
- Adults (SA): 19 to 30 years old
- Elderly (SE): 60 to 75 years old

### Sensors and Data Format
- Data acquired with three sensors (2 accelerometers and 1 gyroscope) at 200 Hz.
- Each file contains nine columns representing acceleration and rotation data from the sensors.
- Data is in bits and can be converted to physical units using provided formulas.

## Folder Structure
- `content/gdrive/MyDrive/Datasets/SisFall_dataset/`: Original SisFall dataset files.
- `content/gdrive/MyDrive/Datasets/SisFall_enhanced/`: Enhanced version of the SisFall dataset.

## Usage

### Running the Code
1. **Setup Environment**: The notebook is designed to run on Google Colab
2. **Mount Google Drive**: Access to dataset files stored in Google Drive
3. **Install Dependencies**: Required packages are automatically installed
4. **Data Processing**: Automated preprocessing pipeline handles data loading and preparation
5. **Model Training**: Choose from multiple model architectures
6. **Evaluation**: Comprehensive performance analysis with visualizations

### Dataset Structure
- Use the dataset files for training and testing Human Activity Recognition models
- Data files are text files with sensor readings for each activity trial
- Each file contains 9 columns representing sensor data from 3 different sensors

### Model Performance
The implementation includes evaluation of multiple models with metrics such as:
- Accuracy, Precision, Recall, F1-Score
- ROC curves and AUC scores
- Confusion matrices
- Learning curves for deep learning models

## Files Structure
```
Human-Activity-Recognition/
├── README.md                           # Project documentation
├── Fall_Detection_System_v2_(1).ipynb  # Main implementation notebook
├── SisFall_dataset/                    # Original dataset
│   ├── SA01/ to SA23/                  # Adult subjects (19-30 years)
│   └── SE01/ to SE15/                  # Elderly subjects (60-75 years)
└── SisFall_enhanced/                   # Enhanced dataset version
    ├── SA01/ to SA23/                  # Adult subjects with enhanced labels
    └── SE01/ to SE15/                  # Elderly subjects with enhanced labels
```

## Requirements
- Python 3.7+
- TensorFlow/Keras
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
- Google Colab (recommended)

## Contact
For more information, contact the dataset creators at josedavid@udea.edu.co.
