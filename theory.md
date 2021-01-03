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

- By dividing branches, you can 1) change contents at feature branch and 2) update master branch then 3) merge feature branch to the updated commonbase  
  <img src="./img/branches.png" width=500px>
- 작업순서:
  1. Create a new branch from the master branch (lets say, feature branch)
  2. At feathre branch, make modification and make a commit at the feature branch
  3. At master branch, update the contents
  4. At feature branch, update from default branch **(Merge master branch into feature branch)**
  5. At master branch, **merge feature branch into master branch**
  6. Delete feature branch
