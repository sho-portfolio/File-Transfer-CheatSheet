# File-Transfer-CheatSheet
How to transfer files between Google-Storage-Buckets, Local-Machine, Google-VM/Google-Compute-Engine and GitHub

| Ref | From          | To                     | Command
| --- | ------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------- 
| A1  | Internet      | Local Machine          | wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt    
| B1  | Github        | Local Machine          | (A1)                                                                                                               
| B2  | Github        | Google Storage Bucket  | (A1) [then] gsutil cp downloads/dataTest.txt gs://stack-overflow-huge                                            
| B3  | Github        | Google Virtual Machine | (A1) [or] git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git                    
| C1  | Local Machine | Githib                 | tbd
| C2  | Local Machine | Google Storage Bucket  | (A1) [then] gsutil cp downloads/dataTest.txt gs://stack-overflow-huge
| C3  | Local Machine | Google Virtual Machine | (A1) [or] git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git
