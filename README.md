# File-Transfer-CheatSheet
How to transfer files between Google-Storage-Buckets, Local-Machine, Google-VM/Google-Compute-Engine and GitHub

| Ref | From                   | To                     | Command
| --- | ---------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------- 
| A1  | Internet               | Local Machine          | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt```    
| B1  | Github                 | Local Machine          | (A1)                                                                                                               
| B2  | Github                 | Google Storage Bucket  | (A1) <br/>[then] gsutil cp downloads/dataTest.txt gs://stack-overflow-huge                                            
| B3  | Github                 | Google Virtual Machine | (A1) <br/>[or] git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git                    
| C1  | Local Machine          | Githib                 | tbd
| C2  | Local Machine          | Google Storage Bucket  | (A1) <br/>[then] gsutil cp downloads/dataTest.txt gs://stack-overflow-huge
| C3  | Local Machine          | Google Virtual Machine | (A1) <br/>[or] git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git
| D1  | Google Storage Bucket  | Local Machine          | gsutil cp gs://bucket_20191022_machine-learning-data/testDataHsbc.txt downloads/dataTestA.txt 
| D2  | Google Storage Bucket  | Google Virtual Machine | gsutil cp gs://my-awesome-bucket/file1.png foldername/file1.png
| E1  | Google Virtual Machine | Github                 | tbd
| E2  | Google Virtual Machine | Local Machine          | gsutil cp downloads/dataTest.txt gs://stack-overflow-huge <br/> [then] (D1)
| E3  | Google Virtual Machine | Google Storage Bucket  | gcloud compute scp dataTest.txt instance-sho:~


# Notes
* Mac OS does not come with wget installed.  To install wget run the following command in Terminal: ```brew install wget```
