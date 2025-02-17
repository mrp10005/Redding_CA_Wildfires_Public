# Redding_CA_Wildfires_Public

* Image processing ML project on Redding, California.
* Utilized 
    * tensorflow
    * keras
        * Sequential
        * Dense, Flatten, Conv2D, MaxPooling2D, Dropout
        * layers
    * sklearn
        * neural_network: MLPClassifier
* I wanted to specifically train on a small geographic area and chose Redding, CA because it gets wildfires and I can also get tabular weather data from NOAA.
* NOAA labels wildfires in images with an orange color. I scanned 10 years of images of the approximate latitudes and longitudes of Redding and got the date that NOAA had the orange color. There were about 324 images (out of about 4000). I then tried to get images that also had a 'smog-like' color but that also got a lot of clouds. Finally I manually looked at the images that were around the dates where I had extracted the data NOAA had labeled with the orange color, this resulted in 426 wildfires images. I did not use images that had complete cloud coverage or where black (NOAA had some images that were just black).
* Images
    * The Images files are used to extract the labeled and unlabeled images from NOAA as well as get the dates where there are/are not wildfires, too many clouds, smog-like colors.
    * Used get requests to saved images with and without the orange wildfire label
* Model
    * The Model directory has the model notebooks
    * Keras Sequential Model
    * I did not do too much with this in terms of hyperparamter tuning. I was originally running it locally on my Mac and wanted to be cautious. Then got a new laptop and had to run three of the notebooks on Google Colab (one had to be changed a fair amount because Colab kept crashing) and the fourth is from March 2022 and I didn't change it.
* EDA
    * Dirty and clean Redding, CA csv files.
* Ways to improve performance:
    * More images
    * Hyperparameter tuning
    * Computer (can't run algorithms on current PC), Colab also crashes
    * Startified sampling
    * Create confusion matrix to analyze results
    * In the first model notebook validation performs better than train. Look into Dropout and variance/bias trade off
    * Definitely need a test set the model has never seen.