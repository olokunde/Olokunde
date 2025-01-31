# Linux File Permissions Demonstration  

This repository contains an example of a Linux directory (`/home/researcher2/projects`) with different file permissions.  

## Directory Structure  

/home/researcher2/projects
├── project_k.txt (User: rw, Group: rw, Other: rw)
├── project_m.txt (User: rw, Group: r, Other: none)
├── project_r.txt (User: rw, Group: rw, Other: r)
├── project_t.txt (User: rw, Group: rw, Other: r)
├── .project_x.txt (User: rw, Group: w, Other: none)
└── drafts/ (User: rwx, Group: x, Other: none)


## 🔑 Understanding File Permissions  

- **Read (r):** View the file contents.  
- **Write (w):** Modify the file contents.  
- **Execute (x):** Run the file as a script or access a directory.  

## 🛠️ How to Modify Permissions  

Use `chmod` to change permissions:  
```bash
chmod 644 project_m.txt  # Sets permissions to rw-r--r--
chmod 750 drafts         # Sets directory permissions to rwxr-x---


3️⃣ **Save and Exit nano**  
- **Press** `CTRL + X` to exit.  
- **Press** `Y` to confirm saving.  
- **Press** `ENTER` to finalize the save.  

---

### **📌 Final Step: Upload to GitHub**
After saving the file, run these commands to push the changes to GitHub:

```bash
git add README.md
git commit -m "Added README with file permissions"
git push origin main
How to Check File Permissions

To see file permissions, use the command:

ls -la

This shows a list of all files, including hidden files, along with their permissions.

Example Output:

-rw-r--r--  1 user group  1234 Jan 31 12:00 project_m.txt
drwx------  2 user group  4096 Jan 31 12:00 drafts

🔍 Understanding the 10-Character File Permission String

Each file in Linux has a 10-character permission string like this:

-rw-r--r--

Position	Meaning	Example (-rw-r--r--)
1st	File type (- = file, d = directory)	- (regular file)
2-4	Owner permissions	rw- (read, write, no execute)
5-7	Group permissions	r-- (read-only)
8-10	Other (everyone else) permissions	r-- (read-only)
👀 Hidden Files in Linux

Hidden files start with a . (dot).
To see them, use:

ls -la

📌 Example of a hidden file: .project_x.txt
📌 Summary

✅ I demonstrated how to check file permissions using ls -la
✅ I explained the 10-character permission string
✅ I learned how to change file permissions using chmod
✅ I discussed hidden files and how to view them
