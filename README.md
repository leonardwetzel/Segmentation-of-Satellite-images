## Satellite Image Segmentation

This project demonstrates a deep learning approach to **satellite image segmentation**, focusing on detecting and delineating building roofs from aerial imagery. Using a **U-Net** architecture implemented in **PyTorch**, the model learns to generate pixel-level segmentations from a labeled dataset of satellite images.

### Data augmentation

The project was initially created for a task with a very limited amount (below 30) of low-res (256 x 256 pixels) satellite images.

To enhance performance on this limited data, the workflow integrates **data augmentation** via the *Albumentations* library and leverages a **pretrained encoder** from the *segmentation-models-pytorch* package (*resnet34* pretrained on *imagenet*). The model is trained and validated on separate subsets of the dataset, and the notebook provides a complete, reproducible pipeline — from data preparation and augmentation to training, evaluation, and visualization of results.

### Key Steps
- Construction of a custom PyTorch dataset for satellite imagery  
- Application of U-Net for semantic segmentation  
- Use of data augmentation to improve generalization  
- Training and inference on GPU (Google Colab environment)  
- Visual evaluation of segmentation performance  

