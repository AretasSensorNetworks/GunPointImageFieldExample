# GunPointImageFieldExample

The GunPoint dataset is a group of univariate sensor data samples that contain accelerometer data in one-axis for an event (a user pointing with their finger or drawing a gun from a holster). This is a binary classification problem (Gun or pointing). 

We import the GunPoint dataset (CSVs) into the Aretas platform and export to Image Field (GAF) for training on CNN and ViT (Vision Transformer)

We withold a subset of the data for "unseen" validation after the model is trained.

The CNN (using untrained ResNet50) acheived great results (99%) with very little tuning. However, the ViT model can get up to 100% accuracy on the validation set and ~100% on the witheld test set and is faster to train. 

Given the small sample size, this is fairly remarkable (in both instances). 

Converting univariate and multivariate sensor data into Image Fields has proven to be a very useful method for utilizing pre-built image models to perform classification tasks on sensor data events. 

You can use this method in the Aretas platform to export univariate and multivariate image fields of labelled data.

We no longer include the best performing models in the github repo, as such, your mileage may vary when you run this notebook against the dataset due to the randomized test/train split and randomization of the initial network parameters (the setSeed method provided by fast AI doesn't seem to provide consistency). 
