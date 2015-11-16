##  Staging and Committing

TBD

note:
    * Git uses an *Index* as a staging ground for you to select exactly which parts of changed files you would like to commit
    * A commit is essentially a snapshot in time of the file system
    * Every commit is hashed to give it a unique ID
        * This hash is based on the hash of its parent commit ID
        * This means that each commit is unique to its position in the commit chain
    * A commit is logged internally even if you throw it away later. This means if you commit a change you can *almost* always retrieve it if something goes wrong.
