##  Stashing and Resetting

TBD

note:
    * Stashing allows you to set aside some changes locally so that you can change to a new snapshot
        * Stashes are local only and cannot be shared
        * Stashes should be used for temporary storage of changes, or longer term storage of routine changes that should not be versioned
    * Resetting is a Git mechanism to move about the commit chain
        * A hard reset *throws away* changes
        * A soft/mixed reset keeps changes (soft auto-stages changes, mixed does not)
