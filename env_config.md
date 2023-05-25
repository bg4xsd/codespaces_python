# Data Analysis Environment 2023

For python=3.9 or 3.10

## Basic packages for data science and data analysis

pip install scipy numpy matplotlib pandas jupyter notebook  jupyterlab ipython scikit-learn statsmodels patsy seaborn beautifulsoup4 simplejson bokeh psutil  pylint flake8 yapf autopep8 black requests lxml astropy scikit-learn-intelex ipykernel plotly pyecharts -i https://mirrors.cloud.tencent.com/pypi/simple

### pip default source

 https://pypi.org/simple

## 时间序列包

 pip install nolds pynamical PyRQA pyts hundun
 pip install  AutoTS Sktime tsfresh

# 按照要求，先装torch， 再装fastai, 最后 tsai

## pytorch 安装， 没有 GPU的看清楚，

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu  # torch CPU latest version
or
pip install torch==1.13.1+cpu torchvision==0.14.1+cpu torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cpu

## fastai 安装

pip install fastai

## tsai

pip install tsai

## Prophet

pip install -U Prophet -i https://pypi.org/simple

## Install R with conda, last update 2023.05
1. install r-base
 conda install r-base   # install 4.2.0
 conda install -c conda-forge r-base==4.2.3 # force to certain version, check the channel often

2. conda install -c conda-forge r-essentials
3. conda install -c conda-forge r-stringi r-irkernel r-devtools 
4. Start R, and run cmd:  IRkernel::installspec()

## Save spaces of codespace

pip cache purge      

conda clean --all
