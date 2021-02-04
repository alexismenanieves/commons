## Setting up a Python Environment

It is possible to set up an environment using Conda and a yaml file. In this way, you don't have to install libraries and dependencies one by one. You need to:

-   Install Anaconda or Miniconda

-   Create a libraries and dependencies file

-   Create the environment

### Install Anaconda (or Miniconda)

Download Anaconda installer from <https://www.anaconda.com/products/individual>, this will install Conda and other programs like Spyder. If you want a lightweight version of Conda, then go to this page: <https://docs.conda.io/en/latest/miniconda.html> where you can download Miniconda.

### Create a libraries and dependencies file

You can create a yaml file (which is basically a text file) and specify the libraries and dependencies you want in your environment. Firstly the name of your environment. Secondly the dependencies, basically python (in the version you want), numpy, matplotlib, and dlib (which includes the basic linear algebra libraries that I use every day). Then pip lets you install the libraries of your preference, in my case turicreate, streamlit, cmake and of course notebook (for Jupyter).

Let me show the structure:

name:

dependencies:

pip:

In this repository you'll find an example of a yaml. Sometimes the version of the dependencies are not compatible and you'll have to try different versions. In this case I am using one that Jonathan Fernandes <https://www.linkedin.com/in/jonathanafernandes/> uses in his courses on LinkedIn. He is a great instructor, you may give it a try.

### Create the environment

Let's create an environment named "ocv4". First create a directory and place the yaml file (in my case ocv4.yml) and go to that directory. Make sure you don't have that environment created by typing on the terminal (for Mac or Linux):

conda env remove -n ocv4

Then, create the environment with this command:

conda env create -f ocv4.yml

You'll have to wait for all the files to download from internet. The more dependencies you list, the longer it takes to install.

When all the installation is done, activate the environment using:

conda activate ocv4
