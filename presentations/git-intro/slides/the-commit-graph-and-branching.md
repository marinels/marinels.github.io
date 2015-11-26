##  The Commit Graph and Branching

* <!-- .element: class="fragment" --> The commit graph (or chain) is a giant linked list
* <!-- .element: class="fragment" --> Every commit points to its parent and is hashed based on its parent's hash
* <!-- .element: class="fragment" --> all branches are simply pointers to a specific commit
* <!-- .element: class="fragment" --> any commit that is orphaned becomes available for garbage collection

---

# Chains

* Visualized with SourceTree (or via command line with `git log --graph --decorate --oneline --all`)
* Committing to a new branch will generate a divergence
* Your chain and the remote chain are always in sync
* If you diverge then your common point of divergence be where the fork is visualized

---

# Pointers

* Because branches are pointers, creating a branch does not create a new commit, just a new pointer
* Pointers can be moved with ease
* Any commits that have no pointers above them are orphaned and *lost*

note:
  No commits are ever lost immediately
