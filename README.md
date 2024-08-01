# Image to Coloring Book Project

## Overview

This project converts an input image into a format suitable for a coloring book. The conversion process involves image preprocessing, applying Gaussian blur, and clustering the image colors. The resulting images can be used as outlines for coloring books.

## Features

- Convert any image to a black-and-white outline suitable for coloring.
- Optionally apply Gaussian blur to smooth out small features in the image.
- Generate a color palette based on the original image.

## Requirements

- Python 3.x
- NumPy
- TensorFlow
- PIL (Pillow)
- Scikit-Image
- Scikit-Learn
- Matplotlib

## Installation

Install the required packages using pip:

```sh
pip install numpy tensorflow pillow scikit-image scikit-learn matplotlib
```

## Usage

The main script is contained within a Jupyter notebook. To use the script, follow these steps:

1. **Open the Jupyter notebook:**

    ```sh
    jupyter notebook ImageToColoring.ipynb
    ```

2. **Run the notebook cells to process your image.** 

    Ensure you have an image file ready to process. You can adjust parameters like the amount of Gaussian blur and the number of color clusters.

3. **Example Usage:**

    ```python
    from ImageToColoring import ColorBooked

    # Initialize the ColorBooked class with the image path, blur value, and number of centroids
    colorbook = ColorBooked("path_to_your_image.png", blur_value, num_centroids)

    # Generate the coloring book image
    colorbook.generate_colorbook_image()
    ```

## Parameters

- `img_fname` (str): Path to the image file.
- `blur` (int or None): Amount of Gaussian blur to apply. If `None`, a default value is used.
- `num_centroids` (int): Number of color clusters to generate.

## Methods

### `ColorBooked`

- `__init__(self, img_fname, blur, num_centroids)`: Initializes the object with the provided parameters.
- `_preblur_img(self, blur)`: Applies Gaussian blur to the image.
- `_normalize_img(self)`: Normalizes the image data.
- `generate_colorbook_image(self)`: Generates the coloring book image and saves it.

## Example Output

The processed image will be saved with a suffix indicating the number of color clusters used, e.g., `your_image_colorized10.png`. The final color list and number of colors are also outputted.

## Contributions

Contributions to this project are welcome. Please fork the repository and submit a pull request.
