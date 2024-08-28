## Developed By: VENKATA BHARADWAJ.B
## Register No: 212222240020
##  Date: 

# Ex.No: 01A  PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (National stock exchange)


# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Use the Date coloumn for tracking the index.
4. Plot the data accordingly which can be altered monthly, or yearly.
5. Display the graph.



# PROGRAM:

 
```python
import pandas as pd
import matplotlib.pyplot as plt

file_path = '1ECO-USD.csv'
data = pd.read_csv(file_path)

print(data.head)

data['Date']=pd.to_datetime(data['timestamp'])

data.set_index('timestamp',inplace=True)
plt.plot(data.index,data['open'],label='temp')
plt.title("Daily Minimum Trades")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Trades")
plt.grid(True)
plt.legend()
plt.show()

```



 





# OUTPUT:
![Screenshot 2024-08-23 220211](https://github.com/user-attachments/assets/8a76a953-5c05-48a5-b7ff-6f1e504b7b9b)
![Screenshot 2024-08-23 220227](https://github.com/user-attachments/assets/4be2e8e9-6c72-42cc-8d65-96f6e39e380b)

![Screenshot 2024-08-23 220242](https://github.com/user-attachments/assets/20dcec82-0522-4f7a-a571-e353658aefcd)







# RESULT:
Thus the python code has created  for plotting the time series of given data successfully.
