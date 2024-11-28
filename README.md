# Scratch blocks to Python transpiler VM

This is a project for translating Scratch blocks and scripts to Python code. 
Specifically this repositroy contains the VM part of Scratch - running and maintaining state of Scratch blocks.

## Description

This VM repository is needed in order to run the GUI part. The GUI part of transpiler is located in [this repository](https://github.com/mh4043/scratch-blocks-to-python-transpiler-gui).
GUI repository contains more information about how the transpiler works.

## Installation

Because this is a local project, installation is required.
To run the project, you will also need a Scratch GUI from [this repository](https://github.com/mh4043/scratch-blocks-to-python-transpiler-gui).
How to connect these two repositores is described below.

### Prerequisites

- Installed Node version 20.12.2. or above
- Installed Python version 3.12.3. or above

### Installation steps

1. Open Node.js command prompt and make a folder where you will have both repositores.
2. In that folder, type the following command:
   ```bash
   git clone https://github.com/mh4043/scratch-blocks-to-python-transpiler-gui.git
   ```
   This creates a folder "scratch-blocks-to-python-transpiler-gui".
3. In the same folder, type the following command:
   ```bash
   git clone https://github.com/mh4043/scratch-blocks-to-python-transpiler-vm.git
   ```
   This creates a folder "scratch-blocks-to-python-transpiler-vm".
4. Go to folder "scratch-blocks-to-python-transpiler-vm" and type the following commands:
   ```bash
   npm install
   npm link
   ```
   This installs the packages and links the two folders together.
5. Go to folder "scratch-blocks-to-python-transpiler-gui" and type the following commands:
   ```bash
   npm install
   npm link scratch-vm
   ```
   This installs the packages and links the two folders together.
6. To run the server, run the following command:
   ```bash
   npm start
   ```
   This will start the server and print out the link to where the project is running.
   It is usually at "http://localhost:8601/" or "http://localhost:8602/". Copy this and paste it in browser.
   Now you should have a working local Scratch website with Python transpiler.
7. For the purposes of running the Python program in arbitrary IDE after translation, you should run the following command in folder "scratch-blocks-to-python-transpiler-gui".
   ```bash
   pip install -r python_transpiler_requirements.txt
   ```
   This installs the required libraries that Python uses.
    
For more information about setting up both repositories and troubleshooting, look at the original repositories from which these two were forked.
