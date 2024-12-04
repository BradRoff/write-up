
<h1 align = "center">Updating a file through a Python algorithm</h1>

<h3  align = "center"> Introduction</h3>

&emsp;In this Scenario I'm a security profesional working at a health care company. I'm reguraly requaried to update a file that determines which employees can access restricted content determined by their IP address. Giving an allow_list and remove_list, in this project we will create a Python Algorithm to check if the `pythonallow_list` contains any IP addresses on the `pythonremove_list`. If they do contain them, the algorithm will automaticly remove them.

<h3  align = "center">Opening the file that contains the allow list</h3>
&emsp;
For the first part of the algorithm, I opened the `pythonallow_list.txt` file. First, I assigned the text file to `pythoninport_list`.

```python
#Assigning allow_list.txt file to import_list for further use
import_file = allow_list.txt
```
&emsp;
Then I used a with statement to `open` the file:

```python
#Opining imported list of allowed IPs useing with open, assigning the read "r" result to file
with open(inport_file, "r") as file:
```
<h3  align = "center">Reading the file's contents</h3>
&emsp;
Next, to read the results I take the file from the privious step and convert it to a string using the `python.read` command. 
This string now stored in `pythonip_addresses` can now be used latter for orginizing and extracting data in the python algorithm.

```python
with open(inport_file,"r") as file:
    ip_address = file.read()
``` 

<h3  align = "center">Converting the string into a list</h3>

&emsp;To remove individual IPs from this string, I need the IPs to be in a list format. Using the `pythonsplit()` method, I will convert the `pythonip_addresses` into a list. In this case, spliting the list by white spaces and assigning the result back to `pythonip_addresses`.

```python
#Using '.split()' to convert IP string to list for ideration
ip_addresses = ip_addresses.split()
```

<h3  align = "center">Iterating through the remove list</h3>
&emsp; By inplementing a `pythonfor` loop, the iteration will repeat for each element in a sequence.

```python
#Iterating through each element using a for loop in remove_list
for element in remove_list:
```

<h3  align = "center">Removing IPs that are on the remove list</h3>

&emsp;The goal of this algorithm requires removing any IP from the allow list (`pythonip_addresses`), that are also contained in the `pythonremove_list`. To achive this I used the following code, note: IPs in the allow list do not repeat.

```python
for element in ip_addresses:
# Build conditional statement
  # If current element is in `remove_list`,
    
    if element in ip_addresses:
    
        # remove that element from `ip_addresses`

        ip_addresses.remove(element)
'''

&emsp;
In this the loop above, the code checks if each IP in remove list matches any ID in ip_addresses. If so, that ID is removed using `pythonip_addresses.remove(element)`.


<h3  align = "center">Updating the file with the revised list of IP addresses</h3>
&emsp;
Our final step is to update our original IP address file with the revised file. To do this first I use the `join` command to make the new file more readable by makeing each IP address appear on a new line ussing "\n".

```python
ip_addresses = "\n".join(ip_addresses)
```

&emsp;Once I have the orginized file, I reopen the inported IP file and write the new IP address file in. This will overwrite the original file with the revised file.

```python
 with open (inport_file, "w") as file:

#rewrite the file, replacing IP file with update version

    file.write(ip_addresses)
```


<h3 align = "center">Summary</h3>
&emsp;In this algorithm we converted a file into a string value and into a list. Then using that list we were able to iterate through that data to remove a base set of items and replace the original file with an orginized version of the result. If you would like, here is the code not broken up.


```python
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]
# Display `import_file`

print(import_file)

# Display `remove_list`

print(remove_list)

#Assigning allow_list.txt file to import_list for further use
import_file = allow_list.txt

#Opining imported list of allowed IPs useing with open, assigning the read "r" result to file
with open(inport_file, "r") as file:
    ip_address = file.read()   

#Using '.split()' to convert IP string to list for ideration
ip_addresses = ip_addresses.split()

for element in ip_addresses:
# Build conditional statement
  # If current element is in `remove_list`,
    
    if element in ip_addresses:
    
        # remove that element from `ip_addresses`

        ip_addresses.remove(element)

ip_addresses = "\n".join(ip_addresses)

with open (inport_file, "w") as file:

#rewrite the file, replacing IP file with update version

    file.write(ip_addresses)

#read to check that new file is working correctly
with open (ip_addresses, "r") as file:


    file.read(ip_addresses)
```
