# MNIST Autoencoder for Image Reconstruction



This project implements a **basic Autoencoder neural network** using the **MNIST handwritten digits dataset**. The goal of the model is to learn a compressed representation of the input images and reconstruct them from this compressed latent space.

An autoencoder consists of two main components:

* **Encoder:** Compresses the input image into a lower-dimensional representation.
* **Decoder:** Reconstructs the original image from the compressed representation.

The model is trained to minimize the **reconstruction error** between the original and reconstructed images.

---

## Dataset

The model uses the **MNIST dataset**, which contains grayscale images of handwritten digits (0–9).

* Image size: **28 × 28 pixels**
* Total training samples: **60,000**
* Total test samples: **10,000**
* Each image is flattened into a **784-dimensional vector**

---

## Model Architecture

### Encoder

784 → 128 → 64 → 32

### Decoder

32 → 64 → 128 → 784

The **latent space dimension is 32**, meaning the model compresses the original 784-dimensional input into only 32 features.

Total trainable parameters: **222,384**

---

## Training Details

* Optimizer: **Adam**
* Loss Function: **Binary Crossentropy**
* Epochs: **20**
* Batch Size: **256**

The model learns to reconstruct the input images by minimizing reconstruction loss.

---

## Results

### Test Loss

Final test loss obtained after training:

**0.0909**

This indicates that the reconstructed images are very similar to the original images.

### Training Performance

The training and validation loss curves show a consistent decrease across epochs, indicating stable learning without significant overfitting.

### Image Reconstruction

The reconstructed digits closely resemble the original MNIST images. Some slight smoothing occurs due to dimensionality reduction, but the essential digit structures are preserved.

---

## Output Visualization

The project includes:

* Training vs Validation Loss Curve
* Original vs Reconstructed Image Comparison

These visualizations demonstrate how effectively the autoencoder learns meaningful representations of the handwritten digits.

---

## Conclusion

The implemented autoencoder successfully compresses and reconstructs MNIST handwritten digits. The encoder learns a compact latent representation of the images, while the decoder reconstructs recognizable digits from this compressed representation. The low reconstruction loss and visual similarity between original and reconstructed images confirm that the model effectively captures the key features of the dataset.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* MNIST Dataset

