# Cell Key Perturbation in Python 
## SML User Guide

### Overview

 | Descriptive      | Details                                             |
 |:---              | :----                                               |
 | Support Area     | Statistical Disclosure Control                      | 
 | Method Theme     | Statistical Disclosure Control                      |
 | Status           | Ready to Use                                        |
 | Inputs           | data, record_key, geog, tab_vars, ptable, threshold |
 | Outputs          | frequency table with cell key perturbation applied  |
 | Method Version   | 2.0.0                                               |
 | Code Repository  | [https://github.com/ONSdigital/cell-key-perturbation](https://github.com/ONSdigital/cell-key-perturbation) |
 
### Summary

This method creates a frequency table which has had cell key perturbation 
applied to the counts to protect against disclosure. 

Cell key perturbation adds small amounts of noise to frequency tables. 
Noise is added to change the counts that appear 
in the frequency table by small amounts, for example a 14 is changed to a 15. 
This noise introduces uncertainty in the counts and makes it harder to identify
individuals, especially when taking the 'difference' between two similar
tables. It protects against the risk of disclosure by differencing since it 
cannot be determined whether a difference between two similar tables represents 
a real person, or is caused by the perturbation.

Cell Key Perturbation is consistent and repeatable, so the same cells are 
always perturbed in the same way.

Full details of the methodology and statistical process flow are given in the Methodology section.


## User Notes

### Finding and Installing the method

This method requires Python 3.7 or above and uses the pandas package.

><sub>To prevent downgrading software on your system, we recommend creating a virtual environment to install and run SML methods. This will enable you to install the method with the required version of Python, etc, without disrupting the newer versions you may be running on your system. </sub>


The method package can be installed from PyPI/Artifactory using the following 
code in the terminal or command prompt:

```py
pip install cell_key_perturbation
```

In your code you can import the cell key perturbation package using:

```py
from cell_key_perturbation.create_perturbed_table import create_perturbed_table
```

