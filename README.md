# Application of Kernel-based Contrastive Independent Component Analysis (KCICA) on EEG Dataset

This repository contains a Jupyter Notebook that demonstrates the application of Kernel-based Contrastive Independent Component Analysis (KCICA) on an EEG dataset. The goal of this project is to separate mixed EEG signals into their independent components using a contrastive learning approach based on the Hilbert-Schmidt Independence Criterion (HSIC).

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Results](#results)
- [Real-World Applications](#real-world-applications)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Contact](#contact)

## Overview
The KCICA model is a neural network-based approach for separating mixed signals into their independent components. It uses a Radial Basis Function (RBF) kernel to capture nonlinear relationships in the data and a contrastive HSIC loss to ensure that the recovered components are independent and distinct from negative samples.

This notebook applies the KCICA model to an EEG dataset containing recordings from 36 subjects, each with 19 channels. The goal is to recover independent components from the mixed EEG signals, which can be used for further analysis such as brain-computer interfaces, mental state analysis, or disease diagnosis.

## Dataset
The dataset contains EEG recordings from 36 subjects, each with 19 channels. The channels are:

```
Fp1, Fp2, F3, F4, F7, F8, T3, T4, C3, C4, T5, T6, P3, P4, O1, O2, Fz, Cz, Pz
```

### Dataset Details
- **Format:** 36 CSV files (one per subject)
- **Shape:** Each CSV file has dimensions `(num_samples, 19)`
- **Sampling Rate:** Not specified (assumed to be consistent across subjects)
- **Preprocessing:** The data is artifact-free and has been preprocessed using Independent Component Analysis (ICA) to remove artifacts (e.g., eye blinks, muscle activity)

## Methodology
### Key Steps
1. **Data Loading:** Load EEG data from CSV files and preprocess it (normalization).
2. **Model Definition:** Define the KCICA model using a feedforward neural network.
3. **Training:** Train the model using a contrastive HSIC loss function.
4. **Evaluation:** Visualize the recovered independent components and analyze their quality.

### Key Components
- **RBF Kernel:** Computes the similarity between data points using a Gaussian kernel.
- **HSIC Loss:** Measures the independence between two sets of features using the Hilbert-Schmidt Independence Criterion.
- **Neural Network:** A simple feedforward network with one hidden layer for learning the transformation.

## Dependencies
To run the notebook, you need the following Python libraries:

```bash
pip install numpy pandas matplotlib torch
```

## Usage
### Clone the Repository:
```bash
git clone https://github.com/your-username/kcica-eeg.git
cd kcica-eeg
```

### Install Dependencies:
```bash
pip install -r requirements.txt
```

### Run the Jupyter Notebook:
```bash
jupyter notebook "Application of Kernel-based Contrastive Independent Component Analysis (KCICA) on EEG dataset.ipynb"
```

### Follow the Notebook:
1. Load the EEG dataset.
2. Preprocess the data.
3. Train the KCICA model.
4. Visualize and analyze the results.

## Results
The notebook produces the following outputs:
- **Recovered Independent Components:** The model outputs independent components with the same shape as the input data `(num_samples, num_channels)`.
- **Visualizations:** Plots of the original EEG signals and the recovered components.
- **Loss Curve:** A plot of the training loss over epochs.

## Real-World Applications
The KCICA model can be applied to various real-world problems, including:
- **Blind Source Separation:** Separating mixed EEG signals into independent components.
- **Brain-Computer Interfaces (BCIs):** Decoding brain signals to control external devices.
- **Mental State Analysis:** Studying brain activity during cognitive tasks (e.g., arithmetic, memory tasks).
- **Disease Diagnosis:** Detecting abnormalities in brain activity (e.g., epilepsy, Alzheimer's).

## Contributing
Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes and push to the branch.
4. Submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
This implementation is inspired by kernel-based methods and contrastive learning techniques.
Special thanks to the PyTorch community for providing excellent tools and resources.

## Contact
For questions or feedback, please open an issue on GitHub or contact the maintainer:

**Your Name**  
📧 Email: [your.email@example.com](mailto:your.email@example.com)  
🔗 GitHub: [your-username](https://github.com/your-username)
