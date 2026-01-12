# Installing WSL (Windows Subsystem for Linux)

## What is WSL?

WSL lets you run a Linux environment directly on Windows without a virtual machine. This is essential for research computing because:
- Most bioinformatics tools run on Linux
- Research clusters and servers use Linux
- It's easier to manage Python packages and dependencies
- You'll learn command-line skills used in computational research

## Prerequisites

- Windows 10 (version 2004 or higher) or Windows 11
- Administrator access on your computer
- About 10 GB of free disk space

## Installation Steps

**1. Open PowerShell as Administrator**
   - Press <kbd>Win</kbd> + <kbd>X</kbd>
   - Select "Windows PowerShell (Admin)" or "Terminal (Admin)"
   - Click "Yes" when prompted for permissions

**2. Install WSL**
   - Copy and paste this command:
     ```bash
     wsl --install
     ```
   - Press Enter and wait 5-10 minutes (it's downloading Ubuntu Linux)
   - You'll see messages about enabling features and installing Ubuntu

**3. Restart Your Computer**
   - After installation completes, restart your computer
   - This is required to complete the setup

**4. First Launch**
   - After restart, Ubuntu will open automatically (if not, search for "Ubuntu" in Start menu)
   - Wait a minute while it completes setup
   - You'll be asked to create a username and password:
     - **Username**: Choose something simple (e.g., your first name, all lowercase, no spaces)
     - **Password**: Type a password (you won't see anything as you type - this is normal!)
     - **Confirm password**: Type it again

   > **Important:** Remember this password! You'll need it for installing software.

**5. Verify Installation**
   - You should now see a command prompt like: `yourname@computername:~$`
   - Type this command to check your Ubuntu version:
     ```bash
     lsb_release -a
     ```
   - You should see information about Ubuntu

**6. Update Your System**
   - Run these commands to update Ubuntu (copy and paste each line, press Enter):
     ```bash
     sudo apt update
     sudo apt upgrade -y
     ```
   - When prompted for your password, type the password you created earlier

## Using WSL

**Opening Ubuntu:**
- Search for "Ubuntu" in the Windows Start menu, or
- Open Windows Terminal and select "Ubuntu" from the dropdown

**Accessing Your Windows Files:**
Your Windows C: drive is available at `/mnt/c/`. For example:
```bash
cd /mnt/c/Users/YourName/Documents
```

**Where WSL Files Live:**
Your Linux home directory (`~`) is separate from Windows. For this course, you can work in either location, but I recommend using your Windows Documents folder for easy access:
```bash
cd /mnt/c/Users/YourName/Documents
```

## Troubleshooting

**"WSL 2 requires an update to its kernel component"**
- Follow the link in the error message to download the kernel update
- Install it and run `wsl --install` again

**"Virtualization is not enabled"**
- Restart your computer and enter BIOS (usually press F2, F10, or Del during startup)
- Look for "Virtualization Technology" or "Intel VT-x" / "AMD-V"
- Enable it and save changes
- If you're uncomfortable with BIOS, ask for help!

**"This app can't run on your PC" or installation fails**
- Make sure you have Windows 10 version 2004 or higher:
  - Press <kbd>Win</kbd> + <kbd>R</kbd>, type `winver`, press Enter
  - Check your version number
- Update Windows if needed: Settings > Update & Security > Windows Update

**Already have WSL but it's an older version?**
- Update to WSL 2:
  ```bash
  wsl --set-default-version 2
  ```

**Forgot your Ubuntu password?**
Don't worry, you can reset it! Follow these steps:
1. Open PowerShell as Administrator
2. Find your default Ubuntu username:
   ```bash
   wsl whoami
   ```
3. Reset the password by running (replace `username` with your actual username):
   ```bash
   wsl -u root passwd username
   ```
4. Enter your new password twice when prompted
5. Close PowerShell and open Ubuntu normally - your password is now reset!

**Still having issues?**
- Check Microsoft's official documentation: [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
- Reach out to the course directors for help!

---

**From this point forward, Windows users should use the Ubuntu terminal for all commands in this course, not PowerShell or Command Prompt.**

[← Back to Setup](README.md#setting-up-your-development-environment)
