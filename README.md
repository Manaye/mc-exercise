# mc-exercise


We started out okay. Each group correctly began working in their own featurebranch, reviewed Bob and Carol's feature, and merge it. Ted and Alice pull the new master down and begin working from there. 

However, when Carol and Bob switch to Bob's laptop, Bob's laptop has not received the new changes. They then begin working on a new feature branch without those changes. 

Ted and Alice merge their feature. It merges just fine. However, when Bob and Carol attempt to merge their feature branch, there is a merge conflict that must be resolved because Bob does not have the changes they had originally made.

Both groups work together, resolve the conflicts and merge. They all pull from master and have identical local master branches.
Then, both groups start making features directly in the master branch. NEVER DO THIS. EVER. The first push has no conflicts, but the second group is unable to push, receiving the following error:


hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.

We see this error because github refuses to remove the changes that had been made by the first group to push to master. We resolved this by stashing local changes and pulling from master, then re-adding our changes. 


We learned a few things. The first portion teaches us to never edit in the same file (or at least, not over the same lines; we only encountered merge conflicts when we worked on the same portion of code.) Merge conflicts are comparatively easy, however, when we are pushing branches instead of directly to master. This creates huge problems that substantially impede workflow, requiring one group to either save their changes, pull and manually re-add them, or merge them within VS Studio, which we discovered has a host of additional issues. It is best never to reach this point. At all. 
