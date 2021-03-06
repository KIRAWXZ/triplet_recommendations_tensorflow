# triplet_recommendations_tensorflow
A simple implementation of learning to rank on dataset lightFM. Actually, there is a keras version here: https://github.com/maciejkula/triplet_recommendations_keras. But some APIs are not compatible with keras of current version (e.g. merge_mode='join'). 

The following performance is measure with ROC AOC SCORE

Using TensorFlow backend.

validation roc_auc_score:0.500467073101
	
 0/100, 778/779. loss:0.587008476257	validation roc_auc_score:0.702677984692
 
 1/100, 778/779. loss:1.462861061166    validation roc_auc_score:0.80255242201
 
 2/100, 778/779. loss:0.2513701319694   validation roc_auc_score:0.854715083016
 
 3/100, 778/779. loss:0.1178833693277   validation roc_auc_score:0.85643688405
 
 4/100, 778/779. loss:0.1781855970628   validation roc_auc_score:0.864170124402
 
 5/100, 778/779. loss:0.1883448362353   validation roc_auc_score:0.865154335231
 
 6/100, 778/779. loss:0.1131904348738   validation roc_auc_score:0.868120570471
 
 7/100, 778/779. loss:0.1563295722013   validation roc_auc_score:0.865612767672
 
 8/100, 778/779. loss:0.0875216051936	validation roc_auc_score:0.866878816628
 
 9/100, 778/779. loss:0.3333355486397   validation roc_auc_score:0.864985669625
 
 10/100, 778/779. loss:0.09641548246158 validation roc_auc_score:0.864135758014
 
 11/100, 778/779. loss:0.3253963291651  validation roc_auc_score:0.864988380759
 
 12/100, 778/779. loss:0.1283061057331  validation roc_auc_score:0.86462891655
 
 13/100, 778/779. loss:0.37685054540637 validation roc_auc_score:0.861607682699
 
 14/100, 778/779. loss:0.0506101064384	validation roc_auc_score:0.863723406701
 
 15/100, 778/779. loss:0.00917862355709	validation roc_auc_score:0.862988460131
 
 16/100, 778/779. loss:0.19491487741598 validation roc_auc_score:0.862756136977
 
 17/100, 778/779. loss:0.06320969760426 validation roc_auc_score:0.864832942235
 
 18/100, 778/779. loss:0.12448710203258 validation roc_auc_score:0.863374504944

Significantly outperform the performance with 'bpr' loss in the official site here: http://lyst.github.io/lightfm/docs/examples/movielens_implicit.html. 

In my_triplet_feats.py, we consider genre features of the movies to improve the performance. Actually we are able to improve the roc auc socre to 89%, and the results are listed as follows:

 [!] Load parameters success!!!
 
	validation roc_auc_score:0.890481743624
	
 0/100, 778/779. loss:0.05905286222782  validation roc_auc_score:0.892570015951
 
 1/100, 778/779. loss:0.16974817216418  validation roc_auc_score:0.890205940637
 
 2/100, 778/779. loss:0.10492754727665  validation roc_auc_score:0.887460079443
 
 3/100, 778/779. loss:0.04295096173887  validation roc_auc_score:0.892610324532
 
 4/100, 778/779. loss:0.14503671228986  validation roc_auc_score:0.890672407806
 
 5/100, 778/779. loss:0.02661069668831  validation roc_auc_score:0.885403041236
 
 6/100, 778/779. loss:0.16777089238218  validation roc_auc_score:0.885388838798
 
 7/100, 778/779. loss:0.14799317717676  validation roc_auc_score:0.893298911301
 
 8/100, 778/779. loss:0.06235758960257  validation roc_auc_score:0.89143136914
 
 9/100, 778/779. loss:0.21639181673527  validation roc_auc_score:0.891467325608
