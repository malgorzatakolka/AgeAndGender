# Multi-task Age-Gender prediction based on UTKFaces dataset
This notebook provides the analysis and prediction for age and gender of UTKFaces dataset from https://www.kaggle.com/jangedoo/utkface-new.

The version that was used was preprocessed by provider to 200x200. This data was stored in personal drive and used through the analysis and modeling. Each image path is labeled: age_gender_ethnicity_path. Age is an integer from 0 to 116, indicating the age. Gender is either 0 (male) or 1 (female). Race is an integer from 0 to 4, denoting White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern).

The objective for this notebook was to build and train a single model which would perform regression on ages and classification on genders within single pass with possibly lowest MSE for age and highiest accuracy for gender. Then expaining the model with possible bias.

## EDA:

check of sizing, color channels and extensions of pictures
removing pictures with incomplete labels
analysing distributions
## Modeling:

For modeling part I used a couple of approaches with iterative adjustemnt of hyperparameters.

stratified split of train, validation and test set for each age/gender/ethicity group
adding layers to head
undersampling up to 250 samples in each age/gender/ethnicity group
experimenting with different batch sizes
augmentation of minority groups
experimenting with ResNet18 and ResNet34

## To run:
* upload the dataset to Drive
* run on Colab
