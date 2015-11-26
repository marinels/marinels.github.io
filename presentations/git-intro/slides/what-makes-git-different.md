##  What Makes Git Different?

* <!-- .element: class="fragment" --> No more *requirement* of a single central server
* <!-- .element: class="fragment" --> Ability to ***rewrite*** commit history
* <!-- .element: class="fragment" --> Eliminates the issue where a developer *cannot commit* their changes due to conflicts from someone else's commits

---

# Distributed Protocol

* Git uses a protocol that permits distributed remote repositories
* You can be someone's remote just as they can be yours
* You can push different branches to different remote repositories
* Typically a git *host* exists that acts as a central server

---

# Time Travel

* Re-order and re-shape the commit chain
* Simplify *commit often* and *cleanup after* strategies
* Support more advanced workflows

---

# Master of Your Own Repository

* Only you commit to your local repository
* Only you can create conflicts locally
* Easy to keep your local repository conflict free

note:
  Committing changes is always possible because you only ever commit to the local repository. Now pushing changes becomes the gateway. But this means the developer can **always** version their changes, just maybe not push them up centrally. This is a much safer practice to versioning changes.
