# To train the model
## Add L2 Directory with the data
Please download the directory (of the exercise). Call it L2.

## Run SegmentationTrain jupyter notebook.
Notice that the model loads pretrained weights from the Londons dataset of dogs/cats segmentation using U-Net.

# To compute the results
run ApplyModelAndGenerateResults jupyter notebook.
The final output of this notebook is:

```BASH
+++++++++++++++++++++++++++++++++++++++++++++++++++++
************* mean Iris parameters ******************
Mean X center - error = 0.56 , Mean Y center error = 0.44
% Mean X radius - error = 66.82 , % Mean Y radius error = 8.16
Mean angle error = 0.76
Mean IoU =  0.8502836294236833
+++++++++++++++++++++++++++++++++++++++++++++++++++++
************* mean Pupil parameters *****************
Mean X center - error = 5.02 , Mean Y center error = 3.13
% Mean X radius - error = 46.7 , % Mean Y radius error = 21.4
Mean angle error = 12.72
Mean IoU =  0.9512815344309031
```
