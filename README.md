# gobrew
A Bash script to quickly switch go versions installed via Homebrew on the Mac.

## Install

Drop the gvm file in a location in your PATH and give it execution permissions. 

Install multiple versions of go with 

```
export HOMEBREW_NO_INSTALL_CLEANUP=1; brew install go@VERSION
```
Make sure that variable is in your shell's rc file or brew will wipe out old
versions next time.

## Run


```
>gobrew help
usage: gvm [GO_VERSION|help]
note: will switch Homebrew's 'go' to the highest version matching
      GO_VERSION at the beginning of the version string. For
      example 1.17 will switch the current go binary to 1.17.X
      with maximum X available. Not passing GO_VERSION will switch
      to the highest version available.
      To install another go version without removing the older ones:
      export HOMEBREW_NO_INSTALL_CLEANUP=1; brew install go@VERSION
 >gobrew
Switching to 1.18.1
 >gobrew 1.17
Switching to 1.17.9
 >gobrew 1.17.5
Version not found. Available versions: 1.16.15 1.17.6 1.17.9 1.18.1
```
