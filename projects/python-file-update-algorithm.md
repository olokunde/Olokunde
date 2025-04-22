# 🛠️ File Update Algorithm in Python

## 📝 What I Did

I created a Python script that **opens a file**, **reads a list of IP addresses**, and **removes unwanted IPs** from the list. After that, the script updates the file with the cleaned list.

This kind of task is useful in cybersecurity, especially when you need to update access control lists or allow-lists based on security rules.

---

## 🧠 Tools & Skills Used

- Python (File Reading & Writing)
- Lists and Loops
- Conditional Logic
- Real-world use case for system access control

---

## 🔍 My Python Code (Explained Step by Step)

```python
# 1. Open the file to read the IP list
with open("allow_list.txt", "r") as file:
    ip_addresses = file.read()

# 2. Convert the string to a list
ip_addresses = ip_addresses.split()

# 3. List of IPs to remove
remove_list = ["192.168.1.10", "10.0.0.3"]

# 4. Remove each unwanted IP if it exists
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)

# 5. Convert the list back to a string and save the file
ip_addresses = "\n".join(ip_addresses)
with open("allow_list.txt", "w") as file:
    file.write(ip_addresses)
---

## ✅ What I Learned

- How to safely open and edit files in Python  
- How to remove specific data from a list  
- Why automation matters in security tasks  
