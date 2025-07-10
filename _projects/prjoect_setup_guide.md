---
layout: page
title: Setting up a Scientific Python Project from Scratch
description: A guide to set up a scientific Python project from scratch, covering version control, virtual environments, and project structure.
category: software
date: 2025-10-07
---

# Setting up a Scientific Python Project from Scratch

This guide is intended as a resource for students and researchers who want to set up a scientific Python project from scratch. It will cover the basic steps to create a project structure that follows good coding practices, including version control, managing Python versions and virtual environments. It is by no means a comprehensive guide, but rather a starting point for your own projects.

It is mainly tested on Windows 10 and Linux. I aim to keep it updated with state-of-the-art tools and practices, but it might not always be up to date. If you find any issues or have suggestions for improvements, please feel free to contact me.

## Installations

1. Install git
    - [Git - Downloads](https://git-scm.com/downloads)
2. Install VSCode
    - [Visual Studio Code - Code Editing](https://code.visualstudio.com/)
3. Install pyenv
    - [pyenv - Simple Python version management](https://pyenv.net/)

## Accounts

- GitHub (connect your machine to GitHub via SSH [Connecting to GitHub with SSH - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh))

## Workflow

1. **Global Python setup**

    We will differentiate between the global Python setup, used to install basic tools like `cookiecutter` and `poetry`, but not for the project itself, and the project setup, which will be done in a virtual environment.

    ```bash
    # get a list of all available Python versions
    pyenv install --list
    # choose the version you want to install, e.g. 3.11.4. I would suggest using the latest stable version
    pyenv install 3.11.4 
    # set the global Python version
    pyenv global 3.11.4
    ```

    Now, we can install `poetry` to manage our virtual environments and dependencies, and `cookiecutter` to create pre-defined project structures.
    
    ```bash
    # install poetry
    pip install poetry
    # configure poetry to create virtual environments within the project folder
    poetry config virtualenvs.in-project true
    # install cookiecutter
    pip install cookiecutter
    ```

2. **Project setup**

    Now we can create a new project using `cookiecutter`. I like to use lightweight templates, such as the one I created. This will create a project structure that follows good coding practices.
    
    ```bash
    cookiecutter gh:RDoerfel/simple-cookiecutter
    ```
    
    Go through the initialization steps and create the project skeleton. cd into the project directory after its creation. You might as well use the `gh:patrickmineault/true-neutral-cookiecutter` template, or for larger projects, `gh:CBS-HPC/replication_package`. 
    
3. **Local Python setup**
    
    Once you have created the project structure with cookiecutter, we are ready to set up our local Python environment. First, install the Python version you want to use for the project. 
    
    ```bash
    # Again, have a look at all available Python versions and choose the one you need
    pyenv install --list
    # install the version you want to use, e.g. 3.11.4
    pyenv install 3.11.4
    # set the local Python version for the project
    pyenv local 3.11.4
    ```
    
    Now we can use `poetry` to manage our virtual environment and dependencies. Poetry will create a virtual environment within the project folder, which is a good practice to keep the project isolated from other projects and the global Python environment.

    ```bash
    # tell poetry to use the local Python version
    poetry env use $(pyenv which python)
    # initialize the poetry project
    poetry init 
    # install the project
    poetry install 
    # install packages
    poetry add numpy # this is how to install packages within the project
    ```
    
4. **Version Control**
    
    Initialize version control and connect it to GitHub. We first need to create a [new repository on GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository). Once you have done that, we can initialize git in the project directory and connect it to the remote repository.
    
    ```bash
    git init
    git remote add origin <your_github_repo>
    ```
    
    Open the `.gitignore` file. This is a file that excludes other files or directories from version control. We use this for data and environments, etc. 
    
    ```bash
    .venv/
    poetry.lock
    data/
    ```
    
    Once all the unwanted files and directories are excluded, stage everything, commit, and push as initial commit.
    
    ```bash
    git add --all
    git commit -m "initialize project"
    git push origin main
    ```

## Further guides

- [Remote development in VSCode using SSH](https://code.visualstudio.com/docs/remote/ssh-tutorial)
- [The Good Research Code Handbook — Good research code](https://goodresearch.dev/)
- [Russ Poldrack's substack and his chapters on Better Code Better Science](https://russpoldrack.substack.com/)