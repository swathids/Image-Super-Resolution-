# Image-Super-Resolution-
Digital Image Processing enhances and analyzes images for use in fields like medical imaging, surveillance, and remote sensing. This project applies interpolation methods and a deep learning-based SRCNN to perform image super-resolution, using Python for implementation and evaluation via PSNR and SSIM.


Image Super-Resolution: Classical and Deep Learning Approaches
This project aims to enhance the quality of low-resolution images using digital image processing techniques. It compares classical interpolation methods with a deep learning-based Super-Resolution Convolutional Neural Network (SRCNN) to evaluate their effectiveness in reconstructing high-resolution images. The notebook offers a detailed, step-by-step implementation pipeline, making it a valuable resource for understanding super-resolution in both academic and practical contexts.

## Project Objectives
Simulate low-resolution images by downsampling high-resolution originals.

Explore and compare five classical interpolation techniques: Nearest Neighbor, Bilinear, Bicubic, Lanczos, and Spline.

Implement a deep learning-based SRCNN model to improve image reconstruction quality.

Apply denoising before interpolation to reduce artifacts and enhance visual fidelity.

Evaluate performance using standard image quality metrics: PSNR and SSIM.
##  Techniques Implemented
1. Preprocessing
Load the original image and convert color spaces if needed.

Visualize the input using Matplotlib.

2. Downsampling
Reduce image resolution (e.g., by 50%) using OpenCV to simulate low-resolution (LR) data.

3. Denoising
Apply filters such as Gaussian blur or bilateral filter to remove noise before reconstruction.

4. Upsampling Using Classical Interpolation Methods
Nearest Neighbor: Assigns each new pixel the value of the closest original pixel. Fast but produces blocky, pixelated images.

Bilinear: Computes new pixels by weighted averaging of 4 nearest neighbors, yielding smoother but slightly blurred images.

Bicubic: Uses cubic polynomials over 16 nearest pixels to produce sharper, smoother results while better preserving edges.

Lanczos: Applies a sinc function kernel over a window (typically 3 lobes), excelling at preserving details with some ringing artifacts.

Spline: Fits piecewise polynomial curves to generate smooth, continuous transitions, ideal for gradual gradients but may oversmooth edges.

Each method reconstructs the image back to its original resolution.

5. Deep Learning-Based Super-Resolution
Load and apply a pretrained SRCNN model using TensorFlow/Keras for improved image reconstruction.

6. Evaluation Metrics
PSNR (Peak Signal-to-Noise Ratio): Measures pixel-level fidelity between reconstructed and ground truth images.

SSIM (Structural Similarity Index): Quantifies perceived visual quality by assessing structural similarity.

## Summary
Interpolation-based super-resolution methods were among the earliest approaches to image upscaling, offering simple, fast solutions without learning or external data. While effective for moderate enhancements, they cannot restore lost fine textures or details, motivating the use of deep learning models like SRCNN for superior results.

This project presents a comprehensive analysis and comparison of both classical and modern techniques, providing valuable insights for selecting appropriate methods in real-world image enhancement tasks.
