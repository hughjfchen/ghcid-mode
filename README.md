# This is a fork from https://github.com/ndmitchell/ghcid/blob/master/plugins/emacs

## Problems
* determine the project root
* figure out how to start ghcid

Here's super basic emacs support for ghcid. This uses a terminal with compilation-mode.

This code also assumes that stack is installed, which maybe isn't a great assumption. I had to do that in the past to get ghcid to behave properly with my stack environment, but perhaps ghcid works well now with stack without having to invoke the stack command directly.

Originally written by @WraithM.
