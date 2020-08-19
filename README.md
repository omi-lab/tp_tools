# tp_tools
Scripts for managing projects made up of multiple git modules. Projects built using tdp-libs are 
assembled from many libraries each of which is held in its own git module, these scripts have been 
created to aid in that process.

## Installation
Clone this repo and add the scripts directory to your path.

### Mac
```
cd ~
git clone https://github.com/tdp-libs/tp_tools.git
cd tp_tools/scripts
sudo sh -c 'pwd >> /etc/paths'

```

## Usage
* **tpUpdate** - This performs git pull on each git module found in this directory and clones new 
modules that are listed in submodules.pri files. See the 
[tp_build documentation](https://github.com/tdp-libs/tp_build) for more information about the 
submodules.pri files.
* **tpStatus** - This performs git status on each git module found in this directory.
* **tpCommit** - Use tpCommit followed by a message to commit and push all changes in each git 
module found in this directory.

## Examples

* [Examples List](https://github.com/tdp-libs/examples) - List of the example programs using the
tdp-libs build system.
