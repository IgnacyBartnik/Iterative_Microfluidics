Fluorescence reaction feedback loop 

Analytical pipeline for controlling 4 syringe pumps to dilute 2 chemicals in a microfluidic chip. This repository compliments a manuscript currently under review.

![image](https://user-images.githubusercontent.com/80273951/173040833-59afe3f3-1e85-44ea-b64c-0e9aa8f85b0f.png)

Getting started
The code has a series of pre requisites: 

Software requirements
- It uses the Ximea CamTool software and therefore requires Windows
https://www.ximea.com/support/wiki/apis/XIMEA_Windows_Software_Package
- python 3.8 or higher with the following non standard libraries: pyautogui, winsound.

Hardware requirements 
- Chemyx Inc. Fusion syringe pumps connected via USB - Other pumps could be used with some modification - in the manuscript we utilised the pumps available within our lab. The code can easily be modified by adjusting the class object which represents the pumps.

- A microfluidic mixing chip - In the manuscript we utilised a mixing feature previously outlined in the following publication (doi: 10.1021/acs.analchem.8b03169). The feature was implemented into PMMA fluidic chips fabricated with laser lithography. The schematics for each layer of the chip is included in the 'Fabrication' folder.

- An appropriate fluorescent microscope assembly - In the manuscript an X microscope was used.

- A Ximea camera - Other cameras and sensor inputs could easily be implemented - we utilised the XimeaCam Tool due to its popularity in the biophysical sciences and its ease of operation.

Overview 
To take measurements, the pipeline automatically operates the Ximea CamTool, to average the values from a line profile. The experimenter initially sets a stoichiometry range and a resolution (~ 10 measurements). This is passed to the pipeline which then operates the pumps and camera. After a pass, the intensity and stoichoiometry are interpolated to yield a dummy function. This function is passed to a simple threshold based algorithm to isolate information within the function. This then allows establishment of the next stoichiometry to isolate the reaction information in high resolution. This loop can run until convolution. 

The code is structured with two python files and two operational notebook files which are split into non diluting and diluting chip approaches.

For the 2pump_control.py program, Mixer V27 in the manuscript was used.
For the 4pump_control.py program, Mixer V28 in the manuscript was used.

The .ipynb files are meant to explain and showcase the features of the respective .py files.

Authors 
- Code & Chip Design - Ignacy Bartnik 
- Experimental design - Robert Strutt
- Project supervision - Nick Brooks and Robet Strutt

