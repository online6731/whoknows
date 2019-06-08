# Data Manager
Data manager is a python code which implements the functionally for dataset pipeline. Dataset pipeline is the production line of a dataset. Each dataset gets created at first state and becomes complete at last state by successfully passing the required operations.


# How to deploy?
Setting up is simple, just follow these steps.


### Python :
1. Install python and pip and git:
`apt install git python3 python3-pip`

2. Clone the repository:
`git clone ...`

3. Go to repository folder:
`cd guessit-template-manager`

4. Install dependencies:
 `pip install -r requirements.txt`

5. Start server:
 `python3 app.py`


###  Docker :
1. Clone the repository:
`git clone ...`

2. Go to repository folder:
`cd guessit-template-manager`

3. Build image from dockerfile:
`docker build -t guessit-template-manager`

4. Run docker image:
`docker run -it guessit-template-manager`

# Main concepts
These are the main concepts of Data Manager

## Dataset
Dataset is a collection of data with the same type

## Dataset Template(Dataset Catalog)
Dataset Template is the specification of a dataset and it's fields.

## Dataset Pipeline

## Main Functions
Main functions of data manager are the following:

### Find new data:
> Finds id of all available data in resources

### Update:
> Updates every field of all data in dataset

### Merge:
> Finds duplicated data from different resources in dataset and merge them together

### Schema test:
> Check the schema of all data in dataset

###  Manual test:
> Human testers check and verify the accuracy and ... of data in dataset

### Usage tagging:
> Complete the tag field of dataset


## State
State shows the situation of dataset in pipeline. These are the following states in the dataset pipeline:

### 1. Out dated
> Dataset may contain expired data

### 2. Duplicated
> Dataset may contain duplicated data

###  3. Stable
> In this state all data is collected and prepared to be tested

### 4. Ready
> Dataset is now ready for manual test and verification

### 5. Verified
> Dataset is now completed and tested and ready for tagging

### 6. In use
> Dataset is done and can be used

# How to use?
Data manager is available via API and CLI

### API
[Read more ...]( )


### CLI
[Read more ...]( )



# Contributers
- Mohammad Parsian
- Danial Keimasi
- Moein Samadi
