# Segmantic_Segmentation_Aerial_Images
Feature extraction from the Aerial Imagery

Aim- study to extract the feature from the aerial images and converting it into usable format.
Reducing the large amount of reduction in time and cost required for digitization manual work in Geospatial Industries

Sequence of how to implement the feature extraction from the images are as followes

Step 1: Data Preparation
Step 2: Model_Training
Step 3: Model_prediction
Step 4: Post_processing
Step 5: Index

Step 1: Data Preparation

The process begins with an exploration of the dataset's characteristics to gain insights into the challenges of accurate land cover and land use monitoring. Satellite and aerial imagery have transformed this field, but limitations persist in rural areas due to data resolution. To overcome these challenges, a comprehensive solution involving high-resolution aerial imagery and advanced machine learning techniques is proposed. Images are cropped into patches that align with the desired patch size, and similarly, corresponding mask patches are created. Subsequently, a selection process identifies patches containing meaningful information, ensuring they encompass non-zero labels of at least 5% in the mask. These useful image and mask pairs are then saved for further processing. The data is further organized by splitting it into training and testing subsets. This streamlined process, combining image pacification, mask processing, data curation, and splitting, forms the foundation for effective land cover and land use monitoring using semantic segmentation with deep learning algorithms.

Step 2: Model_Training

As U-net is the best model for the segmentation of the images (non-structured dataset) and Res-Net as a backbone structure. Increasing the effects of object feature detection weights of ImageNet is also use while compiling it.

Step 3: Model_Prediction

using the saved Model.h5 or Model.hdf5 file to predict unseen data set. Input data required to scale and resize to fit in pretrained model as same which is declaried while creating and training the data in Model_Training and the Data_Preparation.

Step 4: Post_Processing

As the segmenation is not end product of any study it is just the intermediat step in GIS Industry. As the most importing is the attribute imformation, geographical location, coordinate reference system (projection) and geometry (like area, length, distance,etc). Till noe all the processes is into raster data/ images, to do the analysis furthur need to convet the raster to polygon. Shapefile is the best file formate to store the vectore form and related attribute. Creating the supporting file, projecting the file, and able to save in various format (like csv, kml, html, etc)

Step 5: Visualization

Visualization can be done whith the help of Flask, Django, Streamlit, and HTML for the interative map. I had manage to apply with Flask.

