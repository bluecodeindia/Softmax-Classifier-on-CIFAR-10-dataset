# Softmax-Classifier-on-CIFAR-10-dataset

1. Download the data CIFAR-10 dataset and extract in the data folder.

2. The CIFAR-10 dataset has 50,000 images for the training and 10,000 images for the test.

3. Each image size is 32 x 32 pixels.
5. First you need to create a python dictionary and set the following parametrs:
  - learning_rate: to set the learning rate of the model.
  - num_iters: number of iteration or epochs you want to run.
  - batch_size: number of images you want to fed into the model at a time.
  - save_weights: if you want save your model's weights, then create a folder with name "save" in your current directory, and set the parameter to 1. The model will save the weights after 100 iterations automaticaly in the save folder. set to 0, if you don't want to save your weights.
  - load_weights: set to 1 if you want to use your previously updated weights values. set to 0 for train the weights from start.
  - data_dir: set the path of your CIFAR-10 dataset.
6. Create the object of the class and provide the dictionary to initialize.
  > classifier = SoftmaxClassifier(dictionary)
7. The following line will automatically load the data from the path provided by you.
  > classifier.loadData()
8. The following line will show you the sample images.
  > classifier.visualize()
9. Now you need to get the train and test data and their labels, respectively.
  > X_train, X_test, y_train, y_test = classifier.getData()
10. Now train your classifier and function will return the loss per iteration.
  > loss = classifier.train(X_train, y_train)
11. The following could be used for the testing of the model by providing test data and labels.
  > classifier.test(X_test, y_test)
