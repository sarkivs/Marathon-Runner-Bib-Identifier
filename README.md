```markdown
## Marathon Bib Number Detector

This project provides a Jupyter Notebook for detecting and reading marathon bib numbers from images. It uses a custom-trained object detection model to locate the bib and then optical character recognition (OCR) to extract the number.

---

## Features

* **Object Detection:** Identifies the location of the marathon bib on a runner.
* **Optical Character Recognition (OCR):** Reads the bib number from the detected bib.
* **Visualization:** Displays the processed image with bounding boxes around the bib and the extracted number.

---

## Prerequisites

Before running the notebook, you'll need to install the necessary libraries and set up your Roboflow account.

1.  **Roboflow Account:** Create a free account on the [Roboflow website](https://roboflow.com/) to access and manage your dataset and model.
2.  **API Key:** Obtain your Roboflow API key from your account settings. This key is required to download the trained model.
3.  **Required Libraries:** Install the following Python libraries using pip:

    ```bash
    pip install roboflow opencv-python numpy
    ```

---

## Setup and Usage

Follow these steps to get the project running:

1.  **Clone the Repository:** Clone this GitHub repository to your local machine.

    ```bash
    git clone [your-repository-url]
    cd [your-repository-name]
    ```

2.  **Set Up Roboflow:**
    * Open the `bib_detector.ipynb` Jupyter Notebook.
    * In the first code cell, replace the placeholder with your Roboflow API key:

    ```python
    # Replace with your Roboflow API key
    ROBOFLOW_API_KEY = "YOUR_API_KEY_HERE"
    ```

3.  **Add Inference Images:**
    * Place the images you want to process into the **`inference`** folder. The notebook is set up to read all `.jpg` and `.png` files from this directory.

4.  **Run the Notebook:**
    * Execute the cells in the Jupyter Notebook sequentially. The notebook will:
        * Download the trained object detection model from Roboflow.
        * Load and process each image in the `inference` folder.
        * Detect the bib and use OCR to read the number.
        * Display the results, including the bounding boxes and the extracted number.

---
