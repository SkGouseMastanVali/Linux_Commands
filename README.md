# Linux_Commands
Daily usage linux commands

# 🐧 Linux Commands for Daily Data Engineering / Analysis Work

A practical cheatsheet-style guide for everyday Linux usage as a **Data Engineer / Analyst / Scientist**. All commands are tested on Ubuntu/WSL.

---

## 📁 Basic File Operations

```bash
cd <dir_name>         # change to specified directory
cd /path/to/dir       # change directory
cd ..                 # go back one directory
cd ~                  # go to home directory
ls                    # list files and directories
ls -ltr               # list in long format, sorted by time
pwd                   # print current working directory

mkdir <dir_name>      # create a new directory   (mkdir new_folder)
touch <file_name>     # create an empty file or update its timestamp
cp <src> <dest>       # copy file or folder    (cp file1 file2)
mv <src> <dest>       # move or rename file or folder    (mv oldfile newfile)
rm <filename>         # delete a file
rm -r <dir_name>      # delete directory and its contents recursively
```

---

## 📦 Working with Data Files

```bash
head -n 10 file.csv     # view first 10 lines
tail -n 20 file.csv     # view last 20 lines
cat file.csv            # print whole file
less file.csv           # scroll file, q to exit
wc -l file.csv          # count number of lines
cut -d',' -f1,3 file.csv # extract columns 1 and 3 from CSV
```

---

## 🔍 Searching

```bash
grep 'apple' file.txt            # search for 'apple'
grep -i 'apple' file.txt         # case-insensitive
grep -r 'text' /path/folder      # search recursively
find . -name '*.csv'             # find all CSVs in current dir
```

---

## 📊 Disk & Resource Monitoring

```bash
df -h              # disk usage per mount
free -h            # memory usage
top                # live CPU/memory stats
htop               # advanced top (install with sudo apt install htop)
du -sh *           # size of folders/files in current directory
```

---

## 📂 Permissions & Ownership

```bash
chmod +x script.sh         # make a script executable
chmod 755 filename         # rwxr-xr-x
chown user:group filename  # change file owner
touch file.txt             # create empty file / update timestamp
```

---

## 📝 Editing Files

```bash
nano file.txt         # quick and easy editor
vi file.txt           # powerful but steep learning curve
vim filename          # open file in vim editor
code .                # open current folder in VSCode (if installed)
```

---

## 🧠 Useful One-Liners for Data

```bash
sort file.csv | uniq                # remove duplicates
awk -F',' '{print $2}' file.csv     # print 2nd column of CSV
awk 'NR > 1' file.csv               # skip header
cut -d',' -f1,2 file.csv | sort     # select & sort cols
```

---

## 🐍 Python + CSV Quick Scripts

```bash
python3 -c "import pandas as pd; df = pd.read_csv('data.csv'); print(df.head())"
```

---

## 🐘 PostgreSQL / BigQuery / DB-like stuff

```bash
psql -h host -U user -d dbname      # connect to Postgres
gcloud bq query --use_legacy_sql=false 'SELECT * FROM dataset.table LIMIT 10'  # BigQuery
```

---

## 🐳 Docker & Git (Common Ops)

```bash
docker ps             # list running containers
docker exec -it <id> bash   # enter a container

git status
git add .
git commit -m "message"
git push origin main
```

---

## 📅 Cron Jobs (Schedule Tasks)

```bash
crontab -e
# Example: run every day at 6 AM
0 6 * * * /usr/bin/python3 /home/user/script.py
```

---

## 💡 Misc Handy Stuff

```bash
history | grep ssh          # search command history
alias ll='ls -alF'          # make aliases (add to ~/.bashrc)
screen                     # resume sessions even if terminal closes
```

---

## 🔧 Trouble & Debug

```bash
ps aux | grep python        # check running Python processes
kill -9 <PID>               # force kill process
lsof -i :8000               # check what’s using port 8000
```

---

## ✅ Most Commonly Used Commands

```bash
cd <dir_name>       # change directory
cd ..               # go back one level
cd ~                # home directory
ls                  # list directory
ls -ltr             # long listing, sorted by time
pwd                 # print current directory

mkdir <dir_name>    # make directory
touch <file_name>   # create empty file
cp <src> <dest>     # copy
mv <src> <dest>     # move/rename
rm <filename>       # delete file
rm -r <dir_name>    # delete folder recursively

vi <filename>       # edit file in vi
vim <filename>      # edit file in vim

cat <filename>      # view file content
less <filename>     # view with paging
chmod 755 <filename> # change permissions
kill <process_id>   # kill a process
```

---

## ✅ Personal Tips

- Use `tmux` or `screen` to avoid losing progress if your terminal closes.
- Keep raw and processed files in separate folders.
- Maintain a log of every script change or cron job in a `logs/` folder.
- Learn `awk`, `sed`, and `jq` slowly — they're super powerful for text & JSON.

---

Will try to Keep this repo updated as I learn more cool commands 🚀

📍 Last updated: April 2025
