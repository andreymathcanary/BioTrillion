# To train the model
In order to train the model
* Add Directory with the data to the root directory. Call it `L2`.
* Run SegmentationTrain jupyter notebook.

Notice that the model loads pretrained weights from the Londons dataset of dogs/cats segmentation using U-Net.

# To compute the results
run ApplyModelAndGenerateResults jupyter notebook. This notebook uses the model trined earlier. The final, trained model is saved for convenience ( no need to train).
The most important output of this notebook is:

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
# Auxilliary data
* The file `Ellipse.pdf` contains all the necessary formulas for fitting Ellipse to a set of (x,y) points. Linear regression-wise.
* The floder `Articles` contains a few articles that were found and helped to understand more precisely the problem.

# What could be done better:
1. Clean data, by creating a pre-processor, which will erase rreflection from the Pupil (at least).
2. Ellipse fitting can be done robust: points that are far from the fitted ellipse can be ignored. For this one can use weighted linear regression. Something
   like that: https://reference.wolfram.com/applications/eda/RobustFitting.html
3. Augment data to make it more precise (noise, other real distortions).
