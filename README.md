# Iterative_Microfluidics
MSci Project Code 

Hello to my Master Project

It was made to control up to 4 syringe pumps
To dilute 2 chemicals in a microfluidic chip with 4 inputs

It uses the Ximea CamTool software
and therefore requires Windows
https://www.ximea.com/support/wiki/apis/XIMEA_Windows_Software_Package

To take measurements, it takes over the mouse and keyboard, and clicks the appriate icons
It all hinges on averaging the values from a line profile taken using the Ximea CamTool
To create a single intensity value

Other cameras and sensor inputs could be used if they could provide a individual sensor output

Chemyx Inc. Fusion syringe pumps connected via USB were used
Other pumps could be used with some modification

For more insight, please look at the two jupyter notebooks.

The microfluidic chip used were made using a laser lithography technique in PMMA
doi: 10.1021/acs.analchem.8b03169

For the 2pump_control.py program, Mixer V27 was used
For the 4pump_control.py program, Mixer V28 was used

Written by Ignacy Bartnik
IgnacyABartnik@gmail.com

Supervised by
Robert Strutt
Nick Brooks

