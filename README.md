# Low-Light Image Enhancement Techniques

This repository focuses on various techniques for enhancing images captured under low-light conditions. These methods are critical for improving image quality in suboptimal lighting, ensuring accurate object/face recognition, and enhancing the overall visual experience.

## Techniques Covered

### 1. Zero-DCE (Deep Curve Estimation)
Zero-Reference Deep Curve Estimation (Zero-DCE) is a deep learning-based method for low-light image enhancement. It is data-driven and considers multiple light enhancement factors in the design of non-reference loss functions, offering improved robustness, wider dynamic range adjustment, and lower computational overhead.

**Key Components:**
- **Light-Enhancement Curve (LE-curve):** Ensures normalized pixel values, preserves pixel contrast, and supports gradient backpropagation.
- **DCE-Net:** A CNN with seven convolutional layers for mapping input images to curve parameter maps.
- **Non-Reference Loss Functions:**
  - Spatial Consistency Loss
  - Exposure Control Loss
  - Color Constancy Loss
  - Illumination Smoothness Loss

### 2. Single Backlit Image Enhancement
This method enhances images with backlit conditions by generating a balanced intensity image using gamma correction and histogram equalization. The technique further improves the image quality by employing a guided filter and alpha blending.

**Key Steps:**
- **Guided Filter:** Creates a smoothed binary image based on intensity histogram analysis.
- **Alpha Blending:** Combines the input and enhanced intensity images using a weight map derived from the binary image.

### 3. Prompt Learning for Unsupervised Backlit Image Enhancement (CLIP-LIT)
This unsupervised method leverages Contrastive Language-Image Pre-Training (CLIP) for pixel-level image enhancement. The technique involves prompt learning to refine image enhancement results through rank learning.

**Stages:**
1. **Initial Prompt Pair Learning:** Constrains text-image similarity using a frozen CLIP model.
2. **Prompt Refinement:** Refines prompts using backlit and well-lit images.

## Performance Metrics
The following metrics are used to evaluate the techniques:

| Method                  | PSNR (dB) | NIQE |
|-------------------------|-----------|------|
| Zero-DCE                | 4.68      | 5.15 |
| Backlit Image Enhance   | 17.12     | 4.14 |
| Prompt Learning (CLIP)  | 13.96     | 4.46 |

## References
- [CLIP-LIT: Contrastive Language-Image Pre-Training for Image Enhancement](https://zhexinliang.github.io/CLIP_LIT_page/)
- [Single Backlit Image Enhancement](https://github.com/HumanChwan/single-backlit-image-enhancement)
- [Keras Image Enhancement Examples](https://keras.io/examples/vision)

## Author
- **Singam Setty Deshik**  
  *2101AI32*
