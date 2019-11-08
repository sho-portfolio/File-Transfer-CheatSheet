# File-Transfer-CheatSheet
How to transfer files between Google-Storage-Buckets, Local-Machine, Google-VM/Google-Compute-Engine and GitHub

| From                   | To                     | Command
| ---------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------- 
| Internet               | Local Machine          | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt```    
| Github                 | Local Machine          | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt``` <br/> [or] ```git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git```                                                                                                              
| Github                 | Google Storage Bucket  | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt``` <br/>[then] ```gsutil cp downloads/dataTest.txt gs://stack-overflow-huge```                                            
| Github                 | Google Virtual Machine | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt``` <br/>[or] ```git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git```                    
| Local Machine          | Githib                 | tbd
| Local Machine          | Google Storage Bucket  | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt``` <br/>[then] ```gsutil cp downloads/dataTest.txt gs://stack-overflow-huge```
| Local Machine          | Google Virtual Machine | ```wget https://raw.githubusercontent.com/sho-portfolio/MachineLearning-MultiClassClassifier/master/dataTest.txt``` <br/>[or] ```git clone https://github.com/sho-portfolio/MachineLearning-MultiClassClassifier.git```
| Google Storage Bucket  | Local Machine          | ```gsutil cp gs://bucket_20191022_machine-learning-data/testDataHsbc.txt downloads/dataTestA.txt``` 
| Google Storage Bucket  | Google Virtual Machine | ```gsutil cp gs://my-awesome-bucket/file1.png foldername/file1.png```
| Google Virtual Machine | Github                 | tbd
| Google Virtual Machine | Local Machine          | ```gsutil cp downloads/dataTest.txt gs://stack-overflow-huge``` <br/> [then] ```gsutil cp gs://bucket_20191022_machine-learning-data/testDataHsbc.txt downloads/dataTestA.txt```
| Google Virtual Machine | Google Storage Bucket  | ```gcloud compute scp dataTest.txt instance-sho:~```


# Notes
* Mac OS does not come with wget installed.  To install wget run the following command in Terminal: ```brew install wget```
* To install git on a machine (local or virtual) run the following command in terminal: ```sudo apt update
sudo apt install git```
