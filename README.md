## Model - RNN 

### Data set [link](https://github.com/YashvanthD/Voice-Emotions-Data)
  * RAVADEES 
  * SAVEE
  * CREMA
  * TESS

## _**Note**_

```diff
- Create your own branch and Please Push in your branch only
```


### How to Save a Model

    model_json = model.to_json()
    with open("model.json", "w+") as json_file:
       json_file.write(model_json)
      
    # serialize weights to HDF5
    model.save_weights("model.h5")


### How to load a model

    from keras.models import model_from_json

    json_file = open('model.json', 'r+')
    loaded_model_json = json_file.read()
    json_file.close()
    
    loaded_model = model_from_json(loaded_model_json)
    
    # load weights into new model
    loaded_model.load_weights("model.h5")
    loaded_model.compile(loss='categorical_crossentropy', optimizer='rmsprop', metrics=['accuracy'])
    
 ### Evaluating the model
 
    print("Accuracy of our model on test data : " , loaded_model.evaluate(x_test,y_test)[1]*100 , "%")

### **Requirements files**
    
 Feature file <br>
 
    
    features.csv
    
    
 model file <br>
    
    
    
    model.h5
    
    
 model configurationn <br>
    
    
    model.json 
    
    





