# Usage guide
This guide shows users how to generate the Other data (CsOther.html) HTML pages
using Cs as an example.Note that if you are running an ion use "BeII" format.  
Shown first is the version using only command line inputs, shown second is using Jupyter Notebook.

## Python3
Open command prompt. Navigate to the directory with the functions and data folders. The image below shows an example of this directory on a local computer.

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/HTML_folder_location.PNG" alt="Directory to run code" width="600" >

See that all the scripts are in the current directory, and the "Data", "Experimental_Data" etc. folders are present.

Run the OtherData.py script however you run Python scripts. Shown here is the IPython method, by typing in <pre><code>ipython OtherData.py</pre></code>
into the command line. Next there will be a prompt asking for the element to run. Type in using the format BaII, Cs, CaII, etc. Only one element can be run at a time.
See image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Run_Other.PNG" alt="Directory to run code" width="600" >

A series of warning messages will display (these are mostly pandas index caveat warnings), and a statement if there is or is not metastable data.  
See image below.

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Other_result.PNG" alt="Directory to run code" width="600" >

The HTML file will be saved into the "ElementsHTMLs" folder.

##Jupyter notebook  
Another method to run the code and receive the same results is through Jupyter Notebook. The next steps show how to use this method
instead of the method described above.
The next steps assume Jupyter Notebook is installed.

Navigate to the directory with the functions and data folders. This is the same directory as shown in the first image for the "Python3" method above.
Open Jupyter Notebook with the command <pre><code>jupyter notebook</pre></code>
Depending on user settings, a new tab will automatically open on their browser. If not, navigate to the URL provided (often localhost:8888) in a browser.  
The user may need to input a password they have created or use the token that was printed in the command line.  
The correct display is shown in the image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Jupyter_notebook.PNG" alt="Directory to run code" width="600" >

Navigate to the TransitionManualInput.ipynb script and click to open it. At the top menu click on "Kernel", then "Restart and Run All". See image below

<img src="https://raw.githubusercontent.com/Marrs-jin/Images/main/Jupyter_Other.PNG" alt="Directory to run code" width="600" >

At the prompt type in the element name, using the format BaII, Cs, CaII, etc.  
The HTML file will be saved into the "ElementsHTMLs" folder.
