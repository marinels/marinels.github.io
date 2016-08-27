##  What Makes Git Different?

* <!-- .element: class="fragment" --> Version Control System based on sound graph theory principals
* <!-- .element: class="fragment" --> No more *requirement* of a single central server
* <!-- .element: class="fragment" --> Ability to ***rewrite*** commit history
* <!-- .element: class="fragment" --> Eliminates the issue where a developer *cannot commit* their changes due to conflicts from someone else's commits

---

# Distributed Protocol

* Git uses a protocol that permits distributed remote repositories
    * Git protocol supports many transports
    * `http`, `ssh`, and `UNC` (file system) paths
* You can be someone's remote just as they can be yours
    * Every repository is both a client and a server
* You can push different branches to different remote repositories
    * Allows public and private remote repositories
* Typical usage involves a git *host* that acts as a central server for a team
    * i.e. Github and Bitbucket

---

# Time Travel

* Re-order and re-shape the commit chain
    * commits are immutable, the graph itself is mutable
* Simplify *commit often* and *cleanup after* strategies
    * rework and combine commits before pushing up to a remote
* Support more advanced workflows
    * i.e. branching/forking and pull request strategy

---

# Master of Your Own Repository

* Only you commit to your local repository
* Only you can create conflicts locally
    * You resolve conflicts before syncing to a remote
* Easy to keep your local repository conflict free
    * Deal with conflicts when it's convenient for you

note:
  Committing changes is always possible because you only ever commit to the local repository. Now pushing changes becomes the gateway. But this means the developer can **always** version their changes, just maybe not push them up centrally. This is a much safer practice to versioning changes.
