##  Merging and Rebasing

TBD

note:
    * Merging in Git similar to other merging operations is called a non-fast-forward merge
        * These create a new snapshot that includes the merge
    * Fast-forward merges does not create a new snapshot, they simply move the branch pointer
    * Rebasing is a Git operation that takes a common point of ancestry between two branches and *replays* commits on top
        * This is one of the most complicated struggles of learning Git
