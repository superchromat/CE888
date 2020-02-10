# Lab 5 - Recommender systems

## Resources

* rec_latent.ipynb contains the code shown in the lecture for a recommender system based on latent features
* rec_features.ipynb contains the code from the lecture for a hybrid recommender system
* item_features, user_features and user_ratings contain the data
* helper_function.ipynb contains a function that will help you with the exercises below, together with an example of use


## Lab Exercises

- [ ] Create a folder called lab5
- [ ] Create a notebook called *my_recommender.ipynb*

In the Ipython notebook you created
- [ ] Load the data from ``jester-data-1.csv''
    * The data is from [http://eigentaste.berkeley.edu/dataset/](http://eigentaste.berkeley.edu/dataset/) and it contains the ratings of 101 jokes from 24,983 users
	* You can find the jokes in the website [http://eigentaste.berkeley.edu/dataset/jester_dataset_1_joke_texts.zip](http://eigentaste.berkeley.edu/dataset/jester_dataset_1_joke_texts.zip)
	* Check the dataset description to understand why we replace random cells as 99!
- [ ] Using the helper function provided in the helper_function notebook (or create your own), label 20% of the dataset cells as 99. Keep the the actual values of the cells so you can use them at the end.
- [ ] Use half of the values above as **test set** (i.e., don't look at them/use them until the end)
- [ ] The other half is your **validation set**. Keep the the actual values of the cells so you can use them later. 
- [ ] Use latent factor modeling to infer the hidden ratings of the users (they are labeled as "99" in the dataset) on the training set
- [ ] Calculate the performance of the algorithm on the validation dataset
- [ ] Change hyper-parameters (i.e., learning rate, number of iterations of SVD, number of latent factors, etc.) as needed to get good results **using only your training and validation sets**
- [ ] Once you're happy, report the MSE on the **test dataset**
- [ ] (If you have time) Use pandas to find the best- and the worst-rated jokes
- [ ] Make sure you save your changes in Github!

Don't worry if I don't have time to check your work during the lab. As long as it's on GitHub, it will be marked!






