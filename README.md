# MNIST AutoEncoder using PyTorch

This project demonstrates how to build and train a simple **autoencoder** using **PyTorch** on the **MNIST** dataset. An autoencoder is a type of neural network that learns to compress and then reconstruct data. Useful for tasks like denoising, dimensionality reduction, or anomaly detection.

---

## What This Code Does

* Loads the **MNIST** handwritten digits dataset (28x28 grayscale images).
* Builds a custom **autoencoder neural network** with:

  * An **encoder**: compresses the input image into a smaller representation.
  * A **decoder**: reconstructs the original image from this compressed code.
* Trains the model using **MSELoss** to minimize the difference between input and output.
* Visualizes the training loss and shows original vs. reconstructed images after training.

---

## Output

The model will:
   * Train for 20 epochs on MNIST
   * Plot training loss
   * Display 10 reconstructed images vs. their originals
     
---

## Model Architecture

* **Encoder**:

  * Input: 784 (28x28) → 128 → 64 → 36 → 18 → 9
* **Decoder**:

  * 9 → 18 → 36 → 64 → 128 → 784 (28x28)
* Activation functions: **ReLU** (except final output: **Sigmoid**)

---

## 

* The model is trained using the **Adam optimizer** with a small weight decay.
* The final layer uses a `Sigmoid` activation to keep pixel values between `0` and `1`.
* The images are flattened and reshaped during training and visualization.

---
