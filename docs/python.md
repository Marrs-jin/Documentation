# Installation

## Python3
To run the code Python3 is needed. Users can download Python3 at <pre><code><https://www.python.org/downloads/></pre></code>

Once Python is installed, install IPython. IPython is a command shell for interactive Python computing. It can be downloaded
by opening the command prompt (for example on Windows by typing "cmd" in the search bar) and entering the command <pre><code>pip install ipython</pre></code>
Pip installations on Windows are by default done globably, so it does not matter in which directory you install it. If you are using a virtual machine
you will need to run this command at the location of where the codes are stored.

IPython is necessary to run the scripts if you do not wish to use Jupyter Notebook.
To run the HTML generation code you will need to be in the directory where the scripts and data folders are located.

Required libraries:
<ul>
<li>numpy</li>
<li>pandas</li>
<li>xlsxwriter</li>
<li>decimal</li>
<li>re</li>
<li>sympy (old)</li>
<li>sortedcontainers</li>
<li>warnings</li>
</ul>
Most of the required libraries come with Anaconda at <pre><code><https://www.anaconda.com/products/individual></pre></code>  

Otherwise, after Python installation run the command <pre><code>pip install [library]</pre></code> For example, "pip install pandas".
Pip is already installed if you are using a current version of Python.
##Jupyter notebook  
If you would prefer to use the Jupyter editor over command line prompts, you can download Jupyter Notebook at <pre><code><https://jupyter.org/install></pre></code>  

Jupyter notebooks are interactive coding environments allowing for instantaneous modification of specific blocks of code. They require an internet connection to run.

Jupyter is the environment in which all the code was written, so certain aspects of the files will be more intuitive if viewed in this editor.
It is why the .py files have lines like '# In[1]:' included: these were breaks in the Jupyter Notebook cell structure which do not impact the actual
running of the code. All code can be run in using only IPython and working in the command line however.

Also included are the .ipynb files, which are Jupyter Notebooks. If Jupyter Notebook is installed, these files can be open and run instead of the .py files.
