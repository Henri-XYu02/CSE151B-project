## CSE151B-project

# Apology:

We have opened a Piazza post to the TAs about this before(TA Sophia Sun should have replied to us). Though we have a best public score of 563.27999, this is done by utilizing online models with a partial polyline feature that doesn't originally exist in public_test.csv. We are going to submit predictions with score of 663 and 679.87822 in the end.


## Instruction on how to load the model

We just realized on Friday 6/9, just before the submission deadline that we didn't write 

```
model.eval()
```

in prediction, this makes our previous prediction submissions using dropouts. Right now our prediction submissions have been fully used up: this means that our uploaded submissions were irreproducible. Though I have fixed the Load Model.ipynb file for you to load the model and check submission, the prediction you got should be different from our submission and should be better than our submission as it has turned off dropout. 

We apologize for that, but it is also frustrating for us because we realized that we could have gotten far better score without this foolish mistake.

We have provided a file Load Model.ipynb, by running it you should get a prediction file(though different from what we submitted).