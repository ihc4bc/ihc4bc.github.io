---
layout: default
---




# Before Attempting to Download ....

Please read this section before attempting to download the dataset.

The dataset contains near 2 TB of images which are uploaded to [pcloud](https://www.pcloud.com/), in the following address:


https://filedn.com/laHPyhQ5wAHBUyNr64yhV0Q/IHC4BC_Dataset/


Pcloud has a limited download quota to be deducted from either the uploader's or the downloader's limit.
These limits are reset monthly for each user.
So if you failed to download the images due to the uploader's download quota being exceeded, you can create a pcloud free account with a basic download quota.
If that basic quota didn't suffice, you can buy a paid pcloud account.

The labels are maintained in the following repository, and are a couple of gigabytes in total.

https://gitlab.com/ihc4bc-dataset/labels/-/tree/main/  


# About

The below figure illustrates how the patch-pairs in the dataset are obtained.

![overview of streamcollector functionality](stages_screenshot.png)

When registering WSI pairs we learned that there is no rigid registration that can perfectly register two WISs. Therefore, we
firstly annotated region-pairs from the two WSIs (the step labeled
as ”extract regions” in the above figure). Afterwards, we registered each region-pair manually
(in the above figure this step is labeled as ”register regions”). Afterwards, we traversed
each region-pair with a stride of 1500 and extracted patch-pairs. The final
result of this step is a set of patch-pairs each of which are 3000 by 3000 (the
pairs in the right side of the figure).


Roughtly ~150K patch-pairs were extracted from ~240 WIS pairs. Consequently, DAB analysis was done on the H-DAB images (except for Her2/nue).
These ~150K pair were exhaustively inspected and around 60K pairs were discarded due to unreliablity of DAB analysis results.
Finally ~90K patch-pairs made it to the IHC4BC dataset.
For more details please refer to our paper.

# Citation 
If you use this dataset in your research, please cite the following paper:

TODOTODO

# Issues
Please report issues to the following address, and help us improve the dataset

ah8 [at] ualberta [dot] ca

# Acknowledgements

TODO: compute-canada
TODO: other 
 
