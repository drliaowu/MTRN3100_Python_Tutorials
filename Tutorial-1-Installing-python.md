# Tutorial 1: Installing Python

## Aim

This tutorial lists the necessary steps of installing python through anaconda, setting up conda virtual environment and installing required packages.

## Step 1: Installing Anaconda
For the vision part,  we recommend using the free Anaconda Python distribution, which provides an easy way for you to handle 
package dependencies.

### Windows:

Download .exe [file](https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe) and install it.

### Mac :

Download .pkg [file](https://repo.anaconda.com/archive/Anaconda3-2021.05-MacOSX-x86_64.pkg) and install it.

### Ubuntu:

Follow the installation instructions on [web](https://docs.anaconda.com/anaconda/install/linux/).

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

### Mac/Ubuntu:

To set up a virtual environment, open a Terminal and run
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

## Step 3: Installing Dependencies
First activate the virtual envinroment 'mtrn4110' using the method mentioned above
```
#run in Anaconda Prompt/Terminal
conda activate mtrn4110
```

Then check whether you are using the correct version of 'pip' by running

### Windows:
```
#run in Anaconda Prompt
pip --version
```
which will give you 'pip 21.1.3 from .....\Aanaconda3\envs\mtrn4110\lib\site-packages\pip (python 3.7)'

### Ubuntu/MAC:
```
#run in Terminal
which pip
```
which will give you '.../anaconda3/envs/mtrn4110/.../pip'

Next, install the required dependencies. You can do this with two options:

### Option 1:
Download the tutorial [project](https://github.com/drliaowu/MTRN4110_21T2_Python_Tutorials) containing the requirements.txt file, 'cd' to the project folder (.../MTRN4110_21T2_Python_Tutorials) and run (make sure the requirements.txt is in the current folder)

```
pip install -r requirements.txt
```

### Option 2:
Mannually install the required dependencies:
```
pip install matplotlib==3.2.2
pip install opencv-python==3.4.2.17
pip install opencv-contrib-python==3.4.2.17
pip install ipykernel==5.3.2
pip install notebook==6.4.0
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

Now you can type in ```exit()``` and press Enter to exit Python.

## Step 8: Jupyter Notebook

Jupter Notebook is a web application which contains live code, similar to live scripts in Matlab. This allows you to edit/run code in the browser and check the results of computations attached to the code which generated them. This is easier when your work needs a bit of fine-tunning. 

git clone the [repo](https://github.com/drliaowu/MTRN4110_21T2_Python_Tutorials) and change dir to the repo folder and run in Anaconda Prompt (Windows)/Terminal(Mac/Ubuntu)/ in the mtrn4110 environment

```
jupyter notebook
```
click the 'Tutorial-2-Variables-Boolean-and-Operators.ipynb', change the kernel to mtrn4110, and run each section.

If you want to quit jupyter notebook, you can close the page and type "cltr + c" in the Anaconda Prompt several times.

## Summary

Now you should have Python installed and be able to run python and jupyter notebook.
