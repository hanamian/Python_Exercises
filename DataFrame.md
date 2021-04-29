# DataFrame
---
## No. 1
**Dictionary to DataFrame**
```python
import pandas as pd

#Pre-defined lists
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

my_dict = {'country':names,
            'drives_right': dr,
            'cars_per_cap': cpc}

cars = pd.DataFrame(my_dict)
print(cars)

```
Result:

![image](https://user-images.githubusercontent.com/49611937/116402372-8f507280-a856-11eb-9bfd-83d15e1a33f7.png)

---
## No. 2
**Changing the Index**
```python
import pandas as pd

# Build cars DataFrame
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

cars_dict = { 'country':names, 'drives_right':dr, 'cars_per_cap':cpc }
cars = pd.DataFrame(cars_dict)
print(cars)

# Definition of row_labels
row_labels = ['US', 'AUS', 'JPN', 'IN', 'RU', 'MOR', 'EG']

# Change cars index with row_labels
cars.index = row_labels

# Print cars again
print(cars)

```
Result:

![image](https://user-images.githubusercontent.com/49611937/116402924-2ae1e300-a857-11eb-8c66-90a5e9330bd4.png)
![image](https://user-images.githubusercontent.com/49611937/116402981-3a612c00-a857-11eb-838d-1c5553d5156d.png)

---
## No. 3
**Dictionary to DataFrame**
```python
import pandas as pd

# Delete index using index_col=0
cars = pd.read_csv('cars.csv', index_col= 0)
print(cars)
```
Result:

Before (with index)

![image](https://user-images.githubusercontent.com/49611937/116404160-924c6280-a858-11eb-8ab1-f59c659df1f0.png)

After (index is deleted)

![image](https://user-images.githubusercontent.com/49611937/116404321-b9a32f80-a858-11eb-8452-371c3d41eec5.png)

---
## No. 4
**Series vs DataFrame**
```python
#Series
series    = cars['country']
dataframe = cars[['country']]
```

---
## No. 5
**Subset Rows**
```python
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out first 3 observations
print(cars[0:3])

# Print out fourth, fifth and sixth observation
print(cars[3:6])
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116406268-adb86d00-a85a-11eb-8c96-17323e1fd089.png)
![image](https://user-images.githubusercontent.com/49611937/116406330-bd37b600-a85a-11eb-9461-fb746f4b6d3f.png)

---
## No. 6
**Subset using loc**
```python
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Japan is series
print(cars.loc['JPN'])

# Australia and Egypt
print(cars.loc[['AUS','EG']])
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116408604-31735900-a85d-11eb-97fb-f12c72d2db09.png)
![image](https://user-images.githubusercontent.com/49611937/116408303-d5a8d000-a85c-11eb-9dea-d1542ec23bb0.png)

---
## No. 7
**Subset using loc**
```python
import pandas as pd

cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right value of Morocco
print(cars.loc['MOR', 'drives_right'])

# Print sub-DataFrame
print(cars.loc[['RU','MOR'], ['country', 'drives_right']])
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116410361-e5c1af00-a85e-11eb-8100-08efdbe2b033.png)
![image](https://user-images.githubusercontent.com/49611937/116410437-fa9e4280-a85e-11eb-9e7c-61c0d6514897.png)

---
## No. 8
**Subset using loc**
```python
import pandas as pd

cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right value of Morocco
print(cars.loc['MOR', 'drives_right'])

# Print sub-DataFrame
print(cars.loc[['RU','MOR'], ['country', 'drives_right']])
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116410361-e5c1af00-a85e-11eb-8100-08efdbe2b033.png)
![image](https://user-images.githubusercontent.com/49611937/116410437-fa9e4280-a85e-11eb-9e7c-61c0d6514897.png)

---
## No. 9
**Double Subsetting**
```python
import pandas as pd

cars = pd.read_csv('cars.csv', index_col = 0)

sel = cars[cars['drives_right']]

# The code above is equal to below codes
#dr = cars['drives_right']
#sel = cars[dr]

# Print sel
print(sel)
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116425274-5e7b3800-a86c-11eb-938e-7e356baf9793.png)

---
## No. 10
**Subsetting again**
Select the cars_per_cap column from cars as a Pandas Series and store it as cpc.
Use cpc in combination with a comparison operator and 500. You want to end up with a boolean Series that's True if the corresponding country has a cars_per_cap of more than 500 and False otherwise. Store this boolean Series as many_cars.
Use many_cars to subset cars, similar to what you did before. Store the result as car_maniac.
Print out car_maniac to see if you got it right.

```python
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Create car_maniac: observations that have a cars_per_cap over 500
cpc = cars['cars_per_cap']
many_cars = cpc > 500

car_maniac = cars[many_cars]

# Print car_maniac
print(car_maniac)
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116496717-e7778b00-a8cf-11eb-8abb-7ab6e9bf2cd4.png)

---
## No. 11
**Subset and using np.logical_and**
```python
import pandas as pd
import numpy as np

cars = pd.read_csv('cars.csv', index_col = 0)

# Create medium: observations with cars_per_cap between 100 and 500
cpc = cars['cars_per_cap']
between = np.logical_and(cpc > 100, cpc < 500)
medium = cars[between]

print(medium)
```
Result:

![image](https://user-images.githubusercontent.com/49611937/116497076-b77cb780-a8d0-11eb-97de-fe911d1a1995.png)
