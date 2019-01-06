PyTorch implementation of GTSRB Classification Challenge

<h2>Introduction</h2>

The German Traffic Sign Recognition Benchmark (GTSRB) is a multi-class, single-image

This project was part of the Kaggle InClass Challenge held during the Computer Vision MSCS degree course at NYU. My approach got the highest test accuracy of 99.809% on the Private Leaderboard and 99.746% on the Public Leaderboard.  


<h2>Methods used</h2>

CNN and Spatial transformer network: CNN with 3 layers, 2 fully connected layers and 1 spatial transformer network layer with two convolutional layers and one fully connected layer (CNN feature maps: 3 -> 100 -> 150 -> 250 -> 350, filter size: [5, 3 ,3], spatial transformer network feature

Data augmentation: Both training time and test time data augmentation proved to be

<h2>Data preparation</h2>

Download data from here.

<h2>Training</h2>

To train, use the command:
```bash
python code/main.py --data data --epochs 40
```


<h2>Evaluation</h2>
To generate the file of predictions on the test set, use the command:

```bash
```


Test accuracy score reported above is obtained from a model trained on combination of training + validation sets. 

Note: due to the variable nature of the random torchvision transforms such as jittering etc. that are used during test time augmentation, a tiny difference in accuracy will be observed each time the predictions file is generated. I got a public score of 99.746%, 99.714%, 99.730% and 99.699% using the same model. The best private score came from the file with the best public score.

