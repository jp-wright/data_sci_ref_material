
Vocab
-----------------------

  * branch - remains part of the original repository (dependent on orig. repo)
  * fork - This is a github thing. It is like a clone or copy (independent on orig. repo)

General setup
------------------

  * ~$ git config --global user.name 'Adam Richards'
  * ~$ git config --global user.email 'adamricha@gmail.com'
  * ~$ git config --global core.editor atom
  * ~$ git config --global merge.tool meld

How to get ssh working
^^^^^^^^^^^^^^^^^^^^^^^^^^

Create a new key for each computer

  * ~$ ssh-keygen -t rsa -C "adamricha@gmail.com"
  * ~$ ssh-add ~/.ssh/id_rsa
  * ~$ xclip -sel clip < ~/.ssh/id_rsa.pub
  * ~$ got to [[https://github.com/settings/ssh]] and click on 'add key' and paste it in

Test it
* ssh -T git@github.com


Helpful command
------------------

* where am I?
  ~$ git branch
  ~$ git remote show origin

* Undo changes in a file
  ~$ git checkout somefile.py

* look at diff for a file and a previous commit
  ~$ git diff HEAD^..HEAD my_file.rst

* look at diff for a file and two commits back
  ~$ git diff HEAD^^..HEAD my_file.rst


Branches
---------------

Create a branch
^^^^^^^^^^^^^^^^

  * ~$ git clone [repo]
  * ~$ git branch [branch]
  * ~$ git push origin [branch]


Work on a branch
^^^^^^^^^^^^^^^^^^^^^

  * ~$ git checkout [branch]
  * ~$ git add [filename]
  * ~$ git commit -m 'adding something'
  * ~$ git push origin [branch]


Merge a branch
^^^^^^^^^^^^^^^^^^^

Try to automerge branch 2 into branch 1

  * ~$ git checkout [branch1]
  * ~$ git merge [branch2]
  * ~$ git push origin [branch1]

If there is a conflict merging branch 2 into branch 1

  * ~$ git checkout [branch1]
  * ~$ git merge [branch2]
  * ~$ git status
  * **fix the conflicts**
  * ~$ git commit -m 'merged stuff'
  * ~$ git merge [branch2]
  * ~$ git push origin [branch1]

Submit pull request
-------------------

  * ~$ git branch [branch]
  * ~$ git push origin [branch]
  * commit some changes to your branch
  * Go to the repository page on github and click on "Pull Request" button in the repo header
  * Fill out 'title', 'description' etc
  * Then click on send pull request

Random
-------------------

  * add/edit the .gitignore file to exclude things from being monitored (i.e. 'git status')
