# kubeselect

<img src="./kubeselect.gif" width="928px" height="588px" />

## Why?

Working with multiple K8S contexts for many different clients, I'm always annoyed by having to remember context names.
Using `kubectl config get-clusters` then having to type is too much work.
Even searching my shell history gets tidious when I have so many clusters to manage and it's hard to keep track of names,
especially with super longs ones auto-generated by AWS etc.

This small helper util helps select an available Kubernetes context using the arrow keys
using one simple command rather than two seperate kubectl commands to first show, then select contexts.

It uses the mapfile shim found [here](https://github.com/dosentmatter/bash-mapfile-shim).
which itself uses [upvars](http://fvue.nl/wiki/Bash:_Passing_variables_by_reference) by Freddy Vulto.
These are only needed for bash versions < 4, otherwise the native functions are used.

Finally, the small select_option function was found on [this StackOverflow thread](https://stackoverflow.com/questions/11426529/reading-output-of-a-command-into-an-array-in-bash).
I included all source code I used as is in the bash script itself.

Tested on MacOS, YMMV.

P.S.:
The incredibly useful theme I'm using in the GIF above is [bobthefish](https://github.com/oh-my-fish/theme-bobthefish) on the mighty [fish shell](https://fishshell.com/).
The part of which that shows the current Kubernetes context is originally also my contribution.
I consider this a MUST when managing multiple clusters.
The theme itself can be installed using [oh-my-fish](https://github.com/oh-my-fish/oh-my-fish).

## Installation

`$ sudo cp kubeselect /usr/local/bin`

## Usage

`$ kubeselect`

That's it, hope somebody finds it useful like I did. Star if you do!
