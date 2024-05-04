
# Project Overview

This project focuses on using machine learning for image processing, specifically for classifying cancer types based on medical imaging. By leveraging deep learning techniques and adversarial training, this project aims to enhance the robustness and accuracy of cancer diagnosis systems.

## Key Features

- **Data Preprocessing**: Image transformations for data normalization and augmentation.
- **Model Training**: Utilizes transfer learning with a ResNet50 architecture.
- **Adversarial Training**: Incorporates adversarial attack scenarios to improve model resilience.
- **Performance Evaluation**: Tests model accuracy on both clean and adversarially altered images.

## The problem
![image](https://github.com/NikosBakalis/Adversarial-attack-on-Intel-and-MobileODT-Cervical-Cancer-Screening/assets/47317522/bbdd474a-9ef9-4fbb-8f3a-e4b76d35e9d2)
- **Original Image**: A photo of a panda is shown with a label "panda" and the model's confidence in this classification is 57.7%.
- **Perturbation**: The middle image represents a small perturbation (visual noise) calculated using the sign of the gradient of the model's loss function with respect to the input image. This perturbation is multiplied by 0.007 to keep its magnitude small.
- **Adversarial Image**: The resulting image on the right looks almost identical to the original panda image to the human eye, but it now includes the calculated perturbation. This slight modification causes the model to misclassify the image as a "gibbon" with 99.3% confidence.

## Cervical Cancer image classification
![image](https://github.com/NikosBakalis/Adversarial-attack-on-Intel-and-MobileODT-Cervical-Cancer-Screening/assets/47317522/bd3b878e-a4d5-430a-95f3-2b9b8ec08414)
- **Type 1**: This image shows a close-up view of the cervix with a clear and focused visual. The cervix appears slightly open, and there are visible vascular patterns. This type could represent a normal cervix or a particular stage of cervical health.
- **Type 2**: This image includes a medical instrument, possibly a speculum, which is used during cervical exams to provide a clear view of the cervix. The cervix in this image looks similar to Type 1 but is being viewed under different conditions, which might highlight other features or abnormalities.
- **Type 3**: The third type shows the cervix under a different lighting or imaging technique, possibly using a filter or enhancement to highlight specific features such as vascular patterns or surface texture.

## Loss and Accuracy over Epochs before Adversarial Attacks 
### Without Adversarial Attacks
![image](https://github.com/NikosBakalis/Adversarial-attack-on-Intel-and-MobileODT-Cervical-Cancer-Screening/assets/47317522/ad746146-1817-4fd6-88a2-7b8da5f7b3a2)
- **Loss (Blue Line)**: Starts high and decreases sharply, flattening out as the epochs increase.
- **Accuracy (Orange Line)**: Starts low and increases sharply, reaching a plateau as epochs increase.

### With Adversarial Attacks without Adversarial Attack Training
![image](https://github.com/NikosBakalis/Adversarial-attack-on-Intel-and-MobileODT-Cervical-Cancer-Screening/assets/47317522/835deba9-5c75-469b-af60-1f9515f4d983)
- **Loss (Blue Line)**: Shows a steep decline initially, stabilizing towards the later epochs.
- **Accuracy (Orange Line)**: Increases sharply at the start and then levels off.
- **Adversarial Accuracy (Green Line)**: Starts relatively high, decreases slightly in the middle epochs, then slightly increases and stabilizes.

### With Adversarial Attack with Adversarial Attack Training
![image](https://github.com/NikosBakalis/Adversarial-attack-on-Intel-and-MobileODT-Cervical-Cancer-Screening/assets/47317522/bf9827bb-df88-4c0b-8050-852df05c531a)
- **Loss (Blue Line)**: Begins high, drops rapidly, and then flattens.
- Accuracy (Orange Line)**: Begins low, rises quickly, and remains fairly constant.
- **Adversarial Accuracy (Green Line)**: Begins relatively high, drops and then gradually stabilizes.

## Installation

To run this project, ensure you have Python installed, along with the following major libraries:
- PyTorch
- torchvision
- numpy
- matplotlib

```bash
pip install torch torchvision numpy matplotlib
```

## Usage

The notebook is structured to guide you through the process of data preparation, model training, and evaluation step-by-step. Execute each cell sequentially to reproduce the results.

### Configuring Parameters

Adjust the training parameters and device configurations at the beginning of the notebook to suit your computational environment (e.g., GPU settings).

### Running Adversarial Attacks

Detailed instructions are provided on how to generate and apply adversarial attacks to test the robustness of the trained model.

## Contributing

Contributions to this project are welcome. Please feel free to fork the repository, make changes, and submit a pull request.

## Authors

- **Nikolaos Bakalis** - Initial work and documentation

## License

This project is licensed under the MIT License - see the LICENSE file for details.
