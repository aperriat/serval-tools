serval-tools
============

Tools that the [Serval Project][] uses to develop its software.

All unit documentation is in the [doc](doc/) folder.  See below for
installation instructions.

Command-line utilities
----------------------

To use these utilities, check out the **serval-tools** repository somewhere
(eg, into /usr/local/serval-tools) and add its *bin* directory to your path,
eg, by putting the following line into your shell's $HOME/.profile:

    export PATH="$PATH:/usr/local/serval-tools/bin"

The following utilities are aimed at making it easier to work with Git and Git
submodules.  They make no assumptions about the layout of source code Git
repositories.  They all act on the current directory and the current Git
repository as determined by the current working directory.

* [sp-ls-files](doc/sp-ls-files.md) is a wrapper around **git ls-files** that
  handles submodules

* [sp-find](doc/sp-find.md) is a wrapper around the standard *find*(1) utility
  that excludes files ignored by Git

* [sp-grep](doc/sp-grep.md) searches all files in the current Git working copy
  and its submodules

* [sp-mktags](doc/sp-mktags.md) generates **tags** and **cscope.out** index
  files for the current Git working copy

* [sp-exclude-directories](doc/sp-exclude-directories.md) is a simple filter
  that removes all lines that name a directory

The following utility is a general-purpose script for migrating issues from a
Mantis bug tracker to the GitHub Issues list of any GitHub repository:

* [sp-mantis2github](doc/sp-mantis2github.md)

Vim Git plugin
--------------

The *gitdiff.vim* plugin for the *vim*(1) editor provides easy access to
the Git commit history of any file being edited and easy shortcuts for opening
diff windows to reveal changes.

To use the plugin, check out the **serval-tools** repository somewhere (eg,
into /usr/local/serval-tools) and add its *vim* directory to your Vim runtime
path, eg, by putting the following line into your $HOME/.vimrc:

    set runtimepath=~/.vim,/usr/local/serval-tools/vim,$VIMRUNTIME,/usr/local/serval-tools/vim/after,~/.vim/after

The [plugin file](vim/plugin/gitdiff.vim) itself contains a block comment at
the top describing the keymappings that it provides.  The author plans to
create a Vim help file for the plugin soon.

Linux.conf.au 2013
------------------

The [lca-2013](./lca-2013) directory contains scripts and configuration file
samples used to set up the Serval telephony server at Linux.conf.au 2013 held
in Canberra from January 28 to February 5.

[Serval Project]: http://www.servalproject.org
