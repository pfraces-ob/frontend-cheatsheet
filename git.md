Git
===

Merge one branch into another
-----------------------------

Merge A into B

    git checkout B
    git merge A

Rename local branch
-------------------

Current branch

    git branch -m <newname>

Specific branch

    git branch -m <oldname> <newname>

Source: <http://stackoverflow.com/a/6591218/1815446>

Change timestamp of last commit
-------------------------------

    LANG= GIT_COMMITTER_DATE="$(date --date='2 day ago')" git commit \
        --amend --no-edit --date "$(date --date='2 day ago')"

Source: <http://stackoverflow.com/questions/454734/how-can-one-change-the-timestamp-of-an-old-commit-in-git/9701130#9701130>
