# adcs_hardware
Hardware repository for ADCS


# VERSION CONTROL


WHENEVER A SHEMATIC REVISION IS COMPLETED, UNLIKE SOFTWARE, BRANCHES SHOULD NOT BE MERGED. THEY SHOULD BE FROZEN.

TO START A REVISION, THE CURRENT "HEAD" SHOULD BE FORKED (READ: MAKE A NEW BRANCH) NAMED APPROPRIATELY. 

If the revision is accepted and the design changes pass review, the revision branch then becomes the new master branch.

This way, the last "stable" revision branch (the old master branch) remains completely unchanged and unaffected by deltas made in the forked branch.

If there is ever an issue, the old version can be selected SIMPLY by switching back to the old branch, no merging should ever occur.
