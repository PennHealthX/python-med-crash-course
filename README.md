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

**macOS users:** macOS might already have Git installed. Open Terminal and type `git --version` to check. If you see a version number, skip to the next section!

If Git is not installed, install it using Homebrew:
```bash
brew install git
```

(If you don't have Homebrew, install it first: [brew.sh](https://brew.sh))

**Windows users:** Git installation is super easy in Ubuntu!

Open your Ubuntu terminal and run:
```bash
sudo apt install git -y
```

**Verify Installation (both platforms):**
```bash
git --version
```
You should see something like `git version 2.x.x`

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

**Install GitHub CLI:**

**macOS:**
```bash
brew install gh
```

**Windows (Ubuntu terminal):**
```bash
sudo apt install gh -y
```

**Authenticate with GitHub:**

Run this command in your terminal:
```bash
gh auth login
```

Follow the prompts:
- Choose: **GitHub.com**
- Choose: **HTTPS**
- Authenticate: **Login with a web browser** (easiest)
- Copy the code shown, press Enter, and paste it in your browser
- Sign in to GitHub and authorize

**Verify Your Connection:**

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
- Restart your terminal
- Try reinstalling Git using the commands above

**Still having issues?**
- Check the [official Git documentation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- Reach out to the course directors - everyone struggles with Git at first!

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

**Check if Python is already installed:**
```bash
python3 --version
```

**macOS users:** If you see a version number (like `Python 3.x.x`), you're all set! If not, install Python using Homebrew:
```bash
brew install python
```

> **Note:** On macOS, use `python3` instead of `python` for commands.

**Windows users:** Ubuntu comes with Python pre-installed, but let's make sure you have the latest version and necessary tools:

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv -y
```

To use `python` instead of `python3`:
```bash
sudo apt install python-is-python3 -y
```

**Verify Installation (both platforms):**
```bash
python --version
```
You should see something like `Python 3.x.x`

---

**That's it!** You now have all the course materials on your computer and a complete development environment set up. You can open the files, make changes, and start learning Python!

> **Tip:** Whenever the course materials are updated online, you can get the latest version by running `git pull` inside this folder. We'll cover this workflow in class.

---

