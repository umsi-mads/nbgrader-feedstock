About UMSI nbgrader
===================

This repository is used to keep track of the patches we need to apply onto the
upstream version of nbgrader. We use 0.6.2, but occasionally need to use changes
applied in master (so intended for 0.7.x).

These changes are applied via the recipe.

### Add new patch

1. Clone nbgrader 0.6.2
2. Make the change you need and commit it.
3. Run `git format-patch -1` to generate a patch file.
4. Copy that patch file into `recipe/` and rename as appropriate.
5. Add the patch to the list in `recipe/meta.yaml:source.patches[]`

Then, because we aren't using official conda-forge machinery, you can use the
`build-locally.sh` script to run the build and test process.
