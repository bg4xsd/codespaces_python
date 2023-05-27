# Data Analysis Environment 2023

For python=3.9 or 3.10

For "image": "mcr.microsoft.com/devcontainers/universal:2", jupyter and pytorch are ready to work. For Python plus R enviroment, build from here. It contains Python, Java, C compiler.

For "image": "mcr.microsoft.com/devcontainers/python:3.10", it's a smaller and faster image with a blank, clear pip environment only. No conda. Install your packages by yourself.

## 1. Basic packages for data science and data analysis

pip install scipy numpy matplotlib pandas jupyter notebook  jupyterlab ipython scikit-learn statsmodels patsy seaborn beautifulsoup4 simplejson bokeh psutil  pylint flake8 yapf autopep8 black requests lxml astropy scikit-learn-intelex ipykernel plotly pyecharts -i https://mirrors.cloud.tencent.com/pypi/simple

### pip default source

 https://pypi.org/simple

## 2. Time series packages

 pip install nolds pynamical PyRQA pyts hundun
 
 pip install  AutoTS Sktime tsfresh

### install torch，then fastai,  at last tsai

### pytorch for cpu

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu  # torch CPU latest version

or

pip install torch==1.13.1+cpu torchvision==0.14.1+cpu torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cpu

### fastai 

pip install fastai

### tsai

pip install tsai

### prophet

pip install -U Prophet -i https://pypi.org/simple

## 3. Install R with conda, last update 2023.05
   If you have several conda virtual env, make sure that above install steps and below steps are proceeding in the same conda virtual env.
   
   If conda throw error messages for broken install procedure, use cmd conda clean --all  to clean the virtual env, then install again.

1. install r-base
   
   conda install -c conda-forge r-base==4.2.3 # force to certain version, check the channel often
 
2. conda install -c conda-forge r-essentials r-stringi r-irkernel r-devtools 
3. Start R, and run cmd:  IRkernel::installspec()
4. conda install -c conda-forge r-tidyverse r-tidymodels r-mlr3 r-mlr3verse r-rio r-bench rpy2 # add more R packages

### optional
5. conda install -c conda-forge gluonts r-prophet # TSA
6. Start R, and run cmd:  install.packages(c('tseriesChaos', 'nonlinearTseries', 'fNonlinear', 'DChaos'))  $ TSA
### Others， maybe not update often, add by yourself. Note to remember.
7. Start R, and run cmd:  install.packages(c('GGally', 'patchwork','precrec')) 
   
## Save spaces of codespace

pip cache purge      

conda clean --all

## 4. How to import/export the Python environment 
   For python env, conda and pip can work togther, but they managed the package separately, you have to import/export the evn for each of them. Obviously, if you use conda and pip at the same time, you should do conda management before pip's working. 
   
   For Github codespaces, try to use conda base environment, if you want to create new conda virtual env, DO NOT use conda command to install the new virtual env into /opt/conda directory, the Jupyter can not recoginize it, follow the command by click choosing kernel,...create new env...conda..., then the new conda env will be created under current project directory, in .conda directory, which can work well.
   
   For cloudstudio, try by yourself.
   
   For most situations, pip is OK for data analysis and machine learning. Especially, for building a complex working environment, like Python-R mixed system, or some packages pre-compiled in conda-forge only, you have to use conda. For linux,  you can build most of the packages by yourself and the C compiler is more useful.
   
### export python packages

pip list freeze > requestment.txt # You can export the packages list of current working environment,  and others can build the same env.

pip list freeze > requestment.txt # Use this, without path, with version number, it's OK

### install python packages
pip install –r requestment.txt

### uninstall python packages
pip uinstall –r requestment.txt

### sometimes, you use conda install some packages, and you have to use conda do the export/import work

conda env export > da310.yaml  # try to choose the file name same to the envrionment, for easy remember.

conda env create -f da310.yaml  # the conda virtual env's name is contained in the yaml file. Let others build the same env.

## 5. Install some system packages, for Ubuntu only
Some times, your docker image or new system will miss some packages for developing, you have to install them, and below cmd is useful, you can add your own note below for certain developing system.

(1) sudo apt update  # update the apt repository

(2) sudo apt install build-essential gdb # install C compiler and neccesary libs

(3) sudo apt install htop  # view the cpu and memory usage, you can install the ubuntu libs like this by yourself.

## 6. Conclusion
Forming good habits to write note for your project, add notes to your code for making them legible. 

--------------
Last update by Dr. Cat (BG4XSD) @ 2023.05.27
