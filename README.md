# Weakly-Supervised DAUnet
Welcome to Weakly-Supervised DAUnet, a weakly supervised domain adaptation framework for infant MRI skull-stripping using adversarial learning. This repository facilitates the adaptation of your model for this challenging task.

![third](https://github.com/user-attachments/assets/8fbe134a-621b-492f-88b0-c6b43a68f0c3)

# dHCP Data
We utilized the Developing Human Connectome Project (dHCP) dataset as a part of our target dataset, a comprehensive resource containing high-resolution T1- and T2-weighted neonatal MRI scans with weakly annotated segmentation masks. This dataset plays a critical role in improving the model's generalization across diverse newborn brain anatomies.

# GMM Data
The code for creating synthetic data can be found in the GMM folder. This synthetic data, generated using a Gaussian Mixture Model, enriches the diversity of training data and can be integrated into your source dataset directory. For access to the GMM dataset, please contact us using the information in the Contact Us section.

# Adult Data
We also have leveraged the CALGARY-CAMPINAS PUBLIC BRAIN MR DATASET, available at [this link](https://sites.google.com/view/calgary-campinas-dataset/home). Please download the dataset from the provided link to proceed. Additionally, we have included sample data-split CSV files in the Data-split folder to help you organize your data.

# Newborn Data
A private dataset from Alberta Children’s Hospital, gathered using a GE 3T MRI scanner, was used as a part of our target dataset. This dataset complements the dHCP data in training and evaluating the model.

# Configuration
The current patch size for both adult and newborn data is set to 112x112x122. However, you can easily customize the patch sizes for both datasets by modifying the parameters in the data_loader_da.py script.

# Getting Started
To run the code, execute the following command, making sure to adjust the paths to your source and target data splits and your desired output folder:

`python main.py --batch_size 2 --epochs 400 --source_dev_images Data-split/source_train_set_neg.csv --source_dev_images Data-split/source_train_set_masks_neg.csv --source_dev_images Data-split/target_train_set.csv --results_dir Outputs`

# Resuming Training
If you need to resume your training, simply include the `--resume_training True` argument in your command.

# Download Trained Weights
Trained model weights can be downloaded from [this link](https://sites.google.com/view/calgary-campinas-dataset/home)

Feel free to reach out if you have any questions or need assistance.

### Contact us
Feel free to contact us via email or connect with us on LinkedIn.

- Abbas Omidi --- [Linkedin](https://www.linkedin.com/in/abbasomidi77/), [Github](https://github.com/abbasomidi77), [Email](mailto:abbasomidi77@gmail.com)
