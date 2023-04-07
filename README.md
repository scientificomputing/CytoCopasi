# CytoCopasi

CytoCopasi is a Cytoscape app that enables modeling, importing, simulating, and comparing biochemical reaction networks. It uses the Java bindings of Complex Pathway Simulator (COPASI) for quantitative systems biology modeling. 

Besides the regular ODE-based tasks, such as time course simulation and steady state analysis, users can also superimpose and compare two chemical reaction networks (e.g., a healthy vs diseased state) to display the concentration deviations at steady state. Users can also manually perturb a model by modifying one or more parameters of their choice (e.g., the activity of an enzyme or the initial concentration of a drug molecule) and visualize the downstream effects on the steady state profile.

## Features

●	Systems Biology Markup Language (SBML) support

●	Ability to import local SBML files

●	Direct connection to KEGG for importing pathways and converting them into SBML

●	Ability to extract KEGG modules as subnetworks

●	Supports BRENDA’s SOAP access for enzyme functional data queries

●	Comparative systems biology analysis to visualize deviations between two reaction networks

●	Perturbation analysis to visualize downstream effects of mutations or drug treatment

●	Optional dynamic simulation via SBMLSimulator

## Installation

### System Requirements

●	Windows, Linux, Unix, or MacOS operating system

●	Cytoscape 3.8.+ https://cytoscape.org/ 

●	Java OpenJDK 11.0.14 

### Important: Native Libraries

The Native Libraries file contains three native library files, .dll, jnilib, and .so for Windows, MacOS, and Linux/Unix, respectively.

Since COPASI is written in C++, COPASI classes are compiled into copasi.jar contained within the main bundle. This jar file will only work when the accompanying native library is in the java.library.path. 

Work is underway to automate native library access. For the time being, before initializing CytoCopasi, make sure to copy the appropriate native file to a directory in your java.library.path

#### How to see the current value of the java.library.path variable

#### Windows

Open an MS-DOS prompt and type

echo %PATH%

#### Mac OS X

Console

java -XshowSettings:properties

#### Linux/Unix

Terminal

java -XshowSettings:properties

### Installation

Since CytoCopasi is not yet available on App Store, you need to install it in one of the following two methods.

#### 1-	App Manager

Click on “Install from file” on the App Manager Dialog, and find the downloaded .jar file

#### 2-	Copy the downloaded jar file

Copy the jar file to [...]/CytoscapeConfiguration/3/apps/installed

Once the installation is complete, you will see the CytoCopasi tab on the left panel space




