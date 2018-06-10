Let's start  
  
Level 0

     kali1@sorry: ~  ssh bandit0@bandit.labs.overthewire.org -p 2220
     bandit0@bandit.labs.overthewire.org's password:                                           
     bandit0@bandit: ~$ ls
     readme
     bandit0@bandit: ~$ cat readme
     boJ9jbbUNNfktd78OOpsqOltutMc3MY1
     bandit0@bandit: ~$ logout
     Connection to bandit.labs.overthewire.org closed.
    
Level 0  -- Level 1

     kali1@sorry: ~$ ssh bandit1@bandit.labs.overthewire.org -p 2220
     bandit1@bandit.labs.overthewire.org's password: 
     bandit1@bandit: ~$ ls
     -
     bandit1@bandit: ~$ cat ./-
     CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
     bandit1@bandit: ~logout
     Connection to bandit.labs.overthewire.org closed.

Level 1  -- Level 2

     kali1@sorry: ~$ ssh bandit2@bandit.labs.overthewire.org -p 2220
     bandit2@bandit.labs.overthewire.org's password: 
     bandit2@bandit: ~$ ls
     spaces in this filename
     bandit2@bandit: ~$ cat "space in this filename"
     UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
     bandit2@bandit: ~$ logout
     Connection to bandit.labs.overthewire.org closed.

Level 2  -- Level 3

     kali1@sorry: ~$ ssh bandit3@bandit.labs.overthewire.org -p 2220
     bandit3@bandit.labs.overthewire.org's password: 
     bandit3@bandit: ~$ ls
     inhere
     bandit3@bandit: ~$ cd inhere
     bandit3@bandit: ~/inhere$ find
     .
     ./.hidden
     bandit3@bandit: ~/inhere~$ cat ./.hiddet 
     pIwrPrtPN36QITSp3EQaw936yaFoFgAB
     bandit3@bandit: ~/inhere$ logout
     Connection to bandit.labs.overthewire.org closed.
    
Level 3 -- Level 4
    
     kali1@sorry: ~$ ssh bandit4@bandit.labs.overthewire.org -p 2220
     bandit4@bandit.labs.overthewire.org's password: 
     bandit4@bandit: ~$ ls
     inhere
     bandit4@bandit: ~$ cd inhere
     bandit4@bandit: ~/inhere$ ls
     -file00  -file02  -file04  -file06  -file08
     -file01  -file03  -file05  -file07  -file09
     bandit4@bandit:~/inhere$ cat ./-file07    // try one and one and find in which file humanreadble data is available 
     koReBOKuIDDepwhWk7jZC0RTdopnAYKh
     bandit4@bandit:~/inhere$ logout
     Connection to bandit.labs.overthewire.org closed    

Level 4 -- Level 5
             
     ali1@sorry: ~$ ssh bandit5@bandit.labs.overthewire.org -p 2220
     bandit5@bandit.labs.overthewire.org's password: 
     bandit5@bandit: ~$ ls
     inhere
     bandit5@bandit: ~$ cd inhere
     bandit5@bandit: ~/inhere$ ls
     maybehere00   maybehere04   maybehere08  maybehere12  maybehere16
     maybehere01   maybehere05   maybehere09  maybehere13  maybehere17
     maybehere02   maybehere06   maybehere10	 maybehere14  maybehere18
     maybehere03   maybehere07   mmaybehere11 maybehere15  maybehere19
     bandit5@bandit:~/inhere$ 
     bandit5@bandit: ~/inhere$ find -size 1033c | sort -h 
     ./maybehere07/.file2
     bandit5@bandit: ~/inhere$ cat ./mayebehere07/.file2
     DXjZPULLxYr17uwoI01bNLQbtFemEgo7
