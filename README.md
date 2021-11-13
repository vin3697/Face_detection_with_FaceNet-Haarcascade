# Face_detection_with_FaceNet-Haarcascade

***** https://github.com/davidsandberg/facenet/wiki/Classifier-training-of-inception-resnet-v1 *****

Steps to train the model for face recognition!

#https://github.com/nemuelpah/Face-Recognition-with-FaceNET/blob/main/FaceRecog_with_COLAB.ipynb (I took help from this gentlemen)

FaceNet is the model (pretrained)

It uses method of One shot training! so we dont have to train the model with many pictures
Amazingly with one pic as well we can train it!


Haar Cascaded classifier(its not CNN but a signal based model[rules are defined which makes the face capturing easy]) -> FaceNet (CNN) -> column vector matrix 128*1 (its not the confidence rather its a unique values for praticular face) -- face signature!
and at the output we will have the number of neurons equal to number of faces/labels we have given to the network while training

Haar cascad will detect the face and recognition will be done by the FaceNet!
Frobenius Norm - to know the difference between face signatures its same as Euclidean Distance
the output vector is compared with the signatures and whoever has the least error, that signature is given to the face with label.


haarcascade xml document.
facenet_keras.h5 file

Database where sigantures are stored the file type is pickle (file_name.pkl)


#> Haarcascade syntax is imp!

OpenCv BGR
Pillow RBG - image format used by these lirabries!! 

Nomralization of capptured face is done in generation of dataset because the FaceNet uses normalized iamge for processing

Face Net takes 4 dimension input 
> number of faces * width * height * channel(eg RBG - 3 channels)

#Test Images!
The accuracy is great! I have taken these pics in very low light!
![test_1](https://user-images.githubusercontent.com/92587549/141658206-4cb819c7-fbc1-41ae-9d5b-0485ef5f9594.JPG)


![test_2](https://user-images.githubusercontent.com/92587549/141658210-d4c1ecd1-52c6-48ab-bed5-1385aa8e7aa4.JPG)

