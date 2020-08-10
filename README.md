# AgePrediction
The task is to predict the age of a person from his or her facial attributes. For simplicity, the problem has been converted to a multi-class problem with classes as Young, Middle and Old. Here the problem is found to be of Computer Vision.  So we have to train the model in such a way that it can predict the age of the actor as young, middle age or old.

# Steps applied to solve the problem

•	The libraries that were used are numpy, pandas, matplotlib, PIL, os, scikit-learn, keras and tensorflow.
•	First the labels that are stored in csv file in coloumn ‘ID’ are encoded using labelencoder.
•	The images are opend after that and as the images are of diffrent size they are converted into 32X32.
•	I than created array of all such images to treate into model.
•	Splitting of the data into test and train.
•	Also used autoencoder to reduce data dimensions by learning how to ignore the noise in the data.

# Model Architecture 

•	BatchNormalization(input_shape = (32,32,3)),
•	Convolution2D(28,(3,3), activation='linear'),
•	LeakyReLU(alpha = 0.3),
•	BatchNormalization(),
•	Convolution2D(32,(3,3), activation='linear'),
•	LeakyReLU(alpha = 0.3),
•	BatchNormalization(),
•	MaxPooling2D(),
•	Convolution2D(64,(3,3), activation='linear'),
•	LeakyReLU(alpha = 0.3),
•	BatchNormalization(),
•	Convolution2D(128,(3,3), activation='linear'),
•	LeakyReLU(alpha = 0.3),
•	BatchNormalization(),
•	MaxPooling2D(pool_size=(2, 2)),
•	Flatten(),
•	Dropout(0.2),
•	Dense(384, activation='linear'),
•	LeakyReLU(alpha = 0.3),
•	Dropout(0.2),
•	Dense(3, activation='softmax')

# Model Metrics

•	Accuracy : 0.7105
•	Loss : 0.6746
•	Val_accuracy : 0.7261
•	Val_loss : 0.6739
