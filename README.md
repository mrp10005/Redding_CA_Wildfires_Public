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
* Model
    * The Model directory has the model notebooks
    * I did not do too much with this in terms of hyperparamter tuning. I was originally running it locally on my Mac and wanted to be cautious. Then got a new laptop and had to run three of the notebooks on Google Colab (one had to be changed a fair amount because Colab kept crashing) and the fourth is from March 2022 and I didn't change it.
* The EDA directory has dirty and clean Redding, CA csv files.

* Overall, it's pretty difficult to look at an image and see if there was a wildfire. There are some images that look like there is no wildfire but NOAA had them labeled as wildfire. The model does do pretty well on an image with smoke. Overall, MLPClassifier was very bad but the Keras Sequential model was ok.