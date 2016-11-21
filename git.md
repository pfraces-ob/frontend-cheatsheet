Git
===

Merge one branch into another
-----------------------------

Merge FEAT into DEV

    git checkout DEV
    git merge FEAT

Merge FEAT into DEV (update branches from remotes)

    git checkout FEAT
    git pull
    git checkout DEV
    git pull
    git merge FEAT

Resolve conflicts

    git mergetool
    git commit
    git push origin DEV

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
