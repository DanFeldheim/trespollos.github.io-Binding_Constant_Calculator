# Binding_Constant_Calculator

06-17-2019

I. File list
Readme.md
Binding constant calculator.py (python 3)

II. Description
This python 3.0 program calculates biomolecule binding affinity constants from 96-well fluorescence titration measurements.
The Tkinter gui allows the user to select one or more csv files for analyis and a path for results. 
Entry boxes exist for ligand concentrations and the range of columns in the well plate to be analyzed.
The protein concentration entry box is not needed in this version, but could used in a future version 
for a quadratic fit to the data. This version uses a hyberbolic fit only.

III. Data input
CSV files must have the following format:
No column or row numbers/letters.
Each column contains one titration with 7 rows, one for each ligand concentration (+ligand/+target). The 8th row of the column 
is +ligand/-target. This background fluorescence signal is automatically subtracted from the other 7 entries. 

IV. Data output
The 2nd tab in the gui displays plots of fluorescence vs. concentraton for each column of each plate selected for analysis.
A maximum of 12 plates will be displayed. If multiple plates are selected for analysis only plots from the last plate are displayed.
If a checkbox is selected, each plot is exported as a pdf file with the plot, the fit to the hyperbolic Kd equation, the Kd with 
standard deviation and 95% CI, and the max fluorescence from the fit with its standard deviation.
These params are also exported to a csv file if desired.
File names are provided automatically based upon the file name of the input csv file, with A, B, C... added for each individual plot.
