# tdp_tools
Scripts for managing projects made up of multiple git modules. Projects built using tdp-libs are assembled from many libraries each of which is held in its own git module, these scripts have been created to aid in that process.

## Installation
Clone this repo and add the scripts directory to your path.

## Usage
* **tdpUpdate** - This performs git pull on each git module found in this directory and clones new modules that are listed in submodules.pri files. See the [tdp_build documentation](https://github.com/tdp-libs/tdp_build) for more information about the submodules.pri files.
* **tdpStatus** - This performs git status on each git module found in this directory.
*  **tdpCommit** - Use tdpCommit followed by a message to commit and push all changes in each git module found in this directory.