##  Cloning and Checkout

* <!-- .element: class="fragment" --> the `clone` command creates a local repository from a remote repository
* <!-- .element: class="fragment" --> the `checkout` command restores a snapshot

---

# A Fully Working Clone

* A `clone` is an exact duplicate of the remote repository
* All network I/O is compressed for efficiency
* Cloning works with `http`, `ssh`, and `UNC` paths

---

# Moving Around the Commit Chain

* `checkout` lets you view the file system at a specific commit snapshot
* You can `checkout` a branch or a specific commit
* Checkouts are near instant because your local repository knows everything!

note:
  `checkout` projects the repository file system at a snapshot in time
