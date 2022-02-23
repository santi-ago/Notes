# **Virtual environments**

- Why?

Because projects should have their own packages separated from each other due to compatibility issues.

## How to setup a Virtual Environment with virtualenv and pip.

- Installation
 
First we need to check whether or not the package is installed with `pip show virtualenv`. To install it you use `pip install virtualenv`.

- Creation

If Windows you need to manually [download](https://www.python.org/downloads/windows/) the version you want and make sure you don't add the new installed Python to the Path but do remember where it is.

Once you have installed your version you'll need to type the following to create a new virtual environment:

    virtualenv PATH\<env_name> -p PATH_VERSION\python.exe

    virtualenv D:\Universidad\PDI\PDI_venv -p C:\Users\Santiago\AppData\Local\Programs\Python\Python39\python.exe`
Where PATH is the folder you want your environment and PATH_VERSION is the location fo your newly installed Python.

For the sake of this notes we are going to use the name of the new environment as Notes.

- Activation

        Notes\Scripts\Activate.bat

Once you've run that line on your terminal, you'll notice the name of the environment in parenthesis, also you can type `where python` it gives us the paths to the current python command and our virtual environment directory is listed at the top.

To deactivate you type `deactivate`

- Installing packages to your new environment

Now that the environment is set, you can install the packages you want for your project with the `pip` command and add the packages you want, you can even install multiple libraries at the same time, just make sure to keep an space between them.

    pip install numpy matplotlib opencv-python torch torchvision

- Installing packages from requirements.txt

        pip install -r requirements.txt


- Deleting an environment

Just need to deactivate and delete the directory.

    rmdir PATH /s

## How to setup a Virtual Environment with Conda.

- After you install Conda open the prompt

        conda create -n yourenvname python=x.x

were `x.x` means the version you want

To activate this environment, use
  
    conda activate PDIenv

To deactivate an active environment, use

    conda deactivate

### Install additional Python packages to a virtual environment.

    conda install -n yourenvname packages

    conda install -n PDIenv numpy matplotlib opencv-python pandas pytorch torchvision torchaudio cpuonly -c pytorch

 