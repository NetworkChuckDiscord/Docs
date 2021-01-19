# Installing dependencys in Python
## Contents
1. [What are dependencys](#what-are-dependencys)  
1. [How to install dependencys](#how-to-install-dependencys)  
1. [requirments.txt](#requirmentstxt)  
1. [setup.py](#setuppy)  
1. [package conflicts](#package-conflicts)
## What are dependencys
Dependecy are files that contain that are needed by your program in order to run, They can be compiled functions, librarys, or even compiled binarys.
## How to install dependencys
The main tool used to install python dependencys is `pip`, there are 3 way a program can be installed
- `pip install [program]` install as a system program. This works however can be really messy so is usaully not reccomended.
- `pip install [program] --user` installs a program in the users default envroment. This is also messy but not as bad as installing it systemwide.
- [virtual enviroments](##-virtual-enviroments) The best option see setion for more details.
## virtual enviroments
A virtual enviroment is the best option for installing packages with python can provide multiple clean working enviroments and help to avoid alot of dependency issues. There are two main python enviroment managers.
   ### 1. Virtualenv and pip  
   This is the main method used by developers/devops/casual users installing it is dead simple
   
       $ pip install virtualenv
       $ virtualenv myenv
       $ source myenv/bin/activate
  
  ### 1. Conda  
  This is the main method used by the scientific/math users id allows for more types of dependencys for more details see here.  
  https://docs.conda.io/en/latest/
      
  

## Requirments.txt   
the requirments.txt file is a listing of dependencys needed by the program you are using there are 4 ways a file can be listed there
- package installs the latest version of the package
- package==version installs the listed version of the package
- package=>version installs the latest version of the package assuming its greater then version
- package=<version installs the latest version of the package up untill version

The programs listed in requirments.txt can be easily installed using:  

    $ pip install -r requirments.txt 

## Setup.py
This is a alternitive setup script it should install all the deppendencys and set up some other stuff for you. If the documentation says that exists make sure you use it.
## Package conflicts   
‘Dependency hell’ is an apt term for the vexation that can be experienced when trying to resolve dependency conflicts. Dependency conflicts occur when different Python packages have the same dependency, but depend on different and incompatible versions of that shared package. Because only a single version of a dependency is permitted in any project’s environment, finding a compatible solution can be difficult.

Even in a project that has been isolated in a virtual environment, transitive dependency conflicts can arise. Transitive dependencies are indirect dependencies, otherwise known as dependencies of dependencies. For example, if package A has dependency B and dependency B has dependency C, then package A transitively depends on dependency C. An example of a transitive dependency conflict would be when multiple packages depend on different versions of dependency C. 

Hopefully you will never have to deal with this but it may throw you off when you do.


