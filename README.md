# Reading-blank-cells-from-csv-file-in-python
To read a csv file Using strip function where blank cells and rows would be read using this function help to read column and rows without any errors in python 
import pandas as pd

data = pd.read_csv("D:/python/sheet.csv")

# remove leading/trailing whitespaces from all string columns
data = data.apply(lambda x: x.str.strip() if x.dtype == "object" else x)

# print the dataframe in a proper line
print(data.to_string(index=False))
