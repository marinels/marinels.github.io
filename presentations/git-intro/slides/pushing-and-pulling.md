##  Pushing and Pulling

* <!-- .element: class="fragment" --> Pushing syncs your local changes with the remote you are pushing to
* <!-- .element: class="fragment" --> Pulling (or fetching) updates your remote pointers with any updates from the remote

---

## Pushing

* Pushing will fail if you are out of sync with the remote
* You can *force* push to override the remote (***DANGEROUS***)
* You are uploading your commit chain(s) that don't exist on the remote
* Only upload the local changes for efficient data I/O

note:
  force push is required for a rebase workflow

---

## Pulling

* Pulling performs a `fetch` followed by a `merge`
* Fetching simply updates your remote references
* You can always manually merge your local branches with remote references
* Fetching should never fail, but pulling can create merge conflicts

note:
  pulling can unintended side effects due to the automated merge
