

# **Flare Removal Using Deep Learning for Image Enhancement**

This repository contains the implementation of a deep learning-based model for **lens flare removal** from images using a **Generative Adversarial Network (GAN)** framework. The project demonstrates how deep learning techniques can be utilized to remove unwanted lens flare artifacts, restoring clarity and improving image quality for various computer vision applications.

## **Project Overview**

Lens flare removal is an important image preprocessing task, especially in computer vision systems where image clarity is critical. This project leverages a **Generative Adversarial Network (GAN)** to effectively remove lens flare artifacts from images, enhancing the quality of the visuals for downstream tasks such as object detection, image recognition, and autonomous navigation. The model is trained to differentiate between flared and flare-free areas and generate clear, glare-free images.

## **Dataset**

The project uses a dataset structured with images containing lens flare artifacts. The dataset contains both **flared images** (with glare) and **ground truth images** (without glare). The dataset is divided into:

- **Training Data**: Contains images with lens flare and their corresponding flare-free ground truth images.
- **Test Data**: Used to evaluate the model's performance on unseen data.
  
Preprocessing steps include:

- **Image Normalization**: Scaling pixel values to [0, 1] range.
- **Data Augmentation**: Techniques like rotation, flipping, and color jittering to improve model generalization.

## **Model Architecture**

The model consists of the following components:

- **Encoder-Decoder Architecture**: The encoder extracts features from the input image (with lens flare), while the decoder reconstructs the image to remove the flare.
- **Generative Adversarial Network (GAN)**: 
  - **Generator**: Learns to generate flare-free images.
  - **Discriminator**: Distinguishes between real (flare-free) images and fake (generated) images.
- **Loss Function**: A combination of **pixel-wise loss** and **adversarial loss** for training the generator, and **binary cross-entropy loss** for the discriminator.

## **Training and Evaluation**

**Training Parameters:**

- **Optimizer**: Adam optimizer for training both the generator and discriminator.
- **Loss Function**: 
  - Generator: Pixel-wise Loss + Adversarial Loss
  - Discriminator: Binary Cross-Entropy Loss
- **Batch Size**: 32
- **Epochs**: 50

**Evaluation Metrics:**

- **PSNR (Peak Signal-to-Noise Ratio)**: Measures the quality of the generated images.
- **SSIM (Structural Similarity Index)**: Measures the structural similarity between the generated and ground truth images.

## **Results**

The GAN model achieved strong performance in removing lens flare from images. Evaluation on benchmark datasets showed significant improvement in **image clarity**, with the model demonstrating high PSNR and SSIM scores. The adversarial training helped generate more realistic and high-quality flare-free images, suitable for use in real-world applications.

## **License**

This project is licensed under the MIT License.

## **Contact**

For any questions or feedback regarding the project, please feel free to contact me via the email provided below.

- [LinkedIn Profile](https://www.linkedin.com/in/devika-b-826637288/)  
- **E-mail**: devikab140@gmail.com
