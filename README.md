# CAF
How to merge a newer CAF tag in an android kernel

First go here:

        https://wiki.codeaurora.org/xwiki/bin/QAEP/release

This site gives information about all msm soc release details with tag + android version

Search your msm here.. Check the latest one and look for correct android version and mark that tag.

Now open one of the following links (dependent on your linux kernel version)

3.10: https://source.codeaurora.org/quic/la/kernel/msm-3.10/
3.18: https://source.codeaurora.org/quic/la/kernel/msm-3.18/
4.4: https://source.codeaurora.org/quic/la/kernel/msm-4.4/

Choose the right one and copy it, now go into your kernel folder with a terminal and do

    git fetch <repo link> <tag>

example: 

    git fetch https://source.codeaurora.org/quic/la/kernel/msm-3.18/ LA.UM.5.5.r1-05300-8x96.0 

Then to do the merge you just have to do

    git merge FETCH_HEAD

Now just fix the conflicts if there and then do

    git add -A
    git merge --continue
    
Congratulation, you have (probably) succesfully merged a new caf tag.
