# TA-Skripsi
Documentation for Undergraduate thesis project, a CNN based classification of Alzheimer's disease stages from brain MRI scans using TensorFlow

## Dataset
The dataset used for training this model is a **preprocessed version available on Kaggle Dataset**, specifically designed for CNN classification. This preprocessed dataset is based on the **OASIS MRI Images Dataset**, which is also publicly available on Kaggle.

The preprocessing involved several key transformations to prepare the raw grayscale MRI images (originally 248x496 pixels) for CNN input:
* **Initial Cropping (6px left, 40px right):** This was performed to horizontally center the brain object within the image. Resulting dimensions: 248x450 pixels.
* **Adding Padding (64px top, 63px bottom):** Black pixels were added to vertically center the object. This step also increased image height for better variation during subsequent vertical shift data augmentation. Resulting dimensions: 375x450 pixels.
* **Resizing:** Finally, all images were scaled down to a standardized size of 150x180 pixels, optimized for model input.

Link to Kaggle Dataset
* [**Link to the Preprocessed Dataset**](https://www.kaggle.com/datasets/rafaelmahesa/imageoasis-150x180-aug-5fold)
* [**Link to the original OASIS MRI Images Dataset on Kaggle**](https://www.kaggle.com/datasets/ninadaithal/imagesoasis)