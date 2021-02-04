# Lab 4 - Recommender systems

## Resources

* rec_latent.ipynb contains the code shown in the lecture for a recommender system based on latent features
* rec_features.ipynb contains the code from the lecture for a hybrid recommender system
* item_features.csv, user_features.csv and user_ratings.csv contain the data needed for this lab
* helper_function.ipynb contains a function that will help you with the exercises below, together with an example of use


## Lab Exercises

- [ ] Create a folder called lab4
- [ ] Create a notebook called *my_recommender.ipynb*

In the Jupyter notebook you created
- [ ] Load the data from ``jester-data-1.csv'',
    * The data is from [http://eigentaste.berkeley.edu/dataset/](http://eigentaste.berkeley.edu/dataset/) and it contains the ratings of 100 jokes from 24,983 users
	* You can find the jokes in the website [http://eigentaste.berkeley.edu/dataset/jester_dataset_1_joke_texts.zip](http://eigentaste.berkeley.edu/dataset/jester_dataset_1_joke_texts.zip)
	* Check the dataset description to figure out which value you should replace with NaNs. This is the **test set** (the cells for which we don't have a rating)
	* To replace values when you load, you can find help here: [https://stackoverflow.com/questions/29247712/how-to-replace-a-value-in-pandas-with-nan](https://stackoverflow.com/questions/29247712/how-to-replace-a-value-in-pandas-with-nan)
	* There's a column you need to remove because it doesn't contain ratings. Check the description of the dataset and figure out which one. Then drop it.
- [ ] Use pandas to find the best- and the worst-rated jokes
- [ ] Modify and use the helper function provided in the helper_function notebook (or create your own) to label 10% of the dataset cells that are not NaNs as 99. This is your **validation set**. Keep the the actual values of the cells so you can use them later (as done in the example of the helper_function notebook). 
- [ ] Use latent factor modeling (with 4 latent factors) to infer the hidden ratings of the users (they are labeled as "99" in the dataset) on the training set. You will have to modify at least one line in the provided sgd() function for this.
	* sgd with 300000 iterations will take a long time to run: you can decrease this number.
- [ ] Calculate the performance (e.g., MSE) of the algorithm on the **validation dataset**
- [ ] Repeat the two points above changing hyper-parameters (i.e., learning rate, number of iterations of SVD, number of latent factors, etc.) as needed to get good results (you can create multiple validation sets if you want, and run a bootstrap!)
- [ ] Once you're happy, make predictions for the **test dataset**
- [ ] Make sure you save your changes in Github!

