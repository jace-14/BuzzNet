A. Step-by-step instructions on what source code to execute for each item in Number 2, including the actual command to use.
	1. To group the dataset from the HumBugDB into the classes, run the 'group.py' python file
	2. To sort the audio files from the longest to shortest and then split it into the training, validation, and testing sets in a 70:15:15 ratio, run the 'tvt_split.py' python file
	3. To splice the audio files into 1.92s chunk durations, run the 'splice.py' python file
	4. To convert the 1.92s chunk audio files while ignoring audio files that are less than 1.92s, run the 'convert.py' python file (logmel, mfcc, pcen)
	5. By running these pythons scripts in chronological order, the final dataset will be created

B. Step-by-step instructions on what source code to execute to train and test the model (backend)
	1. To train and test the model, open the 'siamese_vgg19_svm.ipynb' file as a jupyter notebook.
	2. After opening the file as a jupyter notebook, make sure that all dependencies are installed (those that are being imported at the notebook)
	3. Do not forget to include all the necessary models for the pre-trained CNN models (contained in the models subfolder)
	3. The notebook contains how the Siamese CNN-SVM model can be trained and tested using the three different spectrogram pairs.
	4. To get to the best performing model, execute the appropriate lines of code for the spectrogram pair, Log-mel+MFCC.
	5. The model will then be trained and will be able to generate predictions afterwards for testing.
	6. Other spectrogram pair inputs can also be executed, as well as for the single spectrogram image input CNN-SVM model under the 'singlespec_vgg19_svm.ipynb' file.

C. Step-by-step instructions on what source code to execute to deploy the model (frontend)
	1. To execute the deployed model, from the 'BuzzNet Web App', open the 'app.py' file using any Python IDE (example: PyCharm)
	2. Make sure that all dependencies are installed (those that are being imported at the python file)
	3. Do not forget to include all the necessary models for the Siamese CNN model as well as the BuzzNet model (contained within the same directory)
	4. To execute the deployed web application, simply execute the 'app.py' file and access the address using any up-to-date web browser (example: Google Chrome).
	5. Upload mosquito audio files from the system files an upload into the web app to generate the predictions.