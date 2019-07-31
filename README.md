#Dataloader(revised)

##### https://medium.com/datadriveninvestor/how-to-custom-datasets-and-dataloaders-with-pytorch-e27f9e2a9009

Pytorch 장점
------------

I can build my custom data pipeline by subclassing the dataset class ,allowing me to load and preprocess my data easily

### Dataset Class

"you can have data without information, but you cannot have information without data"

#### Data pipeline

```
- Data acquisition - raw data
- Data preprocessing - data mining technique
    raw data -> understandable format
    (주의 사항: real data -> incomplete,inconsistent,lack)
- Reading data - feed batches of data of size n.
```

#### Dataset subclass

```
__init__: the constructor
__len__: return length of Dataset
__getitem__: takes the path from constructor reads files and preprocesses it
```

### Visualizing a sample from dataset

Skip

### Creating custom transforms\*\*

Once making dataset, transformation of data is needed. because by transforming we can have more information in single image. taking one image and creating different variations of the same image is the goal of transforming dataset. it also can prevent overfitting, by giving different variations of the same data(generalized understanding of the data).

### Dataloader

##### 1.Batching the data

##### 2.Shuffling the data

##### 3.Load the data in parallel using multiprocessing workers
