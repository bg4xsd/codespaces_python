# Data Analysis Environment 2023

For python=3.9 or 3.10

For "image": "mcr.microsoft.com/devcontainers/universal:2", jupyter and pytorch are ready to work. For Python plus R enviroment, build from here.

For "image": "mcr.microsoft.com/devcontainers/python:3.10", it's a smaller and faster image with a blank, clear pip environment only. No conda. Install your packages by yourself.

## Basic packages for data science and data analysis

pip install scipy numpy matplotlib pandas jupyter notebook  jupyterlab ipython scikit-learn statsmodels patsy seaborn beautifulsoup4 simplejson bokeh psutil  pylint flake8 yapf autopep8 black requests lxml astropy scikit-learn-intelex ipykernel plotly pyecharts -i https://mirrors.cloud.tencent.com/pypi/simple

### pip default source

 https://pypi.org/simple

## Time series packages

 pip install nolds pynamical PyRQA pyts hundun
 
 pip install  AutoTS Sktime tsfresh

## install torch，then fastai,  at last tsai

## pytorch for cpu

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu  # torch CPU latest version

or

pip install torch==1.13.1+cpu torchvision==0.14.1+cpu torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cpu

## fastai 

pip install fastai

## tsai

pip install tsai

## Prophet

pip install -U Prophet -i https://pypi.org/simple

## Install R with conda, last update 2023.05

1. install r-base

   conda install r-base   # install 4.2.0
   
   conda install -c conda-forge r-base==4.2.3 # force to certain version, check the channel often
 
2. conda install -c conda-forge r-essentials r-stringi r-irkernel r-devtools 
3. Start R, and run cmd:  IRkernel::installspec()

## Save spaces of codespace

pip cache purge      

conda clean --all
