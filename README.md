# Face-Recogn
Face Recognition Using Eigenfaces. Python
Requirements:
    Python Version > 3.0
    Packages:
        numpy: http://www.numpy.org/
        PIL (Python Image Library): https://pillow.readthedocs.io/en/4.1.x/
        Scipy: https://docs.scipy.org/doc/
        Scikit-learn(sklearn): http://scikit-learn.org/stable/index.html
*Only the submodule of sklearn called "joblib" is used to create and read the database. (.pkl file)

*face.py has the main algorithm required for face recognition.
*func_code.py is a user defined library where i have written all the functions that might be required to use face.py
*face_recogn.py is a command line application built using face.py

Usage:
    Create a folder named "data_set" in the same directory containing the above three files.
    To train the algorithm to recognize a preson named 'xyz' face, create a folder named 'xyz' and 
     add all the revlevant image's of the persons face in that directory.
    Run face_recogn.py through command line: python face_recogn.py --udb
     database.pkl file will be created. This file is the trained database that can be used to load the model for prediction.
     
 
face_recogn.py:
    Usage Syntax: python face_recogn.py [agrument] [String Content]

    Positional Arguments:
        --cdb : create database from image path
        --ldb : load existing database from path
        --udb : add person to database
        --help : print this help and exit
        
face.py:
    The core Algorithm used to recognize the face is called as 'Eigenface':https://en.wikipedia.org/wiki/Eigenface

App improvements Required:
    While training the Algorithm from the data_set images, the images can be preprocessed in a way to corp only the persons
     face. So that unwanted data is eliminated. The teat image also need the same image processing so that there is no
     mismatch between the trained data and the test data.
    This will Improve the accuracy of the Model and multiple people's faces can be recognized from a single image.
    Face detection Algorithm can be used fro the OpenCV library.