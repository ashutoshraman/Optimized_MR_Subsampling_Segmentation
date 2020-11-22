# Optimized_MR_Subsampling_Segmentation

This is a small repository containing code for how to optimize subsampling of MR k-space data in order to decrease scan times and cost, while preserving resolution, signal, and ability to effectively segment. 

A U-Net architecture is implemented and trained in order to perform binary semantic segmentation, and create a mask from a given image of a brain, with the mask being a tumor.
This U-Net is further used to optimize another Physical Layer, which forces the CNN to choose columns of k-space to sample, in order to still accurately recreate the mask with minimal error. As number of samples the CNN is allowed to incorporate is decreased, the CNN is forced to choose only the most important ones for accurate mask prediction and reconstruction. Metrics for comparison include loss (SparseCategorical and Binary Cross Entropy are both used and are interchangeable as long as model is correspondingly altered to fit the loss function). Other metrics are accuracy, which in segmentation is pixel-to-pixel, PSNR, and Mean Intersection over Union.

This project was completed as part of the BME548: Machine Learning in Imaging class at Duke University. All resources are open-source and don't require reference.
