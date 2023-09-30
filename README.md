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

During the process, for example, "student" might be tokenize to "stu" "dent", and if "student" is labels by "1", then I will let the token "stu" labels to "1",and "dent" labels to "1" too.  

In the experiment above, I get the score by using adjust_labels, in more detail, if "stu" is predicted by model "1" and "dent" also predicted "1", it will count two correct , however, in the test set "student" is one data, so if model predict "1" , it only counts one correct , Go further , if "stu" is predicted label "2" and "dent" is predicted to "1" , it might cannot corectly predicted the label of "student". 

I want to check if there exist a big distance between two differnt scoreing method, I let the predict "student" by useing the maximum occurence in it's split label, for example , if one word is tokenize into three token ,and the three token is predicted by "1","1","2", then the origin word will be prediction be "1".  

I do the experiment using two different model, in the first model, it has subtle different bewteen 91.84 and 91.72 , in the second model, it has moresubtle different bewteen 89.46 and 89.43, 
in this two case, same as what I thought, the score has subtle drop. 
