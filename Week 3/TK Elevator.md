# TK-Elevator Solution

Date: October 13, 2025

### Steps

#### Flag 1

- Repeating for Every Level
    - `ls` to See Content of Directory
    - `cat` to See the README File
    - su --login [username]

- Level 0
    - `cd` Ito `creds_level1`
    - `ls` to See Content
    - `cat` the `creds_level1.txt`
        - Next User: level1_51369
        - Password: 11cd8a
- Level 1
    - Typed `find` in Command Line and Listed Everything in Current Directory
    - found `creds_level2.txt` in `./l7ixcbur/jcyvsxor/5x95hyau/8b76asnz/k3opurzr/14hcp5l8/creds_level2.txt`
    - `cat` the `creds_level2.txt` File
        - Next User: level2_51369
        - Password: 05f186
- Level 2
    - `grep "level" creds_level3.txt` to Find the User Name
        - Next User: level3_51369
    - `grep "password" creds_level3.txt` to Find the Password
        - Password: c6d147
- Level 3
    - Typed `./creds_level4.sh` and Got `Permission Denied`
    - Used `chmod +x creds_level4.sh` and Ran `./creds_level4.sh`
        - Next User: level4_51369
        - Password: 3a54b4
- Level 4
    - Used `ls -a` to All Files in Current Directory
    - `cd` to .hidden_creds_level5 Folder
    - Used `ls -a` Again to All Files in Current Directory
    - `cat` .creds_level5.txt
        - Next User: level5_51369
        - Password: 9d280c
- Level 5
    - Used `cd look\ in\ here/` to Get Into the Directory
    - Used `cat creds\ in\ here\!` to Print the Content
        - Next User: level6_51369
        - Password: 419b4d
- Level 6
    - Used `ps aux | grep "level6_51369"` to Find Info
        - Next User: level7_51369
        - Password: 2ae537
- Level 7
    - `:q!` to Force Quit
    - `ls` to See Any Files
    - `cat creds_level8.txt` to See Content
        - Next User: level8_51369
        - Password: fafaba
- Level 8
    - `cd` to `project` Folder
    - Used `git log` and Found the Password
        - Next User: level9_51369
        - Password: 9e148d
- Level 9
    - `ls -a` to See All Content in Current Directory
    - Found `.creds_level10.txt.swp`
    - `cat .creds_level10.txt.swp`
        - Next User: level10_51369
        - Password: 59dadb
- Level 10
    - Need to Go to Root Folder
        - `cd ..` x2
    - `ls` and Found `flag_2.txt`
    - `cat flag_2.txt`
        - osu{v1m_th3_0nly_r34l_3d1t0r}

#### Flag 2

- Continuing from Flag 1 in Root Folder on Level 10
- Tried to `cat flag_1.txt` but Got `Permission Denied`
- Used `ls -l` to See Permission for `flag_1.txt`
- Saw That Level5 Has Permissio to Read File
- Need to Move Down to Level 5
    - Used `exit` x5
- `cd` to Root
- `cat flag_1.txt`
    - osu{gr3p_c4t5_n0t_cl0wn5}