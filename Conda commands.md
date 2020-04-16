#### Managing Conda and Anaconda :

`conda info` Verify conda is installed, check version #
`conda update conda` Update conda package and environment manager
`conda update anaconda` Update the anaconda meta package

#### Managing Environments :

`conda info --envs` Get a list of all my environments
`conda info -e` Active environment shown with *
`conda create --name <env1> <biopython>` or `conda create -n <env1> <biopython>` Create an environment and install program(s) 
`conda activate <env1>` Activate the new environment to use it
`conda deactivate` Deactivate the environment
`conda create -n <env1> python=3.8 <pythonName>` Create a new environment, specify Python version
`conda create -n <env2> --clone <env1>` Make exact copy of an environment
`conda remove -n <env2> --all` Delete an environment
`conda env export > <abc>.yml` Save current environment to a file
`conda env create -f <abc>.yml` Load environment from a file

#### Managing Python :
`conda search --full-name python` or `conda search -f python` Check versions of Python available to install
`conda create -n <customPythonName> python=3.8` Install different version of Python in new environment

#### Managing .condarc Configuration :
`conda config --get` Get all keys and values from my .condarc file
`conda config --get channels` Get value of the key channels from .condarc file
`conda config --add channels <channelName>` Add a new value to channels so conda looks for packages in this location

#### Managing Packages, Including Python :
`conda list` View list of packages and versions installed in active environment
`conda search <packageName>` Search for a package to see if it is available to conda install
`conda install -n <env1> <packageName>` Install a new package
NOTE: If you do not include the name of the environment, it will install in the current active environment.
`conda update <packageName>` Update a package in the current environment
`conda search --override-channels -c <channelName> <packageName>` Search for a package in a specific location (the <channelName> channel on Anaconda.org)
`conda install -c <channelName> <packageName>` Install a package from a specific channel
`conda search --override-channels -c defaults <packageName>` Search for a package to see if it is available from the Anaconda repository
`conda install iopro accelerate` Install commercial Continuum packages
`conda skeleton pypi pyinstrument` or `conda build pyinstrument` Build a Conda package from a Python Package Index (PyPi) Package

#### Removing Packages or Environments :
`conda remove --name <envName> <packageName>` Remove one package from any named environment
`conda remove <packageName>` Remove one package from the active environment
`conda remove --name <envName> <packageName> <customPythonName>` Remove multiple packages from any environment
`conda remove --name <customPythonName> --all` Remove an environment
