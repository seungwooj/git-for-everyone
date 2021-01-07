### 3. CLI : about Git commands

#### 3.0 CLI log, commit, push

- **git log** : shows the commit logs (end: :q)  
  cf> HEAD : Local에서의 위치 / remote : github repository / Origin : repository의 이름 / master : 가장 중심이 되는 branch
- **git add filename** : add a file to the staging area
- **git add .** : add all the file on the directory to the staging area
- **git commit -m "~~~"** : commit with messages
- **git push** : move all the files from staging area to the respitory area
- **-help** : shows possible options (도움말)

#### 3.1 Checkout and Hard Reset / Mixed Reset / Soft Reset

- **git checkout <<commit address>>** : to move HEAD to certain commit
- **git reset HEAD^ --hard ** (Hard Reset) : to move HEAD one commit back and **delete the resetted commit**  
  (커밋내용 취소 & 파일의 수정내용 kill)  
  (number of ^ : number of commits)
- **git push origin master --force** : to move origin (repository) be on the same point as the HEAD  
  (HEAD를 옮긴 것을 강제로 orgin에 push해 줘야 한다.)
- **git reset HEAD^** (Mixed Reset) : to move HEAD one commit back and **move the resetted commit to the unstaged area**  
  (커밋내용 취소 & 파일의 수정내용을 unstaged area에 보존)
- 이후에 다시 커밋하고 origin과의 sync를 맞춰준다 → **git push origin master --force** 사용
- **git reset HEAD^ --soft** (Soft Reset) : o move HEAD one commit back and **move the resetted commit to the staged area**  
  (커밋취소 & 파일의 수정내용을 staged area에 보존 -> 현재 작업중인 unstaged area의 파일과 구분이 가능)  
  → Mixed Reset이후 add하는 것과 동일

#### 3.4 Checkout Branches

- **git checkout -b <<branch-name>>** : to retain the changes made and **make a new branch** at the same time
- **git checkout <<commit address>> -b <<branch-name>>** : to create a new branch **with the specific commit address**
- to move between branches : **git checkout branch-name**
- **git push origin <<branch-name>>** : to push the contents of the specific branch to the origin (repository)

#### 3.5 Amending commits / .gitignore / removing

- **git commit --amend -m <<message>>**: to take the latest commit and modify it  
  (추가로 커밋할 내용을 빼고 커밋했을 경우, 해당 내용을 add하고 위 메세지를 입력하면 기존 커밋이 add한 내용이 포함된 커밋으로 변경됨)
- **git status** : to check the status of commits
- **touch .gitignore** : to create .gitignore file
- **git rm <<file-name >>** : to remove the file from stage area or git repository
- **git rm -r <<directory-name >>** : to remove the directory(folder) from stage area or git repository

#### 3.6 And more

- **git remote add <<repository-name>> <<repository-url>>** : 현재 local의 내용을 지정한 이름, 주소의 github repository에 추가  
  (현재 가지고 있는 내용을 다른 github/bitbucket/gitlab repository에 추가할 수 있다. -> git push <<repository-name>> master)
- **git clone <<url-of-repository>> <<folder-name>>**: github repository url의 내용을 local의 특정 folder로 받을 수 있음
