# 🧠 DCGAN for Synthetic Brain MRI Image Generation

This project implements a Deep Convolutional Generative Adversarial Network (DCGAN) to generate synthetic brain MRI images. The model is trained on the BraTS 2021 dataset, which contains MRI scans of glioma patients. This work supports data augmentation in medical imaging by addressing the scarcity of annotated data.

## 📊 Dataset
- **Source:** [BraTS 2021](https://drive.google.com/file/d/1DpIqAbGMCOAyXwX5MdfhFwLQKJLeB1il/view?usp=sharing)
- **Preprocessing:**
  - Resized to `128x128`
  - Converted to grayscale
  - Pixel values normalized to range `[-1, 1]`


## ⚙️ Training Details
- **Loss:** Binary Crossentropy
- **Optimizer:** Adam (`lr=0.0001`, `beta_1=0.5`)
- **Batch Size:** 32
- **Epochs:** 50–200 (configurable)
- **Latent Vector (`z_dim`):** 100

> The discriminator and generator are trained alternately to improve performance iteratively.

## 📈 Output
- Generator outputs are visualized at regular intervals
- Image quality improves with training progression

## How to Run the Project
1. Install dependencies using:
   ```bash
   pip install tensorflow numpy matplotlib pillow
2. Clone this repository:
   ```bash
   git clone https:github.com/HariharaJujjarapu/Synthetic-Brain-MRI-Image-Augmentation-Using-DCGAN.git
3. Run the Python script or Jupyter Notebook to train the model and test its accuracy.
