##  Cloning and Checkout

* <!-- .element: class="fragment" --> the `clone` command creates a local repository from a remote repository
* <!-- .element: class="fragment" --> the `checkout` command restores a snapshot (commit)

---

# The Snapshot File System

* All files and commits in the graph are uniquely hashed
* Every version of every file exists locally (compressed)
* Every commit in the graph lists all file hashes in the snapshot

---

# A Fully Working Clone

* A `clone` is an exact duplicate of the remote repository database
    * Any version of any file in the graph can be re-created
* All network I/O is compressed for efficiency

---

# Moving Around the Commit Chain

* `checkout` lets you view the file system at a specific snapshot (commit)
* You can `checkout` a branch or a specific commit
* Checkouts are near instant because your local repository knows everything!
    * Files are simply replaced from the local database

note:
  `checkout` projects the repository file system at a snapshot in time
