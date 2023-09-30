# NER_bc5cdr

Dataset : BC5CDR (BioCreative V CDR corpus)

Using trainer:  
In code NER_92.40, I reach f1_score = 92.40 in the testing set.  
In code NER_92.02, I reach f1_score = 92.02 in the testing set.   
In code NER_91.18, I reach f1_score = 91.18 in the testing set.  
In code NER_90.78, I reach f1_score = 90.78 in the testing set.  
In code NER_88.96, I reach f1_score = 88.96 in the testing set.  

<img src="https://github.com/frankyang603/NER_bc5cdr/assets/93704660/7f4087b7-fb72-4422-ae21-95a6f9086bca" width="500" height="250">  

In the code I reach the highest score, the picture below shows the f1_score of the validation_set during the training step. 

<img src="https://github.com/frankyang603/NER_bc5cdr/assets/93704660/d9005fbf-f296-4677-a6d7-31d414a799ac" width="500" height="250">  

Without using trainer:  
In code ner_no_trainer_86.7, I reach f1_score = 86.7 in the testing set.  
In code ner_no_trainer_90.9, I reach f1_score = 90.9 in the testing set.   

In the code NER_different_label_testing_1 and NER_different_label_testing_2 , I test the score difference between two differnt testing label.
In the experiment above, I get the score by using adjust_labels. 
During the process, for example, "student" might be tokenize to "stu" "dent", and if "student" is labels by "1", then I will let the token "stu" labels to "1",and "dent" labels to "1" too.
1 

