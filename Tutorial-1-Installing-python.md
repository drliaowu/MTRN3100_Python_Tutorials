# Tutorial 1: Installing Python

## Aim

This tutorial lists the necessary steps of installing python through anaconda, setting up conda virtual environment and installing required packages.

## Step 1: Installing Anaconda
For the vision part,  we recommend using the free Anaconda Python distribution, which provides an easy way for you to handle 
package dependencies.

### Windows:

Download .exe [file](https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe) and install it.

### MAC :

Download .pkg [file](https://repo.anaconda.com/archive/Anaconda3-2021.05-MacOSX-x86_64.pkg) and install it.

### Ubuntu:

```
wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh
chmod +x Anaconda3-2021.05-Linux-x86_64.sh
sudo ./Anaconda3-2021.05-Linux-x86_64.sh
export PATH=/home/$NAME/anaconda3/bin:$PATH^C
```

## Step 2: Anaconda Virtual Environment
Once you have Anaconda installed, it is highly recommended to create a virtual environment for the course.

If you use Python for different projects, they may require different versions of Python and/or other modules.
Creating a virtual environment will allow you to install specific versions of Python packages for the course project, without crashing with the dependencies of other projects.
For more details about what the virtual environment is and why it is highly recommended, you can refer to [this page](https://medium.com/@pinareceaktan/what-is-this-virtual-environments-in-python-and-why-anyone-ever-needs-them-7e3e682f9d2).

If you choose not to use a virtual environment, it is up to you to make sure that all dependencies for the code are installed globally on your machine.

### Windows:

To set up a virtual environment, open Anaconda Prompt and run
```
conda create -n mtrn4110 python=3.7.10

```
to create an environment called mtrn4110.

Then, to activate and enter the environment, run
```
conda activate mtrn4110
```
If you want to exit from the environment, you can simply close the window, or run

```
conda deactivate
```

### Ubuntu/Mac:

To set up a virtual environment, run (in a terminal)
```
conda create -n mtrn4110 python=3.7.10
```
to create an environment called mtrn4110.

Then, to activate and enter the environment, run
```
source activate mtrn4110
```
To exit, you can simply close the window, or run

```
source deactivate
```

## Step 3: Installing Dependencies
First activate the virtual envinroment 'mtrn4110' using the method mentioned above, and then check whether you are using the correct 'pip' by running

### Windows:
```
#run in Command Prompt
pip --version
```
which will give you 'pip 20.1.1 from .....\Aanaconda3\envs\mtrn4110\lib\site-packages\pip (python 3.7)'

### Ubuntu/MAC:
```
#run in terminal
which pip
```
which will give you '.../anaconda3/envs/mtrn4110/.../pip'

Next, install required dependecies. Download the tutorial [project](https://github.com/drliaowu/MTRN4110_20T2_Python_Tutorials) containing the requirements.txt file, 'cd' to the project folder (.../MTRN4110_20T2_Python_Tutorials) and run (make sure the requirements.txt is in the current folder)

```
pip install -r requirements.txt
```

## Step 4: Adding Virtual Environment to Jupyter Notebook
Add your virtual environment to Jupyter by typing:
```
python -m ipykernel install --user --name=mtrn4110
```

## Step 5: Running python

Type ```python``` or ``` python3 ```(If you have both python3 and python2) and press Enter. 

## Step 6: Test Opencv

Make sure python is started, then run
```
import cv2
cv2.__version__
```
which gives you '3.4.2'

## Step 7: Exit python

Now you can type ```exit()``` and press Enter to exit Python.

## Step 8: Jupyter Notebook

Jupter Notebook is a web application which contains live code, similar to live scripts in Matlab. This allows you to edit/run code in the browser and check the results of computations attached to the code which generated them. This is easier when your work needs a bit of fine-tunning. 

git clone the [repo](https://github.com/drliaowu/MTRN4110_20T2_Python_Tutorials) and change dir to the repo folder and run in terminal(Ubuntu/Mac)/Command Prompt(Windows) in the mtrn4110 environment

```
jupyter notebook
```
click the 'Tutorial-2-Variables-Boolean-and-Operators.ipynb' and run each section.

If you want to quit jupyter notebook, you can close the page and type "cltr + c" in the Command Prompt several times.

## Step 9: Run a python script

To manage a large codebase easily, you can choose your favoriate python IDEs based on [this](https://www.guru99.com/python-ide-code-editor.html). 

To run a python script, you can choose to run it in terminal(Ubuntu/Mac)/Command Prompt(Windows), change directory to the location of your python script, run
```
python [script_name].py
```
Or run it in the IDE.

## Summary

Now you should have Python installed and able to run python and jupyter notebook.
