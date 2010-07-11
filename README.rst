git-remote-bzr
==============

This is a Bazaar remote helper for git. It uses the remote helpers
functionality introduced recently (1.7.2) in git.

As this is only an early proof of concept, it is not recommended for any
use, except maybe documentation about using git remote helpers or satisfying
your curiosity.

What may work:

- small repositories
- cloning local branches
- being slower than bzr (excellent waste of time!)

What certainly doesn't:

- empty repositories
- pushing
- listing remote refs (they are imported first)
- using differential import (every file of every revision is imported)
- linking with bzr refs (git-fetch pulls the whole repository)


Requirements
------------

- git 1.7.2-rc1 or later
- python 2.6
- bzrlib


Usage
-----

1. export the checkout to you PATH variable for git to find it
2. git checkout bzr::url-of-bzr-repository

