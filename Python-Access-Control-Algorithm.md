# 🐍 Automating IAM: Python Algorithm for File Updates

## 📌 Project Description
[cite_start]In this project, I developed a Python algorithm to automate the updating of an Identity and Access Management (IAM) file[cite: 55, 56]. I simulated a scenario as a security professional at a healthcare company tasked with managing access to a restricted subnetwork containing personal patient records. The algorithm dynamically checks a current list of approved IP addresses (`allow_list.txt`) against a secondary list of IP addresses that require revocation (`remove_list`). By automating the extraction, comparison, and overwriting of these network access logs, I ensured that restricted access policies were strictly enforced and human error was minimized.

---

## 💻 Python Algorithm Breakdown

### [cite_start]1. Open the file that contains the allow list [cite: 58]
To begin, I assigned the target file name to a variable and used a `with` statement to open the file in read mode. The `with` statement ensures the file is safely closed after the block of code executes.

```python
import_file = "allow_list.txt"
with open(import_file, "r") as file:
ip_addresses = file.read()
ip_addresses = ip_addresses.split()
for element in remove_list:
if element in ip_addresses:
        ip_addresses.remove(element)
ip_addresses = "\n".join(ip_addresses)
with open(import_file, "w") as file:
    file.write(ip_addresses)
