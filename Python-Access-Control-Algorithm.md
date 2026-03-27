# 🐍 Automating Access Control: Python Algorithm for File Updates

## 📌 Project Description
In this project, I developed a Python algorithm to automate the updating of an Identity and Access Management (IAM) file. I simulated a scenario as a security professional at a health care company tasked with managing access to a restricted subnetwork containing personal patient records. The algorithm dynamically checks a current list of approved IP addresses (`allow_list.txt`) against a secondary list of IP addresses that require revocation (`remove_list`). By automating the extraction, comparison, and overwriting of these network access logs, I ensured that restricted access policies were strictly enforced.

---

## 💻 The Complete Python Script
Here is the complete algorithm I developed to automate the file update process:

```python
# Assign the file name to a variable
import_file = "allow_list.txt"

# Open the file and read its contents
with open(import_file, "r") as file:
    ip_addresses = file.read()

# Convert the string into a list to remove individual IP addresses
ip_addresses = ip_addresses.split()

# Iterate through the remove list
for element in remove_list:
    
    # Check if the current element is in the allow list
    if element in ip_addresses:
        # Remove the IP address from the allow list
        ip_addresses.remove(element)

# Convert the list back into a string, separating each IP on a new line
ip_addresses = "\n".join(ip_addresses)

# Rewrite the original file with the updated string
with open(import_file, "w") as file:
    file.write(ip_addresses)
```

---

## 🔍 Step-by-Step Code Breakdown

### Open the file that contains the allow list
To begin, I assigned the target file name `"allow_list.txt"` to a variable named `import_file`. Then, I used a `with` statement and the `open()` function in read mode (`"r"`) to securely open the file. I assigned the opened file to the variable `file` to work with it inside the `with` block.

### Read the file contents
To read the file contents, I used the `.read()` method on the `file` variable inside the `with` statement. This converts the raw contents of the file into a single string format so it can be manipulated. I stored this resulting string in a variable called `ip_addresses`.

### Convert the string into a list
In order to remove individual IP addresses from the allow list, the data needed to be in a list format rather than a single string. I used the `.split()` method on the `ip_addresses` string, which converts the string into a list by separating the values at each whitespace character.

### Iterate through the remove list
A second list named `remove_list` contains the IP addresses that must be revoked from the network. I used a `for` loop to iterate through this list. I set up the loop header using the `element` keyword as the loop variable to represent each individual IP address as the loop progresses.

### Remove IP addresses that are on the remove list
Inside the body of the `for` loop, I created a conditional `if` statement to evaluate whether the current `element` (the IP address from the remove list) was present in the `ip_addresses` list. If the condition evaluated to True, I applied the `.remove()` method to delete that specific IP address from the `ip_addresses` list. Applying the `.remove()` method in this way is possible because there are no duplicate IP addresses in the allow list.

### Update the file with the revised list of IP addresses
After removing the unauthorized IP addresses, I needed to update the original file. First, I converted the `ip_addresses` list back into a string using the `.join()` method. I applied `.join()` to the newline character `"\n"` so that each IP address would be separated and placed on a new line in the file. Then, I used another `with` statement and the `open()` function, this time in write mode (`"w"`), to overwrite the existing file. Finally, I used the `.write()` method to write the updated `ip_addresses` string into the file.

---

## 📝 Summary
I created a Python algorithm to automate the process of updating a network access control list. The algorithm opens a text file containing an allow list, reads its contents into a string, and converts that string into a list for precise data manipulation. It then iterates through a separate remove list, checking if any of those IP addresses are present in the allow list, and removes them if they are found. Finally, the algorithm converts the revised list back into a string format and overwrites the original text file with the updated, secure allow list. This effectively demonstrates the ability to use Python scripting to enforce Identity and Access Management (IAM) policies.
