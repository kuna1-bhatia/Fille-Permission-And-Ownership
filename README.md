📁 GitHub Repository Structure
linux-file-permission-ownership/
│
├── README.md
├── commands.sh
├── output.txt
└── screenshots/
    └── (optional terminal screenshots)

📄 README.md
# 🐧 Beginner Linux Project – File Permission & Ownership

This beginner Linux project focuses on **File Permissions and Ownership**, which are core responsibilities of a Linux System Administrator.

The project demonstrates how permissions work, how ownership is managed, and how Linux controls access to files and directories.

---

## 📌 Project Objectives

- Create directories for multiple users
- Understand read, write, and execute permissions
- Modify permissions using `chmod`
- Change ownership using `chown` and `chgrp`
- Understand numeric permissions (755, 644)
- Use `umask` to control default permissions

---

## 🛠️ Commands Used

| Command | Purpose |
|------|--------|
| `chmod` | Change file permissions |
| `chown` | Change file owner |
| `chgrp` | Change group ownership |
| `ls -l` | View permissions |
| `umask` | Set default permission mode |

---

## 🚀 Steps Performed

### 1️⃣ Create Directories
```bash
mkdir /tmp/user1_dir
mkdir /tmp/user2_dir


Example output:

drwxr-xr-x 2 root root 4096 user1_dir

🔐 Understanding Permissions (rwx)
Symbol	Meaning
r	Read
w	Write
x	Execute
Permission Positions:
rwx r-x r-x
 │   │   │
 │   │   └─ Others
 │   └──── Group
 └──────── Owner

🔢 Numeric Permission Explanation
755
Role	Permission
Owner	rwx (7)
Group	r-x (5)
Others	r-x (5)

Command:

chmod 755 user1_dir

644
Role	Permission
Owner	rw- (6)
Group	r-- (4)
Others	r-- (4)

Command:

chmod 644 file.txt

👤 Change Ownership
Change Owner
sudo chown user1 user1_dir

Change Group
sudo chgrp devteam user1_dir

🎭 Using umask

Check current umask:

umask


Set umask:

umask 022


Effect:

Directories → 755

Files → 644

📊 Output Verification
ls -l
ls -ld user1_dir

🎯 Learning Outcome

✔ Strong understanding of Linux permissions
✔ Numeric & symbolic permission mastery
✔ Ownership and group management
✔ Real-world admin skills

🧑‍💻 Author

Kunal Bhatia
Linux & DevOps Beginner 🚀

⭐ GitHub Tip

Star ⭐ the repository if this helped you!


---

# 📜 `commands.sh`

```bash
#!/bin/bash

mkdir /tmp/user1_dir
mkdir /tmp/user2_dir

chmod 755 /tmp/user1_dir
chmod 644 /tmp/file.txt

sudo chown user1 /tmp/user1_dir
sudo chgrp devteam /tmp/user1_dir

umask 022


Make executable:

chmod +x commands.sh

📝 output.txt (Example)
drwxr-xr-x 2 user1 devteam 4096 user1_dir
-rw-r--r-- 1 user1 devteam 0 file.txt
