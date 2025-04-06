# MagnifyMe-Micro-Expression-Recognition-via-CNNs-Motion-Amplification

This repository contains the implementation of a deep learning approach to enhance and recognize micro-expressions by applying motion magnification and leveraging transfer learning techniques. The project focuses on amplifying subtle facial movements to transform them into distinguishable macro-expressions, facilitating improved analysis and classification.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [Acknowledgments](#acknowledgments)

## Project Overview

Micro-expressions are brief, involuntary facial expressions that reveal genuine emotions. Due to their fleeting and subtle nature, detecting and analyzing them is inherently challenging. This project addresses this challenge by:

1. **Motion Magnification**: Amplifying subtle facial movements using specified magnification factors (×10, ×25, ×50) to convert micro-expressions into more noticeable macro-expressions.

2. **Transfer Learning**: Utilizing pre-trained Convolutional Neural Networks (CNNs), specifically VGG16, trained on macro-expression datasets (JAFFE, KTFEv2) to optimize feature extraction and reduce training time.

3. **Evaluation**: Assessing the model's performance on the SAMM micro-expression dataset, achieving a test accuracy of 96.54%, surpassing previous benchmarks and demonstrating potential applications in emotion recognition for security and healthcare sectors.

## Key Features

- **Motion Magnification**: Enhances subtle facial movements to improve visibility and analysis.

- **Transfer Learning with VGG16**: Leverages pre-trained models to optimize feature extraction, reducing training time and improving accuracy.

- **High Accuracy**: Achieves a test accuracy of 96.54% on the SAMM dataset, outperforming previous methods.

## Technologies Used

- **Programming Languages**: Python

- **Libraries and Frameworks**: TensorFlow, Keras, OpenCV

- **Models**: VGG16 Convolutional Neural Network
  
## Installation

To set up the project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your_username/micro-expression-recognition.git
   ```


2. **Navigate to the project directory**:

   ```bash
   cd micro-expression-recognition
   ```


3. **Create a virtual environment** (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use 'venv\Scripts\activate'
   ```


4. **Install the required packages**:

   ```bash
   pip install -r requirements.txt
   ```


## Usage

1. **Data Preparation**:

   - Organize the SAMM dataset such that each micro-expression sequence is stored in a separate folder named after its unique identifier.

   - For transfer learning, ensure the JAFFE and KTFEv2 datasets are available and organized appropriately.

2. **Motion Magnification**:

   - Run the `motion_magnification.py` script to amplify micro-expression frames:

     ```bash
     python motion_magnification.py --input_dir path_to_samm --output_dir path_to_output --magnification_factor 10
     ```

   - Repeat the process for magnification factors of 25 and 50 as needed.

3. **Transfer Learning and Training**:

   - Execute the `train_model.py` script to fine-tune the VGG16 model on the magnified expressions:

     ```bash
     python train_model.py --train_dir path_to_training_data --val_dir path_to_validation_data --epochs 50 --batch_size 32
     ```

4. **Evaluation**:

   - Assess the trained model's performance on the SAMM dataset using the `evaluate_model.py` script:

     ```bash
     python evaluate_model.py --test_dir path_to_test_data --model_path path_to_trained_model
     ```

## Results

The model achieved a test accuracy of 96.54% on the SAMM dataset, outperforming previous benchmarks. This demonstrates the effectiveness of combining motion magnification with transfer learning for micro-expression recognition.

## Contributing

Contributions are welcome! If you have suggestions for improvements or find any issues, please fork the repository and submit a pull request.

1. Fork the Project

2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)

3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)

4. Push to the Branch (`git push origin feature/AmazingFeature`)

5. Open a Pull Request


## Acknowledgments

- [SAMM Dataset](https://www2.docm.mmu.ac.uk/STAFF/M.Yap/dataset.php)

- [JAFFE Dataset](https://www.kasrl.org/jaffe.html)

- [KTFEv2 Dataset](https://ktfev2.com)

- [VGG16 Model](https://keras.io/api/applications/vgg/#vgg16-function)

- Special thanks to the contributors and maintainers of the open-source libraries and datasets used in this project.
