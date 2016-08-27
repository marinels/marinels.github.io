##  The Commit Graph and Branching

* <!-- .element: class="fragment" --> The commit graph (or chain) is a giant singly linked list
* <!-- .element: class="fragment" --> Every commit points to its parent and is hashed based on its parent's hash
* <!-- .element: class="fragment" --> all branches are simply pointers to the `HEAD` of a specific commit
* <!-- .element: class="fragment" --> any commit that is orphaned becomes available for garbage collection

---

# Chains

* Visualized with SourceTree or via command line:
    * `git log --graph --decorate --oneline --all`
* Committing to a new branch will generate a divergence
* Merging two commits creates a convergence
* Your chain and the remote chain remain in sync except for local changes
    * All local changes diverge from the remote graph
* Removing the last branch pointer on a divergence orphans all commits from the most recent divergence

---

# Pointers

* Because branches are pointers, creating a branch does not create a new commit, just a new pointer
* Pointers always start at an existing commit but diverge upon first new commit
* Pointers can be moved with ease
* Any commits that have no pointers above them are orphaned

note:
  No commits are ever lost immediately
