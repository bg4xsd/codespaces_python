# GitHub Codespaces ♥️ Python with Jupyter Notebooks 

Welcome to your shiny new codespace! We've got everything fired up and running for you to explore Python and Jupyter notebooks.

You've got a blank canvas to work on from a git perspective as well. There's a single initial commit with what you're seeing right now - where you go from here is up to you!

Everything you do here is contained within this one codespace. There is no repository on GitHub yet. If and when you’re ready you can click "Publish Branch" and we’ll create your repository and push up your project. If you were just exploring then and have no further need for this code then you can simply delete your codespace and it's gone forever.

--------------- Added by BG4XSD -----------

It's forked from github/codespaces-jupyter, wonderful work.

1. Use this repo as a template for your repo, or download the code to your project. Be careful to the devcontainer.json and requirements.txt, keep the directory structure, they are useful.

2. Create a blank codespaces, and upload these two files onto the codespaces, keep the directory structure. The press Ctl+Shift+P, enter cmd : rebuild container. 

3. For a while, your codespace will be upgrade to your pointed environment.

4. In env_config_templete directory, there are some pre-defined configuration, Copy the necessary content to evcontainer.json and requirements.txt. ML stands for Machine Learning, NN is Neural Network, TS is Time Series analysis with some chaotic toolboxes.

5. Two devcontainer configuration files are tested well. xxxPython3.10.json can be pointed with certain version.
https://github.com/devcontainers/images pre-compiled a lot of docker images. https://github.com/microsoft/vscode-dev-containers/tree/main/containers is another repository. 

6. The default image contain pytorch2.0, use pip install -U xxx for newer version; or pip install xxx==x.x.x.

7. https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/setting-up-your-python-project-for-codespaces  is useful.

8. By now, only the original image is used, it's stable and fast. while the system is ready, install the packages by yourself. The install procedure is described in file env.md.

10. If you use "image": "mcr.microsoft.com/devcontainers/universal:2", you can start the python project with jupyter pytorch. If you want to build Python plus R environment, choose this image, if you want to choose different Python version, use conda or venv to create your own env.

11. If you choose "image": "mcr.microsoft.com/devcontainers/python:3.10", it's a smaller and faster image with a blank, clear pip environment only. No conda. 

----------
Last update: 2023.05.26 by BG4XSD
