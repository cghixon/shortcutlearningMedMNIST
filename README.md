# Exploring Shortcut Learning with MedMNIST data
  **Shortcut Learning** (Geirhos et al, 2020) is found when data performs well with IID data but _not OOD data_. <br />
  Shortcuts are revealed when tested under slightly different circumstances. <br />
  A more detailed explanation of shortcut learning is in file named Shortcute Learning in Deep Neural Networks.
  
  This project explores shortcut learning by comparing various NN models and testing environments using two data sets from MedMNIST. <br />
  There are _4 NN models_, _3 testing environments_, and _2 MedMNIST datasets_ used (breast and pneumonia).
  
## Study Methodology
Description of neural network models built and testing environments.

  ### Models:
  
  - _Simple FC neural net_ (3 dense layers)
  - _Baseline CNN_ (1 Conv2D, kernel size 3, relu + maxpool size 2)
  - _CNN with BN and dropout_ (2 Conv2D layers, keneral size 3, relu + maxpool size 2, Batch Norm, dropout of 0.5)
  - _ResNet_ (4 residual layers)
    
   ### Testing Environment:
   
  - No augmentation
  - Test set augmentation (random shifts, rotations)
  - Train and test set augmentation (random shifts, rotations)
        
## Data
Overview of MedMNIST datasets.

  ### Breast MedMNIST:
  
  - Breast ultrasound
  - Binary class (2)
  - 780 samples
  - Access to data: https://zenodo.org/record/6496656#.Ym7bZ-jMKHs

  ### Pneumonia MNIST:
  
  - Pneumonia chest x-ray
  - Binary class (2)
  - 5,856 samples
  - Access to data: https://zenodo.org/record/6496656#.Ym7bZ-jMKHs

## Results
Overview of model results. More detailed results and images can be in attached file.

  ### Breast:
  - _Highest train acc_: 90.66 from CNN with dropout and test only augmentation
  - _Highest validation acc_: 80.77 from Baseline CNN and test only augmentation
  - _Highest test acc_: 79.49 from Baseline CNN and test only augmentation

  ### Pneunomia:
  - _Highest train acc_: 97.77 from ResNet and train/test augmentation
  - _Highest validation acc_: 96.76 from CNN with dropout and no augmentation
  - _Highest test acc_: 86.38 from Baseline CNN and train/test augmentation


