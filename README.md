# Feast
Feast is an operational data system for managing and serving ml features to models in production.
Feast is able to serve feature data to model from a low latency online store or from an offline store.

# Feast-Feature-store
1. Prepare the Data set into a parquet file format
2. Create a feature repo (feast init)
3. Define feature definitions and update feature_store.yaml file if needed
4. Register and deploy the features (created using feast init)
5. Feast apply (under feature_repo)
6. Generate training data set from feature_store repo
7. Model training
8. Prepare an online feature store
9. Feature serving to model in production

# Feature definition
Set of features/columns out of the dataset which we want to store inside the feast store repo so that they can be further served as
training dataset or online prediction.

# Feast Init
It will create a feature repo directory.  And it will have data, a feature_store.yaml file, and a Feature definition.py file.
Data- Inside data, we can keep our data. 
Feature definition.py - Set of features/columns out of the dataset which we want to store inside the feast store repo
Feature_store.yaml - It contains some metadata of the feature mentioned in feature_defition and info regarding the project.
It contains a demo setup configuring where data sources are
Command - !feast init feature_repo

# Feast Apply
It will create a feature view, entity, and registry. db 
Command -!feast apply

# Generate training data
Here we will load only the required columns out of which we mentioned in the definition file and will save them into the feature store data directory.

# Model Training
Load the saved data and train, save the model 

# Online feature store
Load the features to the online feature store according to the use case(date and time).

# Get online features for prediction
Load the data from the online feature store with the specific primary key to do a prediction

