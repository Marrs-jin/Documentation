# Necessary scripts

##Codes
All the codes can be found at <pre><code><https://github.com/Marrs-jin/WebDesign2> </pre></code>

To generate the HTML files for "transition rates" and "matrix elements" pages for a single element, the only code that will be run by the user is TransitionManualInput.py. This code pulls in several other codes as it is running.

To generate the HTML file for the "other data" page for a single element, the only code that will be run by the user is OtherData.py. This code pulls in several other codes as it is running.

To generate the HTML files for "transition rates", "matrix elements", and "other data" pages for all elements, the only code that will be run by the user is Master1.py. This code pulls in several other codes as it is running.

A full list of all Python scripts that will be needed for the functionality of making any HTML page is provided below.
Necessary scripts:
<ul>
<li>TransitionManualInput.py</li>
<li>modsigfig.py</li>
<li>To_HTML_CSV.py</li>
<li>OtherData.py</li>
<li>LoadInElement.py</li>
<li>LoadFunctions.py</li>
<li>Format_save_copy.py</li>
<li>Master1.py</li>
</ul>

Running these codes is possible through the Ipython command in the command line, e.g. <pre><code>ipython TransitionManualInput.py</pre></code>  

Users also have the option to run codes using the Jupyter Notebook interactive environment. In this case the files have the same names but the extension .ipynb replaces .py. For example
"TransitionManualInput.ipynb".

These codes are run after entering the Jupyter shell through the <pre><code>jupyter notebook</pre></code>  command, navigating to the script you wish to run, and running all cells. See the examples
for more information.
