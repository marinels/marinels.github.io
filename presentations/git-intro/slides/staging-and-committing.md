##  Staging and Committing

* <!-- .element: class="fragment" --> Git uses a staging area to choose what is included in a commit
* <!-- .element: class="fragment" --> Commits can include any number of files, any changed content of a file down to a single line

---

## Staging Ground

* The staging area (aka *Index*) allows you to carefully craft your commits so they contain related changes
* SourceTree simulates checkbox file selection to ease the transition
* Stage individual lines or contextually nearby blocks of changes (called hunks)

---

## Commits

* Save one or more file changes to the commit chain
* Every commit generates a unique hash to identify itself with
* All commits are saved for a period of time
* Any commit can be re-ordered, changed, combined
* All commits point to their parent commit (except the initial commit)

note:
  Every commit is hashed to give it a unique ID

    This hash is based on the hash of its parent commit ID

    This means that each commit is unique to its position in the commit chain

    any change to a commit generates a new hash

  A commit is logged internally even if you throw it away later. This means if you commit a change you can *almost* always retrieve it if something goes wrong.

  The initial commit is often a standard pattern (License, README, `.gitignore` file)
