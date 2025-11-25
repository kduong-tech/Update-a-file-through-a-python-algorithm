# Updating an Allow List Using Python (File Parsing Algorithm)

This project is part of the Google Cybersecurity Professional Certificate. It demonstrates how to use Python to open files, read and parse contents, remove restricted IP addresses, and update the file with revised data. This type of algorithm is valuable for cybersecurity tasks involving access control, network restrictions, and automated file maintenance.

---

## 📄 Project Files
- Completed Python file update algorithm  
- Allow list & remove list (example files)  
- Activity instructions  
- Python code formatting guidelines  

---

## 📝 Project Description
As a security professional at a healthcare company, I was responsible for maintaining a file containing IP addresses permitted to access a restricted subnetwork. A remove list documented which employees should no longer have access based on their job role. I created a Python algorithm that reads the allow list file, compares its addresses to the remove list, removes unauthorized entries, and rewrites the updated list back to the file.

---

## Following Steps
```python
import_file = "allow_list.txt"
Step 1: Open the Allow List File
```python
import_file = "allow_list.txt"
with open(import_file, "r") as file:
    ip_addresses = file.read()
## 📖 Step 2: Read the File Contents
```python
ip_addresses = file.read()

## 🪢 Step 3: Convert the String Into a List
```python
ip_addresses = ip_addresses.split()

## 🔁 Step 4: Iterate Through the Remove List
```python
for element in remove_list:

## ❌ Step 5: Remove Restricted IP Addresses
```python
if element in ip_addresses:
    ip_addresses.remove(element)
## 💾 Step 6: Update the File
```python
updated_list = "\n".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(updated_list)
