##  Merging and Rebasing

* <!-- .element: class="fragment" --> Merging takes two branches (or commits) and produces a new merged commit
* <!-- .element: class="fragment" --> Rebasing takes two branches (or commits) and chains them together (linear)

---

## Merging

* Fast-forward merging is allowed when the path between your commit and the target is a straight line
* Fast-forward merges simply relocate the branch pointer up the chain
* Non fast-forward merging creates a new merge commit that joins two parent commits (convergence)
* You can always force a new merge commit to be created
* The merge commit protects both parents from being orphaned

---

## Rebasing

* Rebasing is used to bring in changes from another (target) branch by relocating your (source) branch on top
* From the point of divergence, cut the fork and connect the tip of the target to the base of the source
* Take a divergence and create a straight line
* Source changes are now embedded behind your commits

note:
  Rebasing is a Git operation that takes a common point of ancestry between two branches and *replays* commits on top

    This is one of the most complicated struggles of learning Git

    This results in a history *re-write*
