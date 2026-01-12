• File permissions (chmod, ls -l)

• Ownership (chown, chgrp)

• Soft links (symbolic links)

• Zip / unzip

• Directory navigation & verification

So I’ll convert exactly this practical work into a clean GitHub project with:

1️⃣ README.md
2️⃣ commands.sh

Both are copy-paste ready.

📁 GitHub Project Structure
linux-file-permissions-links/
│
├── README.md
├── commands.sh
└── screenshots/
    └── (your terminal images)

📄 README.md (Professional & Interview-Ready)
# 🐧 Linux File Permissions, Ownership & Links Project

This project demonstrates **hands-on Linux file system management**, including
file permissions, ownership, symbolic links, and compression using zip.

All commands were executed and verified on a Linux system.

---

## 🎯 Project Objectives

- Create and manage files & directories
- Understand Linux file permissions (rwx, 777, 755)
- Change ownership and groups
- Create symbolic (soft) links
- Compress and extract files using zip/unzip
- Verify changes using Linux commands

---

## 🛠️ Commands Used

| Command | Purpose |
|------|--------|
| `ls -l` | View permissions |
| `chmod` | Change permissions |
| `chown` | Change file owner |
| `chgrp` | Change group |
| `ln -s` | Create symbolic link |
| `zip` | Compress files |
| `unzip` | Extract zip |
| `cat` | View file content |
| `pwd` | Show current directory |

---

## 🚀 Steps Performed

### 1️⃣ Create File and Add Content
```bash
echo "hello world" > myfile.txt
cat myfile.txt

2️⃣ View File Permissions
ls -l myfile.txt

3️⃣ Change File Permissions
chmod 777 myfile.txt
chmod 755 myfile.txt

4️⃣ Change Ownership
sudo chown kunal myfile.txt
sudo chgrp devops myfile.txt


Verify:

ls -l myfile.txt

5️⃣ Create Symbolic (Soft) Link
ln -s /home/kunal/linux/myfile.txt softlink-file


Verify:

ls -l
cat softlink-file

6️⃣ Compress File Using zip
zip data.zip myfile.txt

7️⃣ Extract Zip File
unzip data.zip

📊 Output Verification
ls -l
cat myfile.txt
ls -l softlink-file

🧠 Key Learnings

✔ Linux permission model (rwx)
✔ Ownership & group management
✔ Symbolic links used in real systems
✔ File compression for backups
✔ Production-level Linux basics

🧑‍💻 Author

Kunal Bhatia
Linux | DevOps | Cloud Learner 🚀

⭐ GitHub Tip

If you find this project useful, give it a ⭐


---

## 📜 commands.sh (All Commands in One File)

```bash
#!/bin/bash

# Create file
echo "hello world" > myfile.txt

# View file
cat myfile.txt

# Check permissions
ls -l myfile.txt

# Change permissions
chmod 777 myfile.txt
chmod 755 myfile.txt

# Change ownership and group
sudo chown kunal myfile.txt
sudo chgrp devops myfile.txt

# Create symbolic link
ln -s /home/kunal/linux/myfile.txt softlink-file

# Verify link
ls -l
cat softlink-file

# Zip file
zip data.zip myfile.txt

# Unzip file
unzip data.zip


Make executable:

chmod +x commands.sh
