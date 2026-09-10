# Jupyter Notebook on Kali Linux

A beginner-friendly guide to installing and running Jupyter Notebook on Kali Linux.

This guide starts from the basics and explains how to:

- Check Python on Kali Linux
- Check pip
- Create a Python virtual environment
- Install Jupyter Notebook
- Launch Jupyter Notebook
- Create your first Python notebook
- Run your first Python program
- Save a Jupyter Notebook
- Stop the Jupyter server safely

---

## Requirements

Before starting, you need:

- Kali Linux
- Internet connection
- A user account with `sudo` privileges
- Python 3

---

# 1. Check Python

Open the Kali Linux terminal.

Run:

```bash
python3 --version

Example:
Python 3.14.6

If Python is installed, continue to the next step.

2. Update Kali Linux Package Information
Update the package lists:

sudo apt update

Enter your Kali Linux password when requested.
Note: This command updates package information. It does not upgrade the entire operating system.

3. Check pip
Check whether pip is installed:

pip3 --version

Example:
pip 26.1.2 from /usr/lib/python3/dist-packages/pip (python 3.14)

4. Check Python Virtual Environment Support
Check whether the venv module is available:

python3 -m venv --help

If the command displays the virtual environment help page, venv is available.

5. Create a Project Directory
Create a directory for your Jupyter project:

mkdir ~/jupyter-kali-linux

Enter the directory:

cd ~/jupyter-kali-linux

Verify your current location:

pwd

You should see something similar to:
/home/username/jupyter-kali-linux

6. Create a Virtual Environment
Create a virtual environment named .venv:

python3 -m venv .venv

This creates an isolated Python environment for Jupyter.
The project structure will look similar to:

jupyter-kali-linux/
└── .venv/

7. Activate the Virtual Environment
Activate the environment:

source .venv/bin/activate

Your terminal prompt should now contain:
(.venv)

For example:
(.venv) user@kali:~/jupyter-kali-linux$

Whenever you work with this Jupyter installation, activate the virtual environment first.

8. Upgrade pip
With the virtual environment active, upgrade pip:

python -m pip install --upgrade pip

Verify pip:

python -m pip --version

9. Install Jupyter
Install Jupyter inside the virtual environment:

python -m pip install -r requirements.txt

This installs Jupyter Notebook and its required dependencies.

10. Verify the Jupyter Installation
Check the installed Jupyter components:

jupyter --version

You should see versions for components such as:
IPython
ipykernel
jupyter_client
jupyter_core
jupyter_server
jupyterlab
notebook

The exact versions may be different from the versions shown in this guide.

11. Start Jupyter Notebook
Start the Jupyter server:

jupyter notebook

Jupyter will start a local server and normally open your web browser automatically.
You may see a URL similar to:

http://localhost:8888/tree?token=...

Keep the terminal open while Jupyter is running.
The token shown in the URL is used for authentication. Do not share it publicly.

12. Create Your First Notebook
In the Jupyter browser interface:

Click New.
Select Python 3.
A new notebook will open.
The notebook will use the Python kernel provided by your virtual environment.

13. Run Your First Python Program
Enter the following code into a notebook cell:

print("Hello, Kali Linux!")
print("Jupyter Notebook is working successfully.")

Run the cell by pressing:

Shift + Enter

Expected output:
Hello, Kali Linux!
Jupyter Notebook is working successfully.

If you see this output, Python and Jupyter Notebook are working correctly.

14. Save Your Notebook
Rename your notebook to:

first_program.ipynb

Save the notebook.
The .ipynb extension means that this is a Jupyter Notebook file.

15. Stop Jupyter Notebook
When you finish working, return to the terminal where Jupyter is running.

Press:
Ctrl + C

If Jupyter asks:
Shutdown this Jupyter server (y/[n])?

Enter:
y

Then press Enter.
The Jupyter server and kernel will shut down.

16. Start Jupyter Again Later
When you want to use the project again:

cd ~/jupyter-kali-linux

Activate the virtual environment:
source .venv/bin/activate

Start Jupyter:
jupyter notebook

17. Deactivate the Virtual Environment
After stopping Jupyter, you can leave the virtual environment with:

deactivate

The (.venv) prefix will disappear from your terminal prompt.

18. Troubleshooting
python3: command not found

Check whether Python is installed:
python3 --version

If Python is missing, install it using Kali's package manager.
pip3: command not found

Check your Python installation and install the appropriate pip package using Kali's package manager.
python3 -m venv .venv fails

Make sure the Python virtual-environment support is installed for your Kali/Python setup.
Then try:

python3 -m venv .venv
jupyter: command not found

Make sure the virtual environment is active:
source .venv/bin/activate

Then check:
jupyter --version

If Jupyter is not installed, run:
python -m pip install jupyter

Jupyter does not open the browser automatically
Start Jupyter from the terminal:

jupyter notebook

Copy the http://localhost:8888/... URL shown in the terminal and open it manually in your browser.

19. Project Structure
After completing this guide, your project can look like:

jupyter-kali-linux/
├── .gitignore
├── README.md
└── first_program.ipynb

The .venv/ directory exists locally but is intentionally excluded from Git.

20. Why Use a Virtual Environment?
A virtual environment keeps Python packages for this project separate from Kali Linux's system Python installation.

Benefits include:

Avoiding unnecessary changes to system Python
Keeping project dependencies isolated
Making the setup easier to reproduce
Reducing package conflicts
Making the project cleaner for GitHub

21. Useful Commands
Check Python
python3 --version
Check pip
python -m pip --version
Activate environment
source .venv/bin/activate
Start Jupyter
jupyter notebook
Check Jupyter
jupyter --version
Deactivate environment
deactivate

22. Security Notes
Jupyter Notebook starts a local server by default.

For a beginner setup, use Jupyter locally and avoid exposing the Jupyter server directly to the internet.

Never publicly share:
Jupyter authentication tokens
Passwords
GitHub Personal Access Tokens
API keys
SSH private keys
Other sensitive credentials

Conclusion
You have now learned how to:

Check Python on Kali Linux
Check pip
Create a Python virtual environment
Install Jupyter Notebook
Launch Jupyter
Create a Python notebook
Run your first Python program
Save a notebook
Stop Jupyter safely

Your Kali Linux system is now ready for Python development and Jupyter Notebook experiments.

Author
Created as a beginner-friendly learning resource for Kali Linux and Jupyter Notebook.

If this guide helped you, consider giving the repository a star.
