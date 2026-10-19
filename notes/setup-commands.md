# Setup commands: what they mean

Notes from setting up my bioinformatics environment (WSL2 Ubuntu, Git, GitHub, Miniconda).

---

## 1. Windows PowerShell (setting up Linux)

| Command | What it does |
|---|---|
| `wsl --install -d Ubuntu` | Installs WSL (Windows Subsystem for Linux) and the Ubuntu Linux distribution, so Windows can run a Linux terminal |
| `wsl --update` | Updates the WSL component itself |
| `wsl --status` | Shows WSL's current settings; useful for checking that virtualization works |
| `wsl --list --online` | Lists the Linux distributions available to install |
| `dism.exe /online /enable-feature ...` | Turns on Windows features (Virtual Machine Platform, WSL) that Linux needs to run |
| `bcdedit /set hypervisorlaunchtype auto` | Makes Windows start its virtualization layer at boot |
| `ipconfig /flushdns` | Clears the saved list of website addresses, fixing "could not be resolved" network errors |

**Key idea:** WSL2 runs a real Linux system inside Windows. Almost all bioinformatics software is built for Linux, which is why we need it.

---

## 2. Basic Linux navigation

| Command | What it does |
|---|---|
| `pwd` | **P**rint **w**orking **d**irectory: shows which folder I'm in |
| `ls` | **L**i**s**t the files and folders here |
| `cd folder` | **C**hange **d**irectory: go into a folder |
| `cd ..` | Go up one folder |
| `cd ~` | Go to my home folder (`/home/hp`) |
| `mkdir name` | **M**a**k**e a new **dir**ectory (folder) |
| `rmdir name` | **R**e**m**ove an empty **dir**ectory |
| `echo "text" > file.md` | Writes the text into a file (creates it, or overwrites it) |
| `cat file` | Prints a file's contents on screen |

**Key idea:** work in `/home/hp` (Linux home), not in `/mnt/c/...` (the Windows drive). It's faster and safer.

---

## 3. Installing software on Ubuntu

| Command | What it does |
|---|---|
| `sudo` | "Run this as administrator." Asks for my Ubuntu password (nothing shows as I type) |
| `sudo apt update` | Refreshes Ubuntu's list of available software and versions |
| `sudo apt upgrade -y` | Updates everything already installed (`-y` means "answer yes to prompts") |
| `sudo apt install git -y` | Installs Git |
| `&&` | Runs the second command only if the first one succeeded |

**Key idea:** `apt` is Ubuntu's built-in app store for command-line tools.

---

## 4. Git and GitHub

| Command | What it does |
|---|---|
| `git config --global user.name "..."` | Sets the name attached to my commits |
| `git config --global user.email "..."` | Sets the email attached to my commits (same as my GitHub email) |
| `git config --list` | Shows my Git settings |
| `ssh-keygen -t ed25519 -C "email"` | Creates a pair of keys: a private one (stays on my laptop, never shared) and a public one (given to GitHub) |
| `cat ~/.ssh/id_ed25519.pub` | Shows the public key so I can paste it into GitHub |
| `ssh -T git@github.com` | Tests that my laptop can log in to GitHub using the key |
| `git clone <address>` | Downloads a repository from GitHub to my laptop |
| `git add file` | Chooses which changes go into the next snapshot |
| `git commit -m "message"` | Saves a labeled snapshot of those changes on my laptop |
| `git push` | Uploads my commits to GitHub |
| `git mv old new` | Moves or renames a file in a way Git tracks |

**The daily cycle:** edit files, then `git add`, `git commit`, `git push`.

**Key idea:** Git keeps the history of my work; GitHub is the online copy and my portfolio.

---

## 5. Conda (Python and tool manager)

| Command | What it does |
|---|---|
| `wget <url> -O file` | Downloads a file from the internet and saves it under the name I give |
| `bash script.sh` | Runs a shell script |
| `rm file` | Deletes a file (permanent, no recycle bin; be careful) |
| `conda init bash` | Makes conda load automatically whenever I open the terminal |
| `conda --version` | Shows the installed conda version |
| `conda config --add channels X` | Adds a download source (a "channel") for conda |
| `conda config --set channel_priority strict` | Prefers packages from the higher-priority channel, avoiding conflicts |
| `conda create -n bioinfo python=3.12 -y` | Creates a separate workspace (environment) called `bioinfo` with Python 3.12 |
| `conda activate bioinfo` | Switches into that workspace |
| `python --version` | Shows the Python version in use |

**Channels I use:**
- `conda-forge`: general scientific software (top priority)
- `bioconda`: bioinformatics tools
- `defaults`: Anaconda's own packages

**Key idea:** environments keep projects separate, so installing a tool for one project can't break another. Habit: run `conda activate bioinfo` at the start of every study session, and don't install tools into `(base)`.

---

## Safety rules I follow
- Only run commands from sources I trust.
- Be extra careful with `sudo`, `rm`, and `curl ... | bash` (runs a downloaded script blindly).
- Before running a command, ask: what is this trying to do?
- After running it, write one line in my own words in my notes.

---

## Terms
- **Terminal / shell:** the text window where I type commands
- **Directory:** a folder
- **Repository (repo):** a project folder tracked by Git
- **Commit:** a saved snapshot of my work
- **Environment:** an isolated workspace with its own tools and versions
- **Package:** a piece of software installed by a manager like apt or conda
- **Channel:** a source conda downloads packages from
