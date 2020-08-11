# AgePrediction
The task is to predict the age of a person from his or her facial attributes. For simplicity, the problem has been converted to a multi-class problem with classes as Young, Middle and Old. Here the problem is found to be of Computer Vision.  So we have to train the model in such a way that it can predict the age of the actor as young, middle age or old.

# Dataset
Here Ihave used Indian movie face dataset, which is a large unconstrained face database consisting of 34512 images of 100 Indian actors collected from more than 100 videos. All the images are manually selected and cropped from the video frames resulting in a high degree of variability interms of scale, pose, expression, illumination, age, resolution, occlusion, and makeup. IMFDB is the first face database that provides a detailed annotation of every image in terms of age, pose, gender, expression and type of occlusion that may help other face related applications. This dataset is available at http://cvit.iiit.ac.in/projects/IMFDB/

# Steps applied to solve the problem

*	The libraries that were used are numpy, pandas, matplotlib, PIL, os, scikit-learn, keras and tensorflow.
*	First the labels that are stored in csv file in coloumn ‘ID’ are encoded using labelencoder.
*	The images are opend after that and as the images are of diffrent size they are converted into 32X32.
*	I than created array of all such images to treate into model.
*	Splitting of the data into test and train.
*	Also used autoencoder to reduce data dimensions by learning how to ignore the noise in the data.

# Model Metrics

*	Accuracy : 0.7105
*	Loss : 0.6746
*	Val_accuracy : 0.7261
*	Val_loss : 0.6739
