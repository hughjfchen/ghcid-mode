# This is a fork from https://github.com/ndmitchell/ghcid/blob/master/plugins/emacs

Here's super basic emacs support for ghcid. This uses a terminal with compilation-mode.

This code also assumes that stack is installed, which maybe isn't a great assumption. I had to do that in the past to get ghcid to behave properly with my stack environment, but perhaps ghcid works well now with stack without having to invoke the stack command directly.

Originally written by @WraithM.

## What problems this fork is trying to solved?

This fork's trying to start the ghcid for a project within emacs smoothly by addressing the following two problems:

* determine the project root
* figure out how to start ghcid

## Current Status

This fork has solved the above two problems.

## Install

### Doom

Add following code to your ~DOOMDIR/packages.el~:

(package! ghcid
  :recipe (:host github :repo "hughjfchen/ghcid-mode"))
  
And add following to your ~DOOMDIR/config.el~:

(use-package! ghcid
  :config (load! ghcid))
  
## Things need to improve

Currently, this fork launches ~ghcid~ with ~--test="return ()"~, if you want to run your tests after your codes pass check,
set the ~ghcid-test-command~ in a ~.dir-locals.el~ under an appropriate directory.
