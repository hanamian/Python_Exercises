# Dictionary
---
### No. 1
Create dictionary
```python
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# From string in countries and capitals, create dictionary europe
europe = { 'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

print(europe)
```
Result:
```
{'norway': 'oslo', 'france': 'paris', 'germany': 'berlin', 'spain': 'madrid'}
```
---
### No. 2
Access keys and specific values of dictionary
```python
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Print out the keys in europe
print(europe.keys())

# Print out value that belongs to key 'norway'
print(europe['norway'])
```
Result:
```
dict_keys(['norway', 'france', 'germany', 'spain'])
oslo
```
---
### No. 3
Add elements in dictionary
```python
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Add italy:rome and poland:warsaw 
europe['italy']='rome'
europe['poland']='warsaw'

print(europe)
print(europe['italy'])
```
Result:
```
{'france': 'paris', 'spain': 'madrid', 'norway': 'oslo', 'poland': 'warsaw', 'italy': 'rome', 'germany': 'berlin'}
rome
```
---
### No. 4
Add elements in dictionary
```python
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Add italy:rome and poland:warsaw 
europe['italy']='rome'
europe['poland']='warsaw'

print(europe)
print('italy' in europe)
print(europe['italy'])
```
Result:
```
{'france': 'paris', 'spain': 'madrid', 'norway': 'oslo', 'poland': 'warsaw', 'italy': 'rome', 'germany': 'berlin'}
True
rome
```
---
### No. 5
Update and delete elements in dictionary
```python
europe = {'spain':'madrid', 'france':'paris', 'germany':'bonn',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw',
          'australia':'vienna' }
          
# Update capital of germany:berlin
europe['germany']='berlin'

# Remove australia
del(europe['australia'])

# Print europe
print(europe)
```
Result:
```
{'france': 'paris', 'spain': 'madrid', 'norway': 'oslo', 'poland': 'warsaw', 'italy': 'rome', 'germany': 'berlin'}
```
---
### No. 6
Dictionary of Dictionaries
```python
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }
          
# Print out the capital of France
print(europe['france']['capital'])

# Create sub-dictionary data
data = {'capital':'rome','population':59.83}
print(data)

# Add data to europe under key 'italy'
europe['italy']='data'

# Print europe
print(europe)
```
Result:
```
paris
{'population': 59.83, 'capital': 'rome'}
{'norway': {'population': 5.084, 'capital': 'oslo'}, 'france': {'population': 66.03, 'capital': 'paris'}, 'italy': {'population': 59.83, 'capital': 'rome'}, 'germany': {'population': 80.62, 'capital': 'berlin'}, 'spain': {'population': 46.77, 'capital': 'madrid'}}
```
