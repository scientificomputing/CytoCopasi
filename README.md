# CytoCopasi

CytoCopasi is a Cytoscape app that enables modeling, importing, simulating, and comparing biochemical reaction networks. It uses the Java bindings of Complex Pathway Simulator (COPASI) for quantitative systems biology modeling. 

Besides the regular ODE-based tasks, such as time course simulation and steady state analysis, users can also superimpose and compare two chemical reaction networks (e.g., a healthy vs diseased state) to display the concentration deviations at steady state. Users can also manually perturb a model by modifying one or more parameters of their choice (e.g., the activity of an enzyme or the initial concentration of a drug molecule) and visualize the downstream effects on the steady state profile.

## Features

●	Systems Biology Markup Language (SBML) support

●	Import local SBML files

●	Direct connection to KEGG for importing pathways and converting them into SBML

●	Extract KEGG modules as subnetworks

●	Supports BRENDA’s SOAP access for enzyme functional data queries

●	Comparative reaction network visual analytics 

●	Perturbation analysis capable of visualizing downstream effects due to mutations or drug treatment

●	Optional dynamic simulation via SBMLSimulator

## Installation

### System Requirements

●	Windows, Linux, Unix, or MacOS operating system

●	Cytoscape 3.8. or above https://cytoscape.org/ 

●	Java OpenJDK 11.0.14 or above

### Important: Native Libraries

The Native Libraries file contains three native library files, .dll, jnilib, and .so for Windows, MacOS, and Linux/Unix, respectively.

Since COPASI is written in C++, COPASI classes are compiled into copasi.jar contained within the main bundle. This jar file will only work when the accompanying native library is in the java.library.path. 

Work is underway to automate native library access. For the time being, before initializing CytoCopasi, make sure to copy the appropriate native file to a directory in your java.library.path

#### How to see the current value of the java.library.path variable

Java.library.path usually contains multiple directories, but the user can copy the native library to any of them. 

For all OS types: Open Terminal and type
java -XshowSettings:properties  
(find the java.library.path section in the output)
 
#### To Copy the Native Library to Your java.library.path:
● Download the application and supporting files from https://github.com/scientificomputing/CytoCopasi 
● Extract the folder from .zip





#### Mac OS X

Go to CytoCopasi-main/Native Libraries/
The correct type of Mac OS X native library depends on your Mac processor. If you are not sure, this [article](https://www.makeuseof.com/how-to-find-out-if-your-mac-uses-intel-or-apple-silicon/) explains how to find out

For intel (x64): go to Mac OS X (Intel)
For M1/M2 chips: go to Mac OS X M1M2
Open terminal
sudo cp libCopasiJava.jnilib <the selected java.library.path directory>
ex: sudo cp libCopasiJava.jnilib /Library/Java/Extensions
Enter your user password when prompted.

#### Windows

Go to CytoCopasi-main/Native Libraries/Windows
Run terminal (Windows PowerShell) as administrator (this option will appear when you right-click on the terminal icon.
cp CopasiJava.dll <the selected java.library.path directory>


#### Linux/Unix

Go to CytoCopasi-main/Native Libraries/Linux
Open terminal
sudo cp libCopasiJava.so <selected java.library.path directory>


### Installation

Since CytoCopasi is not yet available on App Store, you need to install it in one of the following two methods.

#### 1-	App Manager

Click on “Install from file” on the App Manager Dialog, and find the downloaded .jar file

#### 2-	Copy the downloaded jar file

Copy the jar file to [...]/CytoscapeConfiguration/3/apps/installed

Once the installation is complete, you will see the CytoCopasi tab on the left panel space




