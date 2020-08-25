# Intended use for the algorithm

Assist radiologist in computing hippocampal volumes along the anterior and posterior dimensions.

# Indications of use

Use for MR brain T2 scans on axial 2D slices.

# About the algorithm

Recusive U-Net algorithm is used to segment the cropped axial slice of human brain. Volume is then computed on the predicted mask. The model is trained on ground truth obtained from medical decathlon competition. The training data was labeled using any of the medical tools such as 3D slicer which makes it easy to create masks on images.

# Training Performance
Overall dice score on training dataset is 0.89. In real world, the performance can be measured by computing the dice score between the predicted labels and the labels curated by radiologists on MR brain T2 scans of axial slices.

In real world, the algorithm will only perform well on T2 scans of MR brain and using axial slices only. This means sagittal and coronal slices won't give good performance, or that using non-T2 scans like T1-scans will not give good results.

