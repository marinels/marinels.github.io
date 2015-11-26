##  Stashing and Resetting

* <!-- .element: class="fragment" --> Stashing is a mechanism of saving your changes (locally) without making a commit
* <!-- .element: class="fragment" --> Resetting is a mechanism of moving around the commit chain

---

## The Stashes

* Live in your local repository but cannot be synced to any remote
* Essentially a patch that can be applied locally
* Useful for applying uncommitted changes to a new branch when checking out is not an option
* Useful for applying routine changes that you don't want to commit

---

## Reset

* Allows you to move to a snapshot without changing your current branch
* You can throw away changes between current and destination commits (hard reset)
* You can keep changes between current and destination commits (soft/mixed reset)
* Resetting allows you to relocate your branch pointer to a new commit

note:
  soft reset auto-stages changes, mixed does not
