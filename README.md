# A Medical Student's Crash Course to Python and Machine Learning

**Faculty Advisor**: Daniel Hashimoto

**Student Course Leadership**: Aaron Hsieh and Freya Gulamali

Welcome! This course covers the fundamentals of Python and machine learning. While not comprehensive, it will give you the foundation to explore and dive deeper on your own.

## Setup

What you are viewing is a repository on GitHub. You can think of repositories as individual projects, and GitHub as the place to host all your coding projects. Coders use GitHub to share code and keep track of the changes they make to their projects. This is similar to the "share" and "version history" function on Google Docs.

To get started, you will need to download this repository to your computer.

### Creating a GitHub Account

Before installing Git, you'll want to [create a free GitHub account](https://github.com/signup). This allows you to save your own projects online, collaborate with others, and access course materials.
> You should use your personal email, since you will obviously use this account longer after you graduate!

### Setting Up Your Development Environment

For this course, you'll need a Unix-like environment. This is because much of scientific computing, bioinformatics, and research computing happens in these environments.

**Windows users:** You'll need to install WSL (Windows Subsystem for Linux), which gives you a full Linux environment inside Windows. Follow the [WSL Setup Guide](wsl-setup.md) to get started.

**macOS users:** You already have a Unix environment! You'll use the built-in Terminal application:
- Find Terminal in Applications > Utilities
- Or press <kbd>⌘</kbd> + <kbd>Space</kbd> and type "Terminal"

---

### Installing Git

Git is a version control system that helps you track changes in your code and collaborate with others. Think of it as a time machine for your projects.

Git allows you to:
- Download code from GitHub (like this course!)
- Save snapshots of your work as you make changes
- Undo mistakes and go back to previous versions
- Collaborate with other developers

Choose your operating system below:

<details>
<summary><b>Windows (WSL/Ubuntu)</b></summary>

Since you installed WSL, Git installation is super easy!

1. **Open Ubuntu**
   - Search for "Ubuntu" in the Start menu

2. **Install Git**
   - Copy and paste this command:
     ```bash
     sudo apt install git -y
     ```
   - Enter your Ubuntu password when prompted

3. **Verify Installation**
   - Type: `git --version`
   - You should see something like `git version 2.x.x`

</details>

<details>
<summary><b>macOS</b></summary>

**Option 1: Using Homebrew (Recommended)**

1. **Install Homebrew** (if you don't have it)
   - Open **Terminal** (find it in Applications > Utilities)
   - Paste this command and press Enter:
     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Follow the on-screen instructions
   - Once it installs, you'll have to open a new terminal window. You can just do <kbd>⌘</kbd> + <kbd>t</kbd>

2. **Install Git**
   - In Terminal, type:
     ```bash
     brew install git
     ```

**Option 2: Using the Git Installer**

1. **Download Git for macOS**
   - Visit [git-scm.com/download/mac](https://git-scm.com/download/mac)
   - Download and run the installer

2. **Verify Installation**
   - Open **Terminal**
   - Type: `git --version`
   - You should see something like `git version 2.x.x`

> **Note:** macOS might already have Git installed. Try running `git --version` in Terminal first!

</details>

### First-Time Git Setup

After installing Git, you need to introduce yourself. Git uses this information when you save changes.

Open your **terminal** (Terminal on macOS, Ubuntu on Windows) and run:

```bash
git config --global user.name "Your Name" # does not have to be your username
git config --global user.email "your.email@example.com"
```

**Example:**
```bash
git config --global user.name "Jane Doe"            
git config --global user.email "jane.doe@gmail.com"
```

> **Important:** Use the same email you used to create your GitHub account!

### Connecting Git to Your GitHub Account

Now that Git knows who you are, you need to connect it to your GitHub account so you can download and upload code. GitHub requires authentication for security.

#### Installing GitHub CLI (Recommended Method)

The easiest way to authenticate is using the **GitHub CLI** (Command Line Interface):

<details>
<summary><b>Windows (WSL/Ubuntu)</b></summary>

1. **Install GitHub CLI in Ubuntu**
   - Open Ubuntu terminal
   - Run these commands:
     ```bash
     sudo apt install gh -y
     ```

2. **Authenticate**
   - In Ubuntu, type:
     ```bash
     gh auth login
     ```
   - Follow the prompts:
     - Choose: **GitHub.com**
     - Choose: **HTTPS**
     - Authenticate: **Login with a web browser** (easiest)
     - Copy the code shown, press Enter, and paste it in your browser
     - Sign in to GitHub and authorize

</details>

<details>
<summary><b>macOS</b></summary>

1. **Install GitHub CLI**
   - If you have Homebrew (from earlier):
     ```bash
     brew install gh
     ```
   - Or download from [cli.github.com](https://cli.github.com)

2. **Authenticate**
   - In Terminal, type:
     ```bash
     gh auth login
     ```
   - Follow the prompts:
     - Choose: **GitHub.com**
     - Choose: **HTTPS**
     - Authenticate with your GitHub credentials
     - Authenticate: **Login with a web browser** (easiest)
     - Copy the code shown, press Enter, and paste it in your browser
     - Sign in to GitHub and authorize

</details>

#### Verify Your Connection

Test that everything is working:

```bash
gh auth status
```

You should see a message confirming you're logged in!

```bash
github.com
  ✓ Logged in to github.com account ayhsieh (keyring)
  - Active account: true
  - Git operations protocol: https
  - Token: gho_************************************
  - Token scopes: 'gist', 'read:org', 'repo', 'workflow'
```

> **What just happened?** You gave Git permission to access your GitHub account securely. Now you can download (clone) repositories and upload (push) your code to GitHub without entering your password every time.

### Troubleshooting

**"git is not recognized" or "command not found"**
- Restart your terminal/command prompt
- On Windows, make sure you selected the PATH option during installation
- Try reinstalling Git

**Still having issues?**
- Check the [official Git documentation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- Ask for help - everyone struggles with Git at first!

---

### Downloading This Repository

Now that you're all set up, let's download this course to your computer! This is called "cloning" a repository.

1. **Choose a location**
   - Decide where you want to save this course (e.g., your Documents folder)
   - Open your terminal and navigate there:
     ```bash
     cd Documents
     ```

2. **Clone the repository**
   - Copy the command below and run it in your terminal:
     ```bash
     git clone https://github.com/pennhealthx/python-med-crash-course.git
     ```
   - Git will download all the course files to a new folder called `python-med-crash-course`

3. **Enter the folder**
   ```bash
   cd python-med-crash-course
   ```

### Installing Python

The final step is installing Python on your computer.

<details>
<summary><b>Windows (WSL/Ubuntu)</b></summary>

Ubuntu comes with Python pre-installed, but let's make sure you have the latest version and necessary tools.

1. **Check if Python is installed**
   - In Ubuntu terminal, type:
     ```bash
     python3 --version
     ```
   - You should see something like `Python 3.x.x`

2. **Install Python and pip** (if not already installed)
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip python3-venv -y
   ```

3. **Set up python command**
   - Ubuntu uses `python3` by default. To use `python` instead:
     ```bash
     sudo apt install python-is-python3 -y
     ```

4. **Verify Installation**
   ```bash
   python --version
   ```
   You should see something like `Python 3.x.x`

</details>

<details>
<summary><b>macOS</b></summary>

**Check if Python is already installed:**
```bash
python3 --version
```

If you see a version number (like `Python 3.x.x`), you're all set!

If not, install Python using Homebrew:

```bash
brew install python
```

> **Note:** On macOS, use `python3` instead of `python` for commands (e.g., `python3 --version`)

**Detailed instructions:** [Install Python for MacOS](https://realpython.com/installing-python/#macos-how-to-check-or-get-python)

</details>

---

**That's it!** You now have all the course materials on your computer and a complete development environment set up. You can open the files, make changes, and start learning Python!

> **Tip:** Whenever the course materials are updated online, you can get the latest version by running `git pull` inside this folder. We'll cover this workflow in class.

---

