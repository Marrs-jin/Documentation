# Location
Data are generated through a variety of sources and stored in several folders. These folders are located in the same directory that all the Python scripts are saved at.

## Subdirectories for data used
All data folders need to be in the same directory as the codes are. The folders at this level are:
<ul>
<li>Data</li>
<li>ElementsHTMLS</li>
<li>Experimental_Data</li>
<li>Format_csvs</li>
<li>OtherData</li>
</ul>

**Data** stores the energy values and matrix elements used to calculate the transition rates for every element. Specific data for each element are
stored in a subdirectory in Data named after the element, for example "Data/Cs"

**ElementsHTMLS** is the folder the final HTML files are saved in.

**Experimental_Data** has the manually generated experimental data values for every element. Also included are the reference key files.

**Format_csvs** has the HTML stylings and button lists for the HTML pages. These are split into subdirectories based on the type of page, for example
"MatrixEle" or "OtherData".

**OtherData** has the metastable, hyperfine, and nuclear data for all elements. Also included are the reference key files. Note that metastable states have
to be saved in an excel file unique to the element as opposed to a combined file.

##Data
Folder contains nist_urls.csv, which stores the URLs for the NIST page of the element. These URLs are used in the "ASD" button on the HTML page.

Files are:
<ul>
<li>nist_urls.csv</li>
</ul>

Energies and matrix elements values are stored in folders within the Data folder named after the element in use, i.e. "Cs" or "BaII".

###-Element subdirectories ("Data/BaII")
Every element needs its own sub-folder, named in this convention: "Cs", "BaII", "Fr". These are located in "Data" as subdirectories.
These folders need three files: datapol, rates1, and rates2.

Using BaII as an example, the folder should have these files in this naming convention:
<ul>
<li>datapolBaII.txt</li>
<li>rates1.txt</li>
<li>rates2.txt</li>
</ul>

**datapol** has the matrix element values, wavelengths, and errors. This is used to calculate transition properties.

**rates1** has the transition rates, branching ratios, etc. with their errors. This is used in comparison with the Python code to calculate errors to ensure the same result was obtained.

**rates2** has the lifetimes with errors. This is used in comparison with the Python code to calculate errors to ensure the same result was obtained.
##Format_csvs
These folders store the styling for the various HTML pages. Each type of page (transition rate, matrix element, page with all the transition rates, other data) has its own
unique styling. These stylings are stored in separate folders.

Stylings are split within a folder. For example, there is an "intro_formatting" for most pages that covers the read in of required libraries and any formatting before data tables.

There is often styling in-between data tables, which is also saved as a separate txt files.

Pages also have an "End_formatting" or similar file that controls any javascript functions used and any formatting after all tabular data is saved.

The sub-folders these styles are saved in are listed below.
Folders are:
<ul>
<li>MatrixEle</li>
<li>TransitionRates</li>
<li>OtherData</li>
</ul>

Descriptions for these folders are given below.
###-MatrixEle ("Format_csvs/MatrixEle")
This houses the formatting for the matrix element HTML pages. Matrix element pages are saved in the format Ra.html, CaII.html.

There are four necessary files for matrix element styling.
These files are (Using Ra as example):
<ul>
<li>Intro_to_excel_formatting.txt</li>
<li>Excel_to_main_formatting.txt</li>
<li>End_formatting.txt</li>
<li>RaIIMatButtons.txt</li>
</ul>

**Intro_to_excel_formatting** loads in bootstrap (default styles) libraries, css styles, and function libraries. It also has all the styling before data tables are loaded in, which includes the
menu bar and the list of buttons among other things.

The **Excel_to_main_formatting** controls the styling in-between the data table that is downloaded on the "excel" button click and the data table that is shown on the portal.

**End_formatting** controls the styling to close the HTML file as well as functions for sorting on button clicks.

**RaIIMatButtons** is the unique list of buttons for the Ra<sup>+</sup> matrix element page. Every element loads in the same Intro_to_excel_formatting, Excel_to_main_formatting, and End_formatting files, but has their own MatButtons txt file.

If a user wishes to change the way the matrix elements pages look, they should change one of these files (excluding the MatButtons file). Any change in one of these files will affect the matrix elements HTML pages for every element, and may require changes in the string substitution section of TransitionManualInput.py. See code explanations for more detail.

###-TransitionRates ("Format_csvs/TranstionRates")
This houses the formatting for the transition rates HTML pages. Transition rates pages are saved in the format FrTranAuto.html, BeIITranAuto.html.

There are five necessary files for a single element's transtition rate styling.
These files are (Using Be as example):
<ul>
<li>Intro_to_life_formatting.txt</li>
<li>Life_to_excel_formatting.txt</li>
<li>Excel_to_main_formatting.txt</li>
<li>End_formatting.txt</li>
<li>BeIIButtonList.txt</li>
</ul>
This follows the same format and guidelines as MatrixEle files.

**Life_to_excel_formatting** controls the styling between the lifetime data table and the data table downloaded after clicking "excel".

**Excel_to_main_formatting** controls the styling in-between the data table that is downloaded on the "excel" button click and the data table that is shown on the portal.

The **ButtonList** needed for an element on its transition rates page is different than the button list needed for its matrix elements page, so a different txt file is necessary.

If a user wishes to change the way the transition rate pages look, they should change one of these files (excluding the ButtonList file). Any change in one of these files will affect the transition rates HTML pages for every element, and may require changes in the string substitution section of TransitionManualInput.py. See code explanations for more detail.

There is a sub-folder in this folder that houses the styling files for the "all" page of transition rates. The "all" page is the HTML file that is displayed when a user clicks on
the "all" button for some element's transition rates. This page has its own unique styling and is stored in its own folder.

Folders used:
<ul>
<li>All_states</li>
</ul>

####-All_states ("Format_csvs/TransitionRates/All_states")
This houses the formatting for the pages that display all transition rates of an element at once. These pages are saved in the format BeIITranFull.html, LiTranFull.html.

There are two necessary files for this styling, listed below. There are no element-unique files for the "all" states since no button list is used.

Files necessary are:
<ul>
<li>Intro_to_table_formatting.txt</li>
<li>End_formatting.txt</li>
</ul>

These files follow the same usage as in the transition rate and matrix element pages.

###-OtherData ("TransitionRates/OtherData")
This houses the formatting for the other data HTML page for an element. These pages are saved in the form NaOther.html, CaIIOther.html.
There are more styling files in this folder due to the increased number of data tables. There is required formatting between the end of any one data table and
the beginning of another.

There are no styling files that are unique for an element- all elements share the same files.

Necessary files are:
<ul>
<li>Intro_to_nuclear.txt</li>
<li>Nuclear_to_hyperfine.txt</li>
<li>Hyperfine_to_metastable1.txt</li>
<li>Hyperfine_to_metastableNoExp.txt</li>
<li>Metastable1_to_2.txt</li>
<li>End_formatting.txt</li>
</ul>

**Intro_to_nuclear** and **End_formatting** follow the same style as for matrix element and transition rate pages.

**Nuclear_to_hyperfine** has the styling between the nuclear data and the hyperfine constants A data.

**Hyperfine_to_metastable1** has the styling between the hyperfine data and the metastable data table with columns "State, Property, Theory, Experiment".

**Metastable1_to_2** has the styling between the metastable table listed above and the metastable table with columns "Initial, Final, Transition, Wavelength, Matrix element, Units,
Transition rate, Branching ratio".

**Hyperfine_to_metastableNoExp** is used in place of Hyperfine_to_metastable1 only when an element does not have a second metastable data table.

##ElementsHTMLS

This is the folder where all the HTML files are saved to. There are saved in the format (using "Fr" as an example):

<ul>
<li>Fr.html</li>
<li>FrTranAuto.html</li>
<li>FrTranFull.html</li>
<li>FrOther.html</li>
</ul>

**X.html** is the matrix element page, where X is the element.

**XTranAuto.html** is the transition rate page with buttons for sorting which transitions are shown (the main transition rate page).

**XTranFull.html** is the transition rate page displayed when a user clicks the "all" button on a main transition rate page.

**XOther.html** is the other data page.

Ions are saved in the format, using Ca<sup>+</sup> as an example, of: CaII.html, CaIITranAuto, etc.

##Experimental_Data
Files, using "Ca" as example:

<ul>
<li>Ca+-lifetimes.csv</li>
<li>Ca+-matrix-elements.csv</li>
<li>Key-File.csv</li>
</ul>

Key file contains references with key and DOI. Need to have lifetimes and matrix element file for every element with experimental values.

##OtherData
Files, using "Ba" as example:

<ul>
<li>Metastable_elements.txt</li>
<li>Metastable_key.xlsx</li>
<li>KEY-hyperfine.xlsx</li>
<li>Nuclear-data.xlsx</li>
<li>BaII_Metastable_csv.csv</li>
<li>Ba+_hyperfine.xlsx</li>
</ul>

Metastable_elements is a manually generated txt file with a list of elements with metastable properties.  
Metastable key has references, keys, and DOIs.Key-hyperfine has references, keys, DOIs.   
Metastable_csv files were manually created: opened original metastable .xlsx file, saved the different elements
in that excel file to their own csv file.   
Future versions could potentially have excel not joined together at creation, removing need for this.
Ion hyperfine files have '+' format instead of 'II' format.
