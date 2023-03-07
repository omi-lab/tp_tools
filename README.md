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

## Usage gitBatchParalell set of commands

**Please note**, this commands are bash scripts. You may run them only with bash. Sripts also use parallel utility. It should be accessible from bash environment.

This represented by set of commands:
  * **gitBatchParallel**
  * **gitBatchParallelIfChanged**
  * **gitBatchParallelIfUpdate**
   
Any command from the list above being started in the directory. Scan all 1-st level folders within it and checks if it is git repository and, then, run command for that repostiory. Command shall be passed as argument. I.e. examle:
```
gitBatchParallel 'git status'
```
will run "git status" command within every directory which is under git version control system.
Similary,
```
gitBatchParallel 'git pull'
gitBatchParallel 'git push'
```
will run "git pull" and "git pull" command.

suffix **...IfChanged** will run command only for directory which is not committed (has changes).
and **...IfUpdate** will run command only for directory which is not up to date with remote/... branch repo. I.e. ahead of remote repo. 

## Examples

* [Examples List](https://github.com/tdp-libs/examples) - List of the example programs using the
tdp-libs build system.
