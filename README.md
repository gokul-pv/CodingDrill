# Codind Drill
A step by step approch to improve the model

The aim is to do the following with MNIST data.

 1. target is to achieve 99.4% **(consistently shown in your last few epochs, and not a one-time achievement)**
 2. Less than or equal to 15 Epochs
 3. Less than 10000 Parameters


**Code 1 - Setup**

[Click here](./Code1_Basic.ipynb)

Target

1. Get the set-up right with a light weight skeleton
2. Set Transforms
3. Set Data Loader
4. Set Basic Working Code
5. Set Basic Training  & Test Loop


Results
1.   Parameters - 7,864
2.   Best training accuracy- 98.47%
3.   Best test accuracy - 98.53%


Analysis
1. Good model!
2. No over-fitting, model is capable if pushed further


**Code 2 - BATCH NORMALIZATION and REGULARIZATION**

[Click here](./Code2_BN_Drop.ipynb)

Target

1. Add Batch-norm to increase model efficiency.
2. Add Regularization, Dropout


Results
 1.   Parameters - 8,016
2.   Best training accuracy- 98.14%
3.   Best test accuracy - 99.22%


Analysis
1. Model is still under-fitting
2. But we're not seeing 99.4. We can further improve it. 
3. The model is not over-fitting at all. 
4. Seeing image samples, we can see that we can add slight rotation. 


**Code 3 - Image Augmentation**

[Click here](./Code3_ImageAugmentation.ipynb)

Target

1.  Add rotation, 5-7 degrees should be sufficient.
2.  Reduce dropout to 0.05

Results

1.  Parameters - 8,016
2.  Best training accuracy - 98.53%
3.  Best test accuracy - 99.31%

Analysis

1.  The model is still under-fitting. This is fine, as we know we have made our train data harder. 2.The test accuracy has improved a little bit, which means our test data had few images which had transformation difference w.r.t. train dataset
2.  Add LR Scheduler may help in getting 99.4 faster


**Code 4 - LR Scheduler**

[Click here](./Code4_LRScheduler.ipynb)

Target

1.  Add LR Scheduler

Results

1.  Parameters - 8,016
2.  Best training accuracy - 99.06%
3.  Best test accuracy - 99.44% (13th epoch)

Analysis

1.  Reached the desired accuracy of 99.4 at 11th epoch.
2.  LR Scheduler did help in getting to 99.4 or faster.
3.  Finding a good LR schedule is hard. Made it effective by reducing LR by 10th after the 10th epoch.
