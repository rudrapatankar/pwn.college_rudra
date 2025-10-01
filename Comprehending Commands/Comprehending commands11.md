# Comprehending Commands

##Epic file system quest

With your knowledge of cd, ls, and cat, we're ready to play a little game!

We'll start it out in /. Normally:

hacker@dojo:~$ cd /
hacker@dojo:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  dev        flag  lib   lib64  media   opt  root  sbin  sys  usr
That's a lot of contents! One day, you will be quite familiar with them, but already, you might recognize the flag file and the challenge directory.

In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

Your first clue is in /. Head on over there.
Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
cat that file to read the clue!
Depending on what the clue says, head on over to the next directory (or don't!).
Follow the clues to the flag!

**Flag:** pwn.college{Izrshq2JDTi9x37W_25xgxN9Y80.QX5IDO0wiNxIzNzEzW}


if we wish to open clue without cd then ls /address. get name of required file then cat /address/filename and clue solved. for hidden clues cd /address then ls -a and then cat /address/filename


```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
GIST  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat /GIST
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/three/examples/js/loaders/obj2/worker

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/javascript/three/examples/js/loaders/obj2/worker
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/three/examples/js/loaders/obj2/worker$ ls -a
.  ..  .NOTE  main  parallel
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/three/examples/js/loaders/obj2/worker$ /usr/share/javascript/three/examples/js/loaders/obj2/worker/.NOTE
bash: /usr/share/javascript/three/examples/js/loaders/obj2/worker/.NOTE: Permission denied
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/three/examples/js/loaders/obj2/worker$ cat /usr/share/javascript/three/examples/js/loaders/obj2/worker/.NOTE
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/Documentation/virt/kvm

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/three/examples/js/loaders/obj2/worker$ cd /opt/linux/linux-5.4/Documentation/virt/kvm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/virt/kvm$ ls -a
.                          api.txt    halt-polling.txt  mmu.txt         review-checklist.txt
..                         arm        hypercalls.txt    msr.txt         s390-diag.txt
.REVELATION                cpuid.rst  index.rst         nested-vmx.txt  timekeeping.txt
amd-memory-encryption.rst  devices    locking.txt       ppc-pv.txt      vcpu-requests.rst
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/virt/kvm$ cat /opt/linux/linux-5.4/Documentation/virt/kvm/.REVELATION
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/git/objects/__pycache__
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/virt/kvm$ ^C
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/virt/kvm$ cd /usr/local/lib/python3.8/dist-packages/git/objects/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ ls
TEASER                   base.cpython-38.pyc  commit.cpython-38.pyc  tag.cpython-38.pyc   util.cpython-38.pyc
__init__.cpython-38.pyc  blob.cpython-38.pyc  fun.cpython-38.pyc     tree.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ cat /usr/local/lib/python3.8/dist-packages/git/objects/__pycache__/TEASER
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/compat/32bit

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ cat /opt/linux/linux-5.4/include/config/compat/32bit
cat: /opt/linux/linux-5.4/include/config/compat/32bit: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ ls /opt/linux/linux-5.4/include/config/compat/32bit
BRIEF-TRAPPED  time.h
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ cat /opt/linux/linux-5.4/include/config/compat/32bit/BRIEF-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/testing/tests

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/git/objects/__pycache__$ cd /usr/local/lib/python3.8/dist-packages/sympy/testing/tests
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ ls
WHISPER      __pycache__          test_code_quality.py  test_module_imports.py  test_runtests_pytest.py
__init__.py  diagnose_imports.py  test_deprecated.py    test_pytest.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ cat /WHISPER
cat: /WHISPER: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ cat /usr/local/lib/python3.8/dist-packages/sympy/testing/tests/WHISPER
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/sympy/functions/elementary/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ ls /usr/lib/python3/dist-packages/sympy/functions/elementary/__pycache__
DISPATCH-TRAPPED          exponential.cpython-38.pyc  miscellaneous.cpython-38.pyc
__init__.cpython-38.pyc   hyperbolic.cpython-38.pyc   piecewise.cpython-38.pyc
complexes.cpython-38.pyc  integers.cpython-38.pyc     trigonometric.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ cat /usr/lib/python3/dist-packages/sympy/functions/elementary/__pycache__/DISPATCH-TRAPPED
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/Documentation/scsi/scsi_transport_srp

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ ls /opt/linux/linux-5.4/Documentation/scsi/scsi_transport_srp
Makefile  README-TRAPPED  rport_state_diagram.dot
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ cat /opt/linux/linux-5.4/Documentation/scsi/scsi_transport_srp/README-TRAPPED
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/pyformlang/tests

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/testing/tests$ cd /usr/local/lib/python3.8/dist-packages/pyformlang/tests
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pyformlang/tests$ ls -a
.  ..  .LEAD  __init__.py  __pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pyformlang/tests$ /usr/local/lib/python3.8/dist-packages/pyformlang/tests/.LEAD
bash: /usr/local/lib/python3.8/dist-packages/pyformlang/tests/.LEAD: Permission denied
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pyformlang/tests$ cat /usr/local/lib/python3.8/dist-packages/pyformlang/tests/.LEAD
pwn.college{Izrshq2JDTi9x37W_25xgxN9Y80.QX5IDO0wiNxIzNzEzW}
```

### New Learnings
Lengthy program does not mean it is difficult

### References 
N.A.
