# Include Panda library 
1. import panda as pd
2. import numpy as np => This will also be used further 

# Create a panda series 
1. s = pd.Series([1,2,3,4,5,6,np.nan,8,9,10]) => np.nan returns null value 

# Create a date array 
1. d = pd.date_range('20210301', periods = 10) => Create an array having the date from 2021-03-01 and 9 more dates just after these 

# Create a Data frame 
1. d = pd.date_range('20210301', periods = 10)
2. df = pd.DataFrame(np.random.randn(10,4), index = d, columns = ['A', 'B', 'C', 'D'])

---------------------------------------------------

# Read a .csv file 
1. dataset = pd.read_csv('filename.csv')

# Display .csv in tabular form 
1. dataset = pd.read_csv('filename.csv')
2. dataset => print whole data
3. dataset.head(5) => print upto 5 rows only 

# Basic commands 
1. dataset = pd.read_csv('filename.csv')
2. type(dataset) => return value = dataframes 

# Check for null values 
1. dataset = pd.read_csv('filename.csv')
2. dataset.Age.isnull() => print the age column having true and false values only , true when age in that box is null in original dataset with indices

# Access a particular coloum 
1. dataset = pd.read_csv('filename.csv')
2. dataset["Age"] or dataset.Age => print the age coloumn with indices 

# Access data using various ways 
1. dataset = pd.read_csv('filename.csv')
2. dataset.loc[0] => return the data in first row or 0th indexed row with the labels/coloumn head
3. dataset.iloc[:,0] => returns the data in first coloumn of all the rows with indices 
4. dataset[["Country", "Age"]] => returns the table having rows corresponding to these head coloumns only 


# Change the index of our data/ make some other coloumn as our indexing coloumn 
1. dataset_random = pd.read_csv('filename.csv', index_col = "Country") => In the dataset random, the Country column in our csv file has now become the index for rest of data 

So we can now do -> 
2. dataset_random.loc("Spain") => returns the table rows having country as spain 

# Find mean of values of a particular column 
1. dataset = pd.read_csv('filename.csv')
2. dataset.Salary.mean()

------------------------------------------------------------

# Handling Missing values 

1. Replace the null values in particular coloumn with the average value of rest of values in that column 
2. X = pd.read_csv('filename.csv')
3. X.Salary[X.Salary.isnull()] = X.Salary.mean() => replace all the null values in Salary column with avg value 


# Note - panda make shallow copy if we do dataset1 = dataset2, so all changes done in dataset will be reflected in dataset 1, so better to make deep copy 
1. X1 = X.copy()


# Label Encoder
=> As our ML model can only understand 0's and 1's, that's why the strings in our dataset needs to be converted into int , one such way is to assign everystring a particular integer 

X = pd.read_csv('filename.csv')
1. from sklearn.preprocessing import LabelEncoder 
2. enc = LabelEncoder()
3. enc.fit(X["Country"])
4. X["Country"] = enc.transform(X["Country"])
5. print(X)









