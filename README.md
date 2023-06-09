## CSE151B-project

# Apology:

We have opened a Piazza post to the TAs about this before(TA Sophia Sun should have replied to us). Though we have a best public score of 563.27999, this is done by utilizing online models with a partial polyline feature that doesn't originally exist in public_test.csv(same for a kaggle submission with a score of 673.58312). We are going to submit predictions with score of 679.87822 in the end.


## Instruction on how to load the model

Unfortunately, for the LSTM model, though we saved our model states, everytime we reload the model states, the predict output is different. (We really don't know why). We used 

```
PATH = 'xxx.pth'
torch.save('xxx.pth')
model.load_state_dict(torch.load(PATH))
```

However, when we re-initialize the model and load the saved model states, everytime the prediction output produced is different.(but the scores are similar around 681-688).


For the MLP model, we have rerun the model to tune parameters (with worse score) and the model states are overwritten, and we are unable to retrieve them. Therefore, for the MLP, we have trained the model again and picked the model state at the same epoch. The output produced will be different, but you should get some idea of what we are working.

We have provided a file Load Model.ipynb, by running it you should get a prediction file(though different from what we submitted).

## To partially prove we got what we submitted:

In Code folder, in Embedding_MLP_model.ipynb and Embedding_MLP_LSTM_model.ipynb, there is a print statement that prints the first 50 lines or the entire prediction, which should be the same with the first 50 rows of Embedding_MLP_moreunit_89.csv and Embedding_MLP_188_retrain.csv we submitted on kaggle, which have public scores of 679.87822 and 681.97093.