# adcs_hardware
Hardware repository for ADCS

# Harware Architecture Overview

![ADCS Hardware Block Diagram 2020.09.08](https://)

# VERSION CONTROL

WHENEVER A SHEMATIC REVISION IS COMPLETED, UNLIKE SOFTWARE, BRANCHES SHOULD NOT BE MERGED. THEY SHOULD BE FROZEN.

TO START A REVISION, THE CURRENT "HEAD" SHOULD BE FORKED (READ: MAKE A NEW BRANCH) NAMED APPROPRIATELY. 

If the revision is accepted and the design changes pass review, the revision branch then becomes the new master branch.

This way, the last "stable" revision branch (the old master branch) remains completely unchanged and unaffected by deltas made in the forked branch.

If there is ever an issue, the old version can be selected SIMPLY by switching back to the old branch, no merging should ever occur.

# Cloning repo for use in Eagle

Clone Repo into your local eagle projects repository
ie: C:/Users/user/Documents/Eagle/projects/

Repo will then appear under projects tab of the 'Control Panel' window when Eagle is launched.

# Eagle File Types Notes
 
## Project Manager File
*.epf is the eagle project manager file and contains all settings information for project. Contains all path references to all the libraries the have been used. *.epf is not crucial to project but can be useful to share with collaborators. 

# Design Files 
*.brd and *.sch files must have matching names and be contained in the same folder. Schematic files also copy all the information from the component libraries once the components are placed in a schematic, making the library files less necessary once used. The .brd files also copy the package information from the component libraries and don’t require libraries again unless you need to place a new component or replace a previous component. 

## Backup Files
*.b#x and *.s#x files are local backups by Eagle. By default Eagle saves 9 backups (9 is also the max).

## Libraries
Libraries are the templates for components. They are unique files that all the information on a specific component that Eagle CAD requires for design. They are the building blocks that contain information like pin numbers, terminal names, symbol shape, package type and footprint size etc. A library has both a symbol (used in schematics) and a package (footprint for pcb layout). Once a library is used in an Eagle design, it is no longer required as Eagle copies all the information over to the schematic and board files. However, while working with your team, it is recommended to share and use the same libraries to keep your designs consistent.

Custom library parts have been saved in managed library: https://library.io/libraries/22876504-my_library
