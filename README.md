
# Project Overview

This project focuses on using machine learning for image processing, specifically for classifying cancer types based on medical imaging. By leveraging deep learning techniques and adversarial training, this project aims to enhance the robustness and accuracy of cancer diagnosis systems.

## Key Features

- **Data Preprocessing**: Image transformations for data normalization and augmentation.
- **Model Training**: Utilizes transfer learning with a ResNet50 architecture.
- **Adversarial Training**: Incorporates adversarial attack scenarios to improve model resilience.
- **Performance Evaluation**: Tests model accuracy on both clean and adversarially altered images.

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
