# Linux User Management Lab

## Overview
This project demonstrates basic Linux user management commands using the Bash shell. It covers:
- Adding a new user
- Assigning file ownership
- Adding a user to a secondary group
- Deleting a user

## Commands Used

### 1. Add a new user  
```bash
sudo useradd -m researcher9
sudo passwd researcher9
sudo groupadd research_team
sudo usermod -g research_team researcher9

Assign file ownership
bash
Copy
Edit
sudo mkdir -p /home/researcher2/projects
sudo touch /home/researcher2/projects/project_r.txt
sudo chown researcher9 /home/researcher2/projects/project_r.txt

Add user to a secondary group
bash
Copy
Edit
sudo groupadd sales_team
sudo usermod -aG sales_team researcher9

Delete user
bash
Copy
Edit
sudo userdel researcher9
sudo groupdel researcher9
