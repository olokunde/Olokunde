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
