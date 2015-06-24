packer-issue1752-fix
===

# Deprecated
As of packer `Packer v0.8.0` this issue has been solved upstream.
I'll leave the repo here for a while before I remove it completely.


# What is it ?
  This repo holds in the `packer/` directory the packer binaries, built from the master branch(14/02/2015) , accordingly to the build instructions in the original repo https://github.com/mitchellh/packer.
  The binaries have been built for the **linux 64bit architecture** aka `amd64` or `x86_64`

  The packer binaries also contain the fix created by mariussturm in https://github.com/mitchellh/packer/commit/3a286ab6bdba7b8e5bf6a43c357a0ffeacd3dc97 that fixes the issue present in the github issue https://github.com/mitchellh/packer/issues/1752  

  This is a temporary repo, it won't be needed once the packer maintainers fix https://github.com/mitchellh/packer/issues/1752  

# How to use and test ?
  Overwrite your current packer binaries with the ones from the `packer/` directory.
  From the root of this repo test that you can build a docker image by running:
- `packer validate template.json && packer build template.json`
- the output will be a docker image by the name of `ubuntu-14.04.image.tar` which packer will drop in the current dir after it is done.

  If the above 2 steps completed succesfully then you've verified that the packer binaries contain the fix for https://github.com/mitchellh/packer/issues/1752
