### 1. Basic Git Concepts

#### 1.0 Repository

- a folder with bunch of files where Git is watching at.
  cf> .files : not shown on finder
- .git : recodrds all the change history of the repository

#### 1.1 Commit

- make a commit : to set a record at the point in time to .git to know ~~what change has been made when~~

#### 1.2 Areas

- **working area**: where we ~~work on files~~ (creating, deleting, modifying..)
- **staging area** : where files are ~~ready to be committed~~ (we can choose whether the files to be included in the staging area or not)
- **repository area** : where files are ~~already committed~~ so that we have the snapshot of the files for the time the commit has been made to .git

#### 1.3 Branches

- By dividing branches, you can 1) change features and 2) update commanbase then 3) merge changed features to the updated commonbase  
  <img src="./img/branches.png" width=500px>
