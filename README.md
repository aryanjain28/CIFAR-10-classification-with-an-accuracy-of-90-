# CIFAR-10 classification.
Convolutional classification model with an accuracy of ~90%.

# Introduction : 

CIFAR is an acronym that stands for the Canadian Institute For Advanced Research. 
The dataset is comprised of 60,000 32×32 pixel color photographs of objects from 10 classes. The class labels and their standard associated integer values are listed below.

    0: airplane
    1: automobile
    2: bird
    3: cat
    4: deer
    5: dog
    6: frog
    7: horse
    8: ship
    9: truck


# Modules Used : 
  
   1. Tkinter for GUI.
   2. Keras for Deep Learning.
   
# Failed/Unsatisfactory models : 

As shown below, these are screenshots of models that gave unsatisfactory results upon training.
Basically, there were two cases that were not favourable : 
    
    1. Accuracy was stuck at ~75%.
    2. After a set of epochs overfitting occured.
    
    
<br>

Case 1 : As you can see below, after around 40 epochs, overfitting occured : <br>
<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/model-998.PNG"></p>
       
<br><br>

Case 2 : Learnt from  my mistakes above, I tried the following, but in this case the accuracy was stuck at ~80%.<br>
<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/model-999.PNG"></p>
<br>
<p align="center">When I incresed number of epochs, the accuracy further decresed.</p>
<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/model-999-(200)-a.PNG"></p>

       
<br><br>

Case 3 : Again, as shown below, when I added Kernel Regularization to overcome above scenario, overfitting occured.<br>
<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/model-9991.PNG"></p>

There are few more cases that I tried training upon. But all were failed due to similar reasons.
    

# Best models : 

<br>
<p align='center'> Model 1 : I used Relu activation function and ADAM optimizer with 125 number of epochs </p>
<p align='center'> with decresing Learning rate and voila! I got a stable accuracy of ~90%.</p>

<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/best/RELU/Best-model-Activation-RELU.PNG"></p>

    If you take a closer look at figure above, 
    you will observe an increment in accuracy at epoch 75 as well as at 100.
    This is were I decreased my learning rate.
    This is the model that is used in project.
    
<p align='center'> I tried to increase the accuracy by incresing number of epochs to 175</p> 
<p align='center'> and further decresing Learning rate, but results were not as I expected them to be. </p>

<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/best/RELU/Best-model-Activation-RELU-175.PNG"></p>

    You can observe after 125 epoch overfitting started to occur.
    
<br><br>
<p align='center'> Model 2 : Here, I used Elu activation function and RMSProp optimizer </p>
<p align='center'> with same 125 number of epochs  with decresing Learning rate.</p>
<p align="center"><img width="460" src="/CIFAR-10/testModelsImages/best/ELU/Best-model-Activation-ELU.PNG"></p>


# Screenshots : 

<br>
<p align="center"><img width="460" src="/CIFAR-10/Screenshots/Screenshot-1.PNG"></p>
<br>
<p align="center"><img width="460" src="/CIFAR-10/Screenshots/Screenshot-2.PNG"></p>
<br>
<p align="center"><img width="460" src="/CIFAR-10/Screenshots/Screenshot-3.PNG"></p>


# Refernces : 

<a href='https://machinelearningmastery.com/how-to-develop-a-cnn-from-scratch-for-cifar-10-photo-classification/'>Link 1</a>
<br><br>
<a href='https://appliedmachinelearning.blog/2018/03/24/achieving-90-accuracy-in-object-recognition-task-on-cifar-10-dataset-with-keras-convolutional-neural-networks/'>Link 2</a>
