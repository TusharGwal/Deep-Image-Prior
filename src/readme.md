# Deep Image Prior (DIP) for Image Restoration

## Project Overview
This project implements various image restoration tasks using Deep Image Prior (DIP), a method that leverages the structure of convolutional neural networks (CNNs) as an implicit prior for natural images. The network is trained without a large dataset, instead focusing on fitting a single corrupted image through an optimization process. The project is developed as part of the CS512 - Computer Vision course (Fall 2024).

### Team Members
- Manoj Gembali (A20527288)
- Tushar Gwal (A20449419)



### Plots, GIFs, and Outputs
The plots, GIFs, and reconstructed images are saved in their respective task folders after running the corresponding parts of the script.


#### Denoising
- Denoising/ folderContains the original uncorrupted image, noisy input, best output, and training plots for denoising
- By default, the script runs with the default image provided in this folder
- To use a different image, update the `img_path` variable in the script
- In the addnoise function, you can vary the standard devaition paramter of the noise to be added

#### TextInpainting
- TextInpainting/ Contains the original image, mask image, inpainted result, and corresponding training plots
- By default, the script runs with the default images provided in this folder
- To use different images or masks, update the `img_path` and `mask_path` variables in the script
- Can use the maskcreator notebook file to generate custom text masks

#### HoleFilling
- HoleFilling/ Contains the original image, images with holes, the filled output, and training plots
- By default, the script runs with the default images provided in this folder
- To use different images or masks, update the `img_path` and `mask_path` variables

#### Reconstruction
- Reconstruction/ Contains the original uncorrupted image, randomly masked images, the reconstruction result, and training plots
- By default, the script runs with the default image provided in this folder
- To use a different image, update the `img_path` variable in the script
- Adjustable Bernoulli Mask Percentage: Users can vary the Bernoulli mask percentage by modifying the p parameter in the script to control the level of image masking

**Note**: By default, all tasks run with the provided images in the respective folders. If you wish to experiment with different images or masks, modify the file path variables (`img_path`, `mask_path`) in the script accordingly.

## Additional Script: Text Mask Creation
This project includes a Jupyter Notebook script (`maskcreator.ipynb`) to create an inverted text mask (black text on a white background) using an input image. The script, `create_text_mask`, allows you to specify multiple texts with different properties such as:
- Position
- Font size
- Rotation
- Alignment

The generated mask can be used for the inpainting task.

### Usage
The script takes an input image and a list of text properties, then generates and saves the text mask. By default, the generated mask is saved in the same folder as the input image.

## Running the Project

### Dependencies
Install the required libraries using `requirements.yml` or set up a conda environment.

### Training
Modify the image paths and masks if needed, and run the corresponding sections in the script to perform:
- Denoising
- Inpainting
- Hole filling
- Reconstruction