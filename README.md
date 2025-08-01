# Water Segmentation from Multispectral Satellite Imagery

This project is a web-based application for segmenting water bodies from 12-channel multispectral satellite images. It utilizes a U-Net architecture with a fine-tuned ResNet50 encoder, built with TensorFlow and Keras, and is deployed using a Flask web server.

## Demo

The application provides a simple interface to upload a `.tif` image and view the resulting water segmentation mask overlaid on the true-color representation of the image.

![Application Demo](./assets/Animation.gif)

## Features

- **Deep Learning Model**: Employs a U-Net with a pre-trained ResNet50 backbone for high-accuracy semantic segmentation.
- **Multispectral Data**: Processes 12-channel TIF images, leveraging rich spectral information.
- **Web Interface**: A user-friendly web app built with Flask for easy interaction.
- **Dynamic Visualization**: Generates and displays a true-color image and a prediction overlay for immediate visual feedback.

## Example Results

Here are some examples of the model's output on test images:

| True Color Input | Prediction Overlay |
| :--------------: | :----------------: |
| ![Result 1](./assets/result1.png) | ![Result 2](./assets/result2.png) |

## Tech Stack

- **Backend**: Python, Flask
- **Deep Learning**: TensorFlow, Keras
- **Image Processing**: OpenCV, Pillow, Matplotlib, Tifffile
- **Frontend**: HTML, CSS

## Setup and Installation

To run this project locally, follow these steps.

### Prerequisites
- Python 3.9+
- Git and Git LFS (for handling the large model file)

### Installation Steps

1.  **Clone the repository:**
    *First, ensure you have Git LFS installed. If not, download and install it from [git-lfs.github.com](https://git-lfs.github.com), then run `git lfs install`.*

    ```bash
    git clone <your-repository-url>
    cd water_segmentation_app
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # For Windows
    python -m venv venv
    venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  **Run the Flask application:**
    ```bash
    python app.py
    ```

2.  **Open the application in your browser:**
    Navigate to `http://127.0.0.1:5000`.

3.  **Upload an image:**
    Click "Choose File", select a 12-channel `.tif` image (you can use the one provided in the `sample_data` folder), and click "Upload and Predict".

4.  **View the results:**
    The page will display the true-color version of your input and the segmentation overlay.
