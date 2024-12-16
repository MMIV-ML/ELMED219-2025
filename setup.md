[ELMED219](https://www.uib.no/en/course/ELMED219): Artificial intelligence and computational medicine

# Setting up your system

_v. 2024-12-16_

<img src="./assets/GPT-MedAI.png" width="500"> <br>
If you have a subscription to [ChatGPT Pluss](https://openai.com/blog/chatgpt-plus), you can also try out the [**Medical AI Assistant (UiBmed - ELMED219 & BMED365)**](https://chat.openai.com/g/g-d90dfN17H-medical-ai-assistant-uibmed-elmed219-bmed365) and see if you can get it to answer some of your questions.

_NOTE: ChatGPT can make mistakes. Consider checking important information._

## Table of Contents
- [Are you using Windows?](#are-you-using-windows)
- [Are you using Mac?](#are-you-using-mac)
- [Are you using Linux?](#are-you-using-linux)
- [Notes on the command line (shell) and Notebooks](#notes-on-the-command-line-shell-and-notebooks)
- [Notes on GitHub](#notes-on-github)
- [Notes on Anaconda](#notes-on-anaconda)
- [Notes on Colab](#notes-on-colab)
    - [What is Google Colab?](#what-is-google-colab)
- [Install and test your course environment](#install-and-test-yoiur-course-environment)
    - [00-test-installation.ipynb](#test-your-installation)
- [Unix shell](#unix-shell)
- [Programming with Python](#programming-with-python)
- [A note on R (tip for previous R users)](#a-note-on-r-tip-for-previous-r-users)


# Are you using Windows?
Then you must install [Git for Windows](https://gitforwindows.org) (for free) before you start. See also [here](https://www.youtube.com/watch?v=J_Clau1bYco). Thereafter:

<img src="./assets/You.png" width="100"> <br>
_How to set up and use GitHub and Jupyter notebooks on **Windows**, by (i) using Anaconda,  (ii) using Visual Studio Code (or Cursor.ai), (iii)  initially cloning the ELMED219-2025 course repository, (iv) activate its conda environment  "elmed219-2025" as specified in "environment.yml" , and (v) being able to experiment with my own notebooks (making a local copy) in this environment without getting in conflict with the original repository?_

<img src="./assets/GPT-MedAI.png" width="370"> <br>

Setting up and using GitHub and Jupyter notebooks on Windows for the ELMED219-2025 course, with Anaconda and Visual Studio Code (or Cursor.ai), involves several steps. I'll guide you through them:

### 1. **Install Anaconda, Visual Studio Code, and Git**
- **Anaconda:**
  - Download Anaconda from the [official website](https://www.anaconda.com/products/individual#windows).
  - Install Anaconda by following the instructions. It includes Python and Jupyter.

- **Visual Studio Code (VS Code):**
  - Download and install VS Code from [here](https://code.visualstudio.com/).
  - In VS Code, install the Python extension available in the Extensions marketplace.

- or **Cursor.ai  (Cursor):**
  - Download and install Cursor.ai from [here](https://www.cursor.com).
  - In Cursor, install the Python extension available in the Extensions marketplace.

- **Git:**
  - Download and install Git for Windows from [Git's official site](https://git-scm.com/download/win).

### 2. **Clone the ELMED219-2025 Repository**
- Open Git Bash or the terminal.
- Navigate to the directory where you want the repository.
- Clone the repository:
  ```bash
  git clone https://github.com/MMIV-ML/ELMED219-2025.git
  ```

### 3. **Set Up the Conda Environment from the "environment.yml"**
- Open Anaconda Prompt.
- Navigate to the cloned repository's directory.
- Create the `elmed219-2025` environment from the `environment.yml` file:
  ```bash
  conda env create -f environment.yml
  ```
- Activate the `elmed219-2025` environment:
  ```bash
  conda activate elmed219-2025
  ```

### 4. **Using Jupyter Notebooks via Anaconda**
- With the `elmed219-2025` environment active, launch Jupyter Notebook:
  ```bash
  jupyter notebook
  ```
- Jupyter will open in your web browser, where you can access and run notebooks.

### 5. **Working with Jupyter in Visual Studio Code (or, Cursor)**
- Open VS Code (Cursor)
- Open the folder containing the cloned ELMED219-2025 repository.
- Make sure to select the `elmed219-2025` environment in VS Code (or Cursor).
- Open or create Jupyter notebook files (`.ipynb`) within VS Code (or Cursor).

### 6. **Experimenting with Your Own Notebooks**
- Within the cloned repository, create a new folder, e.g., `MyNotebooks`, for your experiments.
- Make sure to add `MyNotebooks/` to the `.gitignore` file to avoid conflicts with the original repository.
- Develop and test your notebooks in this folder, using the `elmed219-2025` environment.

### 7. **Manage Changes without Affecting the Original Repository**
- Regularly pull updates from the original ELMED219-2025 repository to stay updated.
- For your work in `MyNotebooks`, you can either:
  - Use Git to manage and track changes.
  - Or, if you prefer not to use Git for personal experiments, just save your work locally.

### 8. **Additional Tips**
- **Familiarize Yourself with Tools:** Explore Anaconda, VS Code (Cursor), and Git functionalities.
- **Backup Your Work:** Consider other backup options for your `MyNotebooks` folder.

This setup should provide a robust environment for working with the ELMED219-2025 course materials while enabling you to experiment in a separate space without affecting the original repository. If you encounter any issues or have further questions, feel free to ask for assistance. Happy coding!


<img src="./assets/You.png" width="100"> <br>
_Can you help me with using the corresponding command line in **Windows** to work with the course material locally, using VS Code, and Git ? Please give me details on how to start  and stop the command line (shell), and explain to me the use of important command line commands to navigate, manipulate, and display files and directories on my disk._


<img src="./assets/GPT-MedAI.png" width="370"> <br>

Certainly! Using the command line (shell) in Windows to work with course materials, especially with tools like Visual Studio Code (VS Code) and Git, can enhance your workflow significantly. Here's a detailed guide:

### Starting and Stopping the Command Line (Shell)
- **To Start:**
  - Press `Win + R`, type `cmd`, and press `Enter` to open the Command Prompt.
  - Alternatively, you can search for "Command Prompt" in the start menu.
  - For Git-specific commands, you can use Git Bash, which comes with Git for Windows. You can start it the same way as Command Prompt, by searching for "Git Bash".

- **To Stop:**
  - Simply type `exit` and press `Enter`, or just close the window.

### Basic Command Line Commands
- **`cd [directory]`** (Change Directory): Changes the current directory.
  - Example: `cd Documents` changes the current directory to `Documents`.

- **`dir`** (List Directory Contents in Command Prompt) or **`ls`** (in Git Bash): Lists the files and folders in the current directory.
  - Example: `dir` or `ls` will display a list of files and folders in the current directory.

- **`mkdir [folder_name]`** (Make Directory): Creates a new folder.
  - Example: `mkdir NewFolder` creates a new folder named `NewFolder`.

- **`del [file]`** (Delete File) or **`rm [file]`** (in Git Bash): Deletes a file.
  - Example: `del example.txt` or `rm example.txt` deletes the file named `example.txt`.

- **`rmdir [folder]`** or **`rm -r [folder]`** (in Git Bash) (Remove Directory): Removes a folder.
  - Example: `rmdir OldFolder` or `rm -r OldFolder` removes the folder named `OldFolder`.

### Working with Git in the Command Line
- **Cloning a Repository:**
  - Use `git clone [repository URL]` to clone a repository.
  - Example: `git clone https://github.com/MMIV-ML/ELMED219-2025.git` clones the ELMED219 repository.

- **Checking the Status:**
  - `git status` shows the status of changes as untracked, modified, or staged.

- **Adding Changes:**
  - `git add [file]` stages a file for commit.
  - `git add .` stages all changes.

- **Committing Changes:**
  - `git commit -m "[commit message]"` commits the staged changes with a message.

- **Pulling Updates:**
  - `git pull` fetches and merges updates from the remote repository.

- **Pushing Changes:**
  - `git push` uploads local repository content to a remote repository.

### Using VS Code with Command Line
- **Opening VS Code:**
  - Navigate to your project's directory using `cd`.
  - Type `code .` to open the current directory in VS Code.

### Integrating Command Line, VS Code, and Git
- Use the command line to navigate to your project directory and manage Git operations.
- Use VS Code for editing, running, and debugging your code. VS Code also has integrated Git support, which can be handy for committing and pushing changes without leaving the editor.

### Additional Tips
- **Tab Completion:** Press the `Tab` key while typing a command to auto-complete file and folder names.
- **Command History:** Use the `Up` and `Down` arrow keys to cycle through previously used commands.
- **Copying and Pasting:** Right-click to copy/paste in the Command Prompt or Git Bash.

Understanding and using these command line tools can greatly enhance your efficiency and capability in handling course materials and development tasks. If you have any specific questions or need further assistance, feel free to ask.



# Are you using Mac?
Then you must install [xcode](https://developer.apple.com/xcode/resources) (for free) before you start. Thereafter (see also [here](https://stackoverflow.com/questions/9329243/how-to-install-xcode-command-line-tools)):


- Launch the `terminal.app`, found in /Applications/Utilities/
- Type the following command string: `xcode-select --install`

<img src="./assets/You.png" width="100"> <br>
_How to set up and use GitHub and Jupyter notebooks on **Mac**, by (i) using Anaconda,  (ii) using Visual Studio Code (or, Cursor), (iii)  initially cloning the ELMED219-2025 course repository, (iv) activate its conda environment  "elmed219-2025 " as specified in "environment.yml" , and (v) being able to experiment with my own notebooks (making a local copy) in this environment without getting in conflict with the original repository?_



<img src="./assets/GPT-MedAI.png" width="370"> <br>
Setting up and using GitHub and Jupyter notebooks on a Mac, particularly for working with the ELMED219 course materials using Anaconda and Visual Studio Code, involves a series of steps. Here's a detailed guide to help you through the process:

### 1. **Install Anaconda, Visual Studio Code (or, Cursor), and Git**
- **Anaconda:**
  - Download Anaconda for Mac from the [Anaconda website](https://www.anaconda.com/products/individual).
  - Open the downloaded file and follow the installation instructions.

- **Visual Studio Code (VS Code):**
  - Download VS Code for Mac from the [Visual Studio Code website](https://code.visualstudio.com).
  - Open the downloaded file and drag the VS Code icon to the Applications folder.

- **Cursor.ai (Cursor):**
  - Download Cursor for Mac from the [Cursor website](https://www.cursor.com).
  - Open the downloaded file and drag the Cursor icon to the Applications folder.

- **Git:**
  - Git usually comes pre-installed on Mac. To check, open Terminal and type `git --version`.
  - If not installed, you can install it via [Homebrew](https://brew.sh) (a package manager for Mac) by running `brew install git` in the Terminal.

### 2. **Clone the ELMED219-2025 Repository**
- Open Terminal.
- Navigate to the directory where you want to clone the repository, e.g., `cd ~/Documents`.
- Clone the repository:
  ```bash
  git clone https://github.com/MMIV-ML/ELMED219-2025.git
  ```
- Move into the cloned directory: `cd ELMED219-2025`.

### 3. **Set Up and Activate the Conda Environment**
- Ensure Anaconda is properly installed by typing `conda --version` in Terminal.
- In the ELMED219 directory, create the `elmed219` environment using the `environment.yml` file:
  ```bash
  conda env create -f environment.yml
  ```
- Activate the `elmed219-2025` environment:
  ```bash
  conda activate elmed219-2025
  ```

### 4. **Using Jupyter Notebooks via Anaconda**
- With the `elmed219-2025` environment active, start Jupyter Notebook:
  ```bash
  jupyter notebook
  ```
- This will open Jupyter in your default web browser, where you can access and run the course notebooks.

### 5. **Working with Jupyter in Visual Studio Code**
- Open VS Code.
- Open the folder containing the ELMED219-2025 repository by going to "File" > "Open...".
- Ensure the `elmed219-2025` environment is selected in VS Code (visible in the bottom left corner or the Python extension tab).
- Open or create Jupyter notebook files (`.ipynb`) within VS Code.

### 6. **Experimenting with Your Own Notebooks**
- Inside the ELMED219-2025 directory, create a new folder, say `MyNotebooks`, for your personal experiments.
- Add this folder to the `.gitignore` file (create one if it doesn't exist) to prevent conflicts with the original repository.
- Work on your notebooks within this folder using the `elmed219-2025` environment.

### 7. **Manage Changes without Affecting the Original Repository**
- Regularly pull updates from the ELMED219-2025 repository to stay updated:
  ```bash
  git pull origin main
  ```
- Manage your work in `MyNotebooks` separately, ensuring not to track these files in Git if they're included in `.gitignore`.

### 8. **Additional Tips**
- Familiarize yourself with Terminal commands for navigating and managing files.
- Backup your work regularly, especially the contents of `MyNotebooks`.

Following these steps, you should be able to work with the ELMED219 course materials using Jupyter notebooks, manage the course materials via Git, and experiment with your own notebooks in a managed environment. If you encounter any issues or need further assistance, feel free to reach out for help.

<img src="./assets/You.png" width="100"> <br>
_Can you help me with using the corresponding command line in **MacOS** to work with the course material locally, using Cursor, and Git ? Please give me details on how to start  and stop the command line (shell), and explain to me the use of important command line commands to navigate, manipulate, and display files and directories on my disk._


<img src="./assets/GPT-MedAI.png" width="370"> <br>
Certainly! Working with course materials locally on macOS using the command line (shell), Visual Studio Code (VS Code), and Git involves a combination of terminal commands and applications. Here's a detailed guide:

### Starting and Stopping the Terminal (Shell)
- **To Start:**
  - You can find the Terminal application in the `Applications` folder, under `Utilities`, or use Spotlight (`Cmd + Space`) to search for "Terminal."
  - Open the Terminal app to start the command line interface.

- **To Stop:**
  - You can exit the Terminal by typing `exit` and pressing `Enter`. Alternatively, you can just close the Terminal window.

### Basic Command Line Commands
- **`cd [directory]`** (Change Directory): Changes the current directory.
  - Example: `cd Documents` moves you to the Documents directory.

- **`ls`** (List Directory Contents): Lists the files and folders in the current directory.
  - Example: `ls` displays a list of files and folders in the current directory.

- **`mkdir [folder_name]`** (Make Directory): Creates a new folder.
  - Example: `mkdir NewFolder` creates a new folder named `NewFolder`.

- **`rm [file]`** (Remove File): Deletes a file.
  - Example: `rm example.txt` deletes the file named `example.txt`.

- **`rm -r [folder]`** (Remove Directory): Deletes a folder and its contents.
  - Example: `rm -r OldFolder` removes the folder named `OldFolder`.

- **`open [file]`** (Open File): Opens a file with its default application.
  - Example: `open example.txt` opens the file `example.txt` in the default text editor.

- **`open -a [application] [file]`** (Open File with Application): Opens a file with a specified application.
  - Example: `open -a TextEdit example.txt` opens `example.txt` with TextEdit.

### Working with Git in the Terminal
- **Cloning a Repository:**
  - Use `git clone [repository URL]` to clone a repository.
  - Example: `git clone https://github.com/MMIV-ML/ELMED219.git` clones the ELMED219 repository.

- **Checking Status:**
  - `git status` shows the status of changes in the current repository.

- **Adding Changes:**
  - `git add [file]` stages a file for commit.
  - `git add .` stages all current changes.

- **Committing Changes:**
  - `git commit -m "[commit message]"` commits the staged changes with a message.

- **Pulling and Pushing Changes:**
  - `git pull` fetches and merges updates from the remote repository.
  - `git push` uploads your local repository content to a remote repository.

### Using Visual Studio Code with the Command Line
- **Opening VS Code:**
  - Navigate to your project's directory using `cd`.
  - Type `code .` to open the current directory in VS Code.

### Integrating Command Line, VS Code, and Git
- Use the Terminal for navigating to your project directory and managing Git operations.
- Use VS Code for editing, running, and debugging your code. VS Code has integrated Git support, which is handy for version control.

### Additional Tips
- **Tab Completion:** In the Terminal, you can start typing a command or file name and press `Tab` to auto-complete it.
- **Command History:** Use the `Up` and `Down` arrow keys to cycle through previously used commands.
- **Copying and Pasting:** Use `Cmd + C` to copy and `Cmd + V` to paste in the Terminal.

By combining these command-line skills with VS Code and Git, you'll have a powerful setup for managing and working on the ELMED219 course materials. If you have any specific questions or need further assistance, feel free to ask.

# Are you using Linux?
Then you are likely familiar with the command line (shell) and can modify the installation procedures described for MacOS. 



# Notes on the command line (shell) and notebooks: 

#### On Mac, Windows and Linux we will use the [command line](https://en.wikipedia.org/wiki/Command-line_interface#Command-line_interpreter) (shell)
See e.g. [Basic Unix Commands](https://people.duke.edu/~ccc14/pcfb/unix.html) and [Computing Skills for Biologists](https://computingskillsforbiologists.com) [[here](https://github.com/CSB-book/CSB)] if this is unfamiliar to you. See also the
[Unix Shell](http://swcarpentry.github.io/shell-novice) lessons (thanks to [Anne Fouilloux](https://www.mn.uio.no/geo/english/people/adm/annefou), UiO)

#### ... and luckily also the [Jupyter notebook](https://www.nature.com/articles/d41586-018-07196-1)
- for openness [!](https://www.nature.com/news/interactive-notebooks-sharing-the-code-1.16261) and reproduciblity [!](https://arxiv.org/pdf/1810.08055.pdf)

# Notes on GitHub:
The course code is hosted on the code-sharing platform GitHub (where you now are reading this). If you do not have a GitHub account already you should make one now (https://github.com/join). We recommend that you are using the platform for your own projects during the course. Hence:


- Create an account on GitHub (https://github.com) using the `Sign up for GitHub` form on the right side of the page.
- Send your GitHub username to your instructor.
- Once your instructor adds you to the course GitHub organization you will receive an email asking you to accept the invitation. Click on the link to accept.
- Check if this worked
  - Go to https://github.com.
  - Sign in if necessary.
  - In the upper left corner click on the drop down with your name.
  - Confirm that the name of the course GitHub organization is present

# Notes on Anaconda:
We recommend installing Python via the [Anaconda Distribution](https://www.anaconda.com/download). Be sure to use the "Python 3.11.x" version. We will use the Conda Package Management System within the Anaconda Distribution. From the [documentation](https://conda.io/docs):
> Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux. Conda quickly installs, runs and updates packages and their dependencies. Conda easily creates, saves, loads and switches between environments on your local computer.

After the installation run `python --version` in a terminal window (e.g. in "Anaconda Prompt" if you are using Windows). If the output show "Python 3.11.x" (and "Anaconda") you are good to go.


# Notes on Colab:
Alternatively, some of the Jupyter notebooks in the Labs can be executed on **Google Colaboratory**. Colaboratory, or “Colab” for short, is a product from Google Research. Colab allows anybody to write and execute arbitrary python code through the browser, and is especially well suited to machine learning, data analysis and education. More technically, Colab is a hosted Jupyter notebook service that requires no setup to use, while providing free access to computing resources including GPUs. Colab is free to use, and resources are not guaranteed and not unlimited, and the usage [resource limits](https://research.google.com/colaboratory/faq.html#resource-limits) sometimes fluctuate.

Colab ode is executed in a virtual machine private to your account, i.e.

> you will need to [Create a Google Account](https://support.google.com/accounts/answer/27441?hl=en) if you not already have one (you don't need a Gmail account to create a Google Account as you can use your non-Gmail address).

Virtual machines are deleted when idle for a while, and have a maximum lifetime enforced by the Colab service.

Colab notebooks are stored in [Google Drive](https://drive.google.com/drive/my-drive), or can be loaded from [GitHub](https://github.com). Colab notebooks can be shared just as you would with Google Docs or Sheets. Simply click the Share button at the top right of any Colab notebook, or follow these Google Drive [file sharing instructions](https://support.google.com/drive/answer/2494822?co=GENIE.Platform%3DDesktop&hl=en).

<img src="./assets/You.png" width="100"> <br>
_I prefer to use COLAB in the course. Please provide information about colab and how to proceed. What about using my own notebooks and data?_

<img src="./assets/GPT-MedAI.png" width="370"> <br>
Using Google Colab (short for Colaboratory) is a great choice for working on the ELMED219 course, especially if you prefer an environment that doesn't require local setup for Python and Jupyter Notebooks. Here's an overview and guidance on how to use Google Colab, including working with your own notebooks and data.

## What is Google Colab?
- **Overview:** Google Colab is a free, cloud-based service that provides a Jupyter notebook environment. It allows you to write and execute Python in your browser, with zero configuration required, free access to GPUs, and easy sharing.
- **Benefits:**
  - No setup: Run notebooks with no installation required.
  - Free access to GPUs: Useful for machine learning tasks.
  - Easy sharing: Just like Google Docs, you can share your Colab notebooks with others.
- **Environment:** Colab runs notebooks on Google Cloud, meaning you can leverage their hardware (including GPUs and TPUs) and save your work on Google Drive.

## Getting Started with Google Colab
1. **Access Colab:**
   - Visit [Google Colab](https://colab.research.google.com/).
   - You'll need a Google account to use Colab.

2. **Create a New Notebook:**
   - Click on `New Notebook` to create a new notebook.
   - Alternatively, you can go to `File` > `Open notebook` to open existing notebooks from Google Drive, GitHub, or upload from your computer.

3. **Interface Familiarization:**
   - The interface is similar to Jupyter Notebook. It has a menu bar, a toolbar, and cells where you can write and execute code or add text.

## Using Your Own Notebooks and Data
- **Uploading Notebooks:**
  - You can upload your Jupyter notebooks (`.ipynb` files) directly to Colab from your local machine or integrate with GitHub to load notebooks.

- **Using Data:**
  - **From Local Machine:** You can upload files from your local machine using:
    ```python
    from google.colab import files
    uploaded = files.upload()
    ```
  - **From Google Drive:** Mount your Google Drive to access files stored there:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
    This allows you to access files stored in Google Drive directly from your Colab notebooks.
  - **From External Sources:** You can also download data from external sources directly to Colab using `!wget [URL]` command or Python's requests library.

## Running Code
- **Execute Cells:** Click the play button on the left of the code cell or use `Shift + Enter` to run the code.
- **GPU/TPU Access:** For tasks requiring heavy computation, you can access GPUs/TPUs by going to `Runtime` > `Change runtime type` and selecting your preferred hardware accelerator.

## Saving and Sharing Work
- **Auto-save:** Colab automatically saves your notebooks to your Google Drive.
- **Sharing:** Share your notebooks just like a Google Doc by clicking the `Share` button and adding collaborators.

## Additional Features
- **Version Control:** Colab supports version history, allowing you to see previous versions of your notebook.
- **Collaboration:** Multiple people can work on a notebook simultaneously, just like Google Docs.

## Tips for Using Colab in Your Course
- **Regular Backups:** While Colab auto-saves to Drive, it's a good practice to keep local backups of important notebooks.
- **Internet Dependency:** Since Colab is cloud-based, you'll need a stable internet connection to use it.
- **Session Limits:** Be aware that Colab sessions are limited (runtime and GPU usage), and you might lose your session if you're inactive for too long or exceed usage limits.

Google Colab is an efficient and powerful tool for working on machine learning and data science projects, making it suitable for your ELMED219 course. It allows you to focus on learning and coding without worrying about your local environment setup. If you have specific needs or run into any issues, feel free to seek further assistance.

# Install and test your course environment

After you have successfully installed Anaconda, Git, VS Code, and cloned the ELMED219 corse repository (see above): 

## Test your installation:
Inspect and run the notebook [`00-test-installation.ipynb`](https://nbviewer.jupyter.org/github/MMIV-ML/ELMED219/blob/main/Lab1-mpMRI-glioblastoma/Lab-optional-imaging/00-test-installation.ipynb) in the `Lab1-mpMRI-glioblastoma/Lab-optional-imaging` directory:
```bash
cd Lab1-mpMRI-glioblastoma/Lab-optional-imaging
jupyter notebook  (or, jupyter lab, or, code . )
```


## Update:
The code and environment will be updated during the course. Run the following commands regularly:
* Update code: `git pull`
* Update environment:
```bash
conda activate elmed219-2025
conda env update
```

# Unix Shell

Learners need to understand what files and directories are and what a working directory is. These concepts are covered in the
[Unix Shell](http://swcarpentry.github.io/shell-novice) lessons (thanks to [Anne Fouilloux](https://www.mn.uio.no/geo/english/people/adm/annefou), UiO)

# Programming with Python

The best way to learn how to program is to do something useful, so [this](http://swcarpentry.github.io/python-novice-inflammation) introduction to Python is built around a common scientific task: **data analysis** ("... _we are studying inflammation in patients who have been given a new treatment for arthritis, and need to analyze the first dozen data sets of their daily inflammation_ ..."); see also [here](https://github.com/swcarpentry/python-novice-inflammation).


# A note on R (tip for previous R users)

**It is possible to run R-scripts in Jupyter notebooks**  (Jupyter = Julia, Python and R).

If you want to continue working with R (*not part of this course*) you should:

- Be using the latest R version (https://www.r-project.org) and the RStudio Desktop [[download](https://rstudio.com/products/rstudio/download)] for your Windows, MacOS or Linux system.
- **Install the R kernel** by opening an R console and then follow the instructions at https://irkernel.github.io/installation
- Necessary (or new) R libraries should be installed via RStudio and the corresponding R environment.
- See also [here](https://datatofish.com/r-jupyter-notebook) and [here](https://developers.refinitiv.com/article/setup-jupyter-notebook-r).
- The [rpy2](https://github.com/rpy2/rpy2) interface to use R form Python is also possible (but can be a bit more messy).
