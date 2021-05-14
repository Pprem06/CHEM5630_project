# CHEM5630_project
Final Project

Description of the baseline correct function:

The purpose of this code is to baseline correct IR spectrum data
	The function is designed to ease the plotting of spectra for users
	The function takes in .CSV files as an argument and allows users to simply loop through all spectra files they have using a single function to baseline correct and plot the data

After inputting the desired spectra files in CSV format, 
	the baseline correct function will reset the lowest non-zero absorbance value to 0

The lowest non-zero absorbance value is also subtracted from all other absorbance values to baseline to correct the spectrum

When the spectra is plotted, the y axis minimum is set to -0.02 in order to provide space between the baseline 0 value for a more clear readout
	Meanwhile, the y axis minimum is set to 0.01 above the max peak absorance height to provide clearance above the highest peak

The x axis is set to read from 3500 to 650 wavenumbers, starting with the higher value on the left to resemeble the typical IR spectrum range

How to use the baseline correct function:

The file input must be in CSV format

Files must be defined as variables.
	Then all the files can be run at once by creating a list of all the files

The x and y axes may need to be adjusted based on the parameters of the spectra
	This can be accomplished by changing the ranges of the ax.set_xlim and ax.set_ylim

The graph title can be changed by entering the desired title into as a string variable: baseline_correct(item, i, "Title goes here ")
	If no title is entered, the default title will read as "Spectrum" and if only one file is passed the filenumber will default to 0 and read out as file one
