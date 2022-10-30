# Lab Report 3

In this lab report we are going to explore three different command line options for "find". 

## Findin a type of file 
Sometimes it is useful to search based on the type we are loooking for such as files, directories, or extensions. 

### Example 1: Finding a file type 
Input:
```
tharun@Tharuns-MBP docsearch % find . -type f
```
Output: (I only copied part of the output since there were a lot of files that were found)
```

./technical/biomed/1476-4598-1-5.txt
./technical/biomed/rr191.txt
./technical/biomed/1471-2148-3-4.txt
./technical/biomed/1471-2458-3-11.txt
./technical/biomed/1475-2875-1-5.txt
./technical/biomed/1477-7827-1-31.txt
./technical/biomed/1471-213X-1-10.txt
./technical/biomed/gb-2002-3-3-research0011.txt
./technical/biomed/gb-2002-3-10-research0054.txt
./technical/biomed/1468-6708-3-1.txt
./technical/biomed/1471-2148-1-6.txt
./technical/biomed/1471-2202-4-3.txt
./technical/biomed/1472-6947-1-5.txt
./technical/biomed/1471-2202-2-5.txt
./technical/biomed/1476-9433-1-2.txt
./technical/biomed/1471-2210-1-2.txt
./technical/biomed/1471-2458-1-9.txt
./technical/biomed/1472-6793-2-2.txt
./technical/biomed/gb-2001-2-12-research0053.txt
./technical/biomed/1478-1336-1-2.txt
./technical/biomed/1471-2202-3-16.txt
./technical/biomed/1471-2180-2-13.txt
./technical/biomed/1471-2121-4-4.txt
./technical/biomed/gb-2003-4-4-r28.txt
./technical/biomed/1471-230X-2-17.txt
./technical/biomed/1477-5956-1-1.txt
./technical/biomed/1471-2156-4-9.txt
./technical/biomed/1471-2431-2-12.txt
./technical/biomed/ar328.txt
./technical/biomed/1471-2210-3-1.txt
./technical/biomed/1471-2121-4-5.txt
./technical/biomed/1471-2350-2-8.txt
./technical/biomed/1471-2202-3-17.txt
./technical/biomed/1471-2407-1-13.txt
./technical/biomed/bcr605.txt
./technical/biomed/1476-069X-2-9.txt
./technical/biomed/1478-1336-1-3.txt
./technical/biomed/1471-2164-2-4.txt
./technical/biomed/1471-2210-1-3.txt
./technical/biomed/1476-9433-1-3.txt
./technical/biomed/1471-2334-1-13.txt
./technical/biomed/1471-2407-3-16.txt
./technical/biomed/1471-2164-4-2.txt
./technical/biomed/cvm-2-4-187.txt
./technical/biomed/1471-2105-3-4.txt
./technical/biomed/1471-2121-3-21.txt
./technical/biomed/1471-2202-4-2.txt
./technical/biomed/1471-2172-3-9.txt
./technical/biomed/gb-2001-2-3-research0007.txt
./technical/biomed/1471-2199-2-6.txt
./technical/biomed/bcr567.txt
./technical/biomed/gb-2002-3-10-research0055.txt
./technical/biomed/1471-2121-2-3.txt
./technical/biomed/1471-213X-1-11.txt
./technical/biomed/1472-684X-1-5.txt
./technical/biomed/1476-4598-1-6.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
./plos-sizes.txt
```

Here we are searching for anything that has the type of files. To do this we used "f" to denote that we are looking for files. 

### Example 2: Finding directories 
Input:
```
tharun@Tharuns-MBP docsearch % find . -type d
```
Output:
```
.
./lib
./.git
./.git/objects
./.git/objects/92
./.git/objects/6f
./.git/objects/02
./.git/objects/a4
./.git/objects/bb
./.git/objects/ab
./.git/objects/c7
./.git/objects/c0
./.git/objects/ca
./.git/objects/fe
./.git/objects/ec
./.git/objects/18
./.git/objects/pack
./.git/objects/89
./.git/objects/80
./.git/objects/10
./.git/objects/19
./.git/objects/21
./.git/objects/72
./.git/objects/44
./.git/objects/07
./.git/objects/info
./.git/objects/62
./.git/objects/96
./.git/objects/08
./.git/objects/64
./.git/objects/b6
./.git/objects/d5
./.git/objects/e1
./.git/objects/f9
./.git/objects/f0
./.git/objects/46
./.git/objects/12
./.git/objects/47
./.git/info
./.git/logs
./.git/logs/refs
./.git/logs/refs/heads
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.git/logs/refs/remotes/upstream
./.git/hooks
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/remotes
./.git/refs/remotes/origin
./.git/refs/remotes/upstream
./.git/branches
./.vscode
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```

Here we are searching for directories. To do this we used "d" to denote that we are looking for the different directories. 

#### Example 3: Searching for a symbolic link 
Input and Output:
```
tharun@Tharuns-MBP docsearch % find . -type l
tharun@Tharuns-MBP docsearch % 
```
Here we tried to find a symbloic link using "l", but since ther was none found it did not return anything and will let us input a new command. 

## Searching by Size 

For the first option we are going to be using -size. This command line option is going to search for files of a specific type such as its size. To use this command we also have to use "-type", because the command searched for files based on a parameter within type which in our case is size. 

### Example 1: less than 1024 Bits 
Input:
```
tharun@Tharuns-MBP docsearch % find . -type f -size -1024c
```

Output: 
```
./count-txts.sh
./DocSearchTest.java
./README.md
./.git/config
./.git/objects/92/82fb717a7d79199bf29de7df7da2637df7dc19
./.git/objects/6f/b93f4938a2568b6da4f3c6be5e9e31d99a4bbb
./.git/objects/02/fda6e0b9cec03be2a5c6f6128b6c720326682a
./.git/objects/a4/0d47c88f17fdf0668c47300c04f5a1bfe94106
./.git/objects/bb/e0a0a4c8af52f9b875d1f6791e15ad434a7aec
./.git/objects/ab/ed38d69409aea3d47337002d3a8353907869e1
./.git/objects/c7/f970621f7bb61d2473b0cffb0ec1b6d3a30f4a
./.git/objects/c7/d26e3b75df3a81dab811269256a9d77b618d33
./.git/objects/c0/07e12331f15fd096d9c9731679913224fd7b27
./.git/objects/fe/e12c2ae5ff08d41d6890baad2f3945bfabeaf8
./.git/objects/ec/35bdf2605157098accf33760252b77cdd41a40
./.git/objects/ec/1fcff542cdc23aab6176143ec8bcfa280788d0
./.git/objects/18/1f1a281aa6ef9183bc6a7555b7275dac0832a0
./.git/objects/89/1831ac24270d517f8b943343123a61e618a560
./.git/objects/80/bdb773e8e41ab8e5d4924dc7f617b138d6a880
./.git/objects/10/c4782442ba9b6dc858d145fd865ae3be9403fa
./.git/objects/10/1c819387dfa5de5aaa29680439fef42c418606
./.git/objects/19/9942693961d3b467c35b581639ffd610680932
./.git/objects/44/2d497a20167f6dadb27f7c4e62bd5aa0144f61
./.git/objects/62/6a4c2e593c9d7748b84db3ae17b4a7bdca8702
./.git/objects/62/ee0d134b4e444828c032a253e00e96cf8676e0
./.git/objects/96/1be5a575660a8f4b22ea5b3a6622e94f1ee443
./.git/objects/08/0c229f05b84666f7fdbdf6569f4e70eabcb4d8
./.git/objects/64/4264e690e5a135425270758cd2d24592a2a881
./.git/objects/b6/193bf8f7de930cfe02955bd876768de30be903
./.git/objects/d5/079985d0f4e3be2d929a9cd22ca64a6027b3f0
./.git/objects/e1/ed34bdd1021f8737c38ddf8967c4c63f6a4a22
./.git/objects/f9/38f8f6016b8902c60a43794f3a4c2ced817d07
./.git/objects/f0/248ded3dee0e51a3ccf5c34040b41cb0549c08
./.git/objects/46/ca393e5d2473083540d82d1c91d2a8edc1e0de
./.git/objects/12/84a844c61e61f3c416fa7bfedf8ee66809b8b8
./.git/objects/47/b41c013aaa0577f13edf17cb0b081cbfa468b3
./.git/HEAD
./.git/info/exclude
./.git/logs/HEAD
./.git/logs/refs/heads/main
./.git/logs/refs/remotes/origin/main
./.git/logs/refs/remotes/upstream/main
./.git/description
./.git/hooks/commit-msg.sample
./.git/hooks/applypatch-msg.sample
./.git/hooks/pre-receive.sample
./.git/hooks/post-update.sample
./.git/hooks/pre-merge-commit.sample
./.git/hooks/pre-applypatch.sample
./.git/refs/heads/main
./.git/refs/remotes/origin/HEAD
./.git/refs/remotes/origin/main
./.git/refs/remotes/upstream/HEAD
./.git/refs/remotes/upstream/main
./.git/packed-refs
./.git/COMMIT_EDITMSG
./.git/FETCH_HEAD
./.vscode/settings.json
./test.sh
./start.sh
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.tx
```
These were all the files found in the file directory that had a size of less than 1024 bits. In this example we searched based on size which was indicated by the -size -1024c command. 


### Example 2: More than 1MB
Input: 
```
tharun@Tharuns-MBP docsearch % find . -type f -size +1M
```
Output: 
```
./.git/objects/pack/pack-8e83e6622bbf3eee803317793d589f82891773da.pack
```
In our example we are going to be searching for files which are greater than 1MB. To this we use "+" to denote that we want to find files greater than the size specified. This search resulted in only one file which is shown above. 

### Example 3: Size is within a range
Input: 
```
tharun@Tharuns-MBP docsearch % find . -type f -size  +512c -size -1024c 
```

Output:
```
./.git/objects/02/fda6e0b9cec03be2a5c6f6128b6c720326682a
./.git/objects/bb/e0a0a4c8af52f9b875d1f6791e15ad434a7aec
./.git/objects/c7/d26e3b75df3a81dab811269256a9d77b618d33
./.git/objects/64/4264e690e5a135425270758cd2d24592a2a881
./.git/objects/47/b41c013aaa0577f13edf17cb0b081cbfa468b3
./.git/hooks/commit-msg.sample
./.git/hooks/pre-receive.sample
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```

Here we specifed our search range by creating a lower bound and an upper bound when using the type and size command. From there we returned a list of files which were between 512 and 1024 bits. 

## Finding Files without remembering exact name
Traditonally, when using the "find" command, one must remeber the name of the file with case sensitivity in mind. This can cause some issues if you are having trouble remembering if you capitilizated a letter or not. To get around this we have the command "-iname" which is used when you dont remeber the exact name of the file. One thing to note though is that the file type must be specified. 

### Example 1
Input: 
```
tharun@Tharuns-MBP docsearch % find . -iname RR37.txt
```
Output:
```
./technical/biomed/rr37.txt
```

In this example, I did not remember if the rr at the beginning was uppercase or not so I used the -iname to help me find the file. 

### Example 2
Input:
```
tharun@Tharuns-MBP docsearch % find . -iname Ar297.txt
```
Output:
```
./technical/biomed/ar297.txt
```
In this example, I did not remember if the a or r was capitalized when searching for the file. But with the help of "-iname" the file was found very quicky. 

### Example 3
Input:
```
tharun@Tharuns-MBP docsearch % find . -iname Chapter-12.txt
```
Output:
```
./technical/911report/chapter-12.txt
```
In this example, I did not remember the exact name again but luckily "-iname" saved me and found the file I was trying to find. 

