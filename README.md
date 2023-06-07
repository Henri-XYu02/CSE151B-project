# CSE151B-project

We have opened a Piazza post to the TAs about this before(Sophia Sun should have replied to us). Though we have a best public score of 563.27999, this is done by utilizing online models with a partial polyline feature that doesn't originally exist in public_test.csv(same for a kaggle submission with a score of 673.58312). We are going to submit predictions with score of 679.87822 in the end.

For the kaggle submission with score of 679.87822:

Unfortunately, though we saved our model states on datahub, they were overwritten by tuning hyperparameters and rerunning. Since we have multiple dropouts in our deep learning model as well(that creates lots of stochasticity), we didn't get a better kaggle score by rerunning. We are unable to retrieve our previous(best) model states on datahub. (We didn't intentionally save the submission-related model states, but we saved the model state for each epoch during training, which gets overwritten for the next training)

To partially prove that we got what we submitted:
There is a print statement that prints the first 50 lines of prediction, which should be the same with the first 50 rows of Embedding_MLP_moreunit_89.csv, as well as the kaggle submission file with a public score of 679.87822.

Our main model is Embedding_MLP_model.ipynb