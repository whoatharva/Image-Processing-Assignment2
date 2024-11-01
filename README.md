# Computer Vision Image Processing - Assignment 2  
### IIT Gandhinagar

This repository contains implementations of various image processing techniques, including Gaussian blur, edge detection algorithms, and different blending methods.

## Features

### 1. Image Loading and Processing
- Custom implementation for loading images from Google Drive
- Automatic RGB color space conversion
- Support for different image formats

### 2. Gaussian Blur Implementation
- Custom Gaussian kernel generation with configurable parameters
- Support for different kernel sizes (3x3, 5x5, 7x7)
- Variable sigma values (1, 10, 50)
- Comparison with OpenCV's implementation

### 3. Edge Detection Algorithms

#### Sobel Edge Detection
- Horizontal and vertical edge detection
- Custom implementation of Sobel operators
- Edge magnitude calculation
- Comparison with OpenCV's Sobel implementation

#### Laplacian Edge Detection
- Custom Laplacian kernel implementation
- Edge enhancement and detection
- Comparison with OpenCV's Laplacian implementation

### 4. Advanced Blending Techniques
- Alpha Blending (configurable alpha values)
- Multiply Blending
- Screen Blending
- Overlay Blending
- Gradient Magnitude Blending
- Adaptive Blending
- Directional Blending

## Requirements
- `python`
- `numpy`
- `matplotlib`
- `opencv-python`

## Usage

1. Set up the working directory:
    ```python
    WORKING_DIR = '/your/working/directory'
    IMAGE_PATH = os.path.join(WORKING_DIR, 'RGB.jpg')
    ```

2. Run the main script:
    ```bash
    python untitled21.py
    ```

   Results will be saved in a `results` folder within your working directory.

## Function Documentation

### Image Processing Functions
- `load_image_from_drive()`: Loads and converts an image to RGB format.
- `create_gaussian_kernel(size, sigma)`: Creates a normalized Gaussian kernel.
- `custom_convolution(image, kernel)`: Applies convolution operation.
- `custom_gaussian_blur(image, kernel_size, sigma)`: Applies Gaussian blur.

### Edge Detection Functions
- `custom_sobel(image)`: Implements Sobel edge detection.
- `custom_laplacian(image)`: Implements Laplacian edge detection.

### Blending Functions
- `alpha_blend(image1, image2, alpha)`: Linear blending of two images.
- `multiply_blend(image1, image2)`: Multiplicative blending.
- `screen_blend(image1, image2)`: Screen mode blending.
- `overlay_blend(image1, image2)`: Overlay mode blending.
- `gradient_magnitude_blend(edges_x, edges_y)`: Combines edge maps using magnitude.
- `adaptive_blend(edges_x, edges_y)`: Adaptive edge combination.
- `directional_blend(edges_x, edges_y, angle_weight)`: Direction-based blending.

### Utility Functions
- `plot_results(original, processed, title)`: Visualizes results.
- `save_results(image, filename)`: Saves processed images.

## Output

The script generates multiple output files comparing different techniques:
- Gaussian blur results with varying parameters
- Sobel edge detection maps (horizontal, vertical, combined)
- Laplacian edge detection results
- Various blending results
- Comparisons with OpenCV implementations

## Notes
- All implementations include comparisons with OpenCV's built-in functions.
- Results are automatically saved and displayed.
- Edge maps are normalized for better visualization.
- The code includes error handling and proper file management.
