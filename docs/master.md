# Usage guide
This guide shows users how to generate all the HTML pages at once (matrix elements, transition rates, all transition rates, other data).
Shown first is the version using only command line inputs, shown second is using Jupyter Notebook.

Note that the Master1 script has the list of elements it will run through. Modify the variable "element_list" if this needs to be changed.

## Python3
Open command prompt. Navigate to the directory with the functions and data folders. The image below shows an example of this directory on a local computer.

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/HTML_folder_location.PNG" alt="Directory to run code" width="600" >

See that all the scripts are in the current directory, and the "Data", "Experimental_Data" etc. folders are present.

Run the Master1.py script however you run Python scripts. Shown here is the IPython method, by typing in <pre><code>ipython Master1.py</pre></code>
into the command line.
See image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Run_master.PNG" alt="Directory to run code" width="600" >

A series of warning messages will display, the same as if an element was run individually. The code will automatically kill the run if
an error is encountered. Depending on the computer being used, this script will take approximately 9 minutes.

The HTML files will be saved into the "ElementsHTMLs" folder.

##Jupyter notebook  
The next steps assume Jupyter Notebook is installed.

Navigate to the directory with the functions and data folders. See the image for the Python3 section above.
Open Jupyter Notebook with the command <pre><code>jupyter notebook</pre></code>
Depending on user settings, a new tab will automatically open on their browser. If not, navigate to the URL provided (often localhost:8888) in a browser.  
The user may need to input a password they have created or use the token that was printed in the command line.  
The correct display is shown in the image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Jupyter_notebook.PNG" alt="Directory to run code" width="600" >

Navigate to the Master1.ipynb script and click to open it. At the top menu click on "Kernel", then "Restart and Run All". See image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Jupyter_Master.PNG" alt="Directory to run code" width="600" >

The HTML files will be saved into the "ElementsHTMLs" folder.
