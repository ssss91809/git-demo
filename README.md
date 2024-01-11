# GET-DEMO

### 版本號檢視
■ git --version


### 建立全域端使用者

- git config --global user.name [your-name]
- git config --global user.email [your-email]


### 檢視git config

- git config --list

### vscode

- ctrl+shift+p
    - 選擇 Default
        - Terminal cmd

### 專案控管

- git init


### 檔案加入控管

- git add [filename]
	- Untrack => Added => Modified => Deleted
- git add .(所有都加)

### 檢視控管狀態

- git status

### 檢視物件內容(t: 型態 p: 內容)

- git cat-file -t sha(編碼簡稱)+4碼(2+4)
- git cat-file -p sha(編碼簡稱)+4碼(2+4)


### Added => Modified
	- git status
	- git add fiename(確認修改)

### 反悔修改 
	- git restore <filename>

### 檢視暫存區的內容
	- git ls-files -s

### 記錄到倉庫
	- git commit -m "message"
	- git commit -am(不用add)

### 檢視目前commit	
	- git log
	- git log --online

### 開啟VIM編輯器(linux)
-git commit -m "XXXX"
	- git commit
		- i (Insert)
		- esc 切換
			- :wq(儲存後離開)
			- :q!(直接離開)

### 合併上一個commit()
- git commit --amend commit[承諾]、amend[改正]

### 指令刪除
- git rm -f filename(強制刪除)
	-git restore --staged <filename>(恢復)

### 移出控管(將檔案從暫存/控管區移出)
-git rm --cached [filename]

### 檢視分支	
- git branch branch[分支]
	- 預設為master分支(需有commit才會出現)

### 新增分支
- git branch [name]


### 刪除分支
- git branch -D [name]


### 切換分支
- git checkout  commit[name]
- 回到過去的修正
	- 新增分支跟commit
	- 切回master進行合併
- 回到最新的位置
	-git checkout master (回到主分支)

### 新稱+切換
- git checkout -b(branch) [name]


### 合併分支 
-  git checkout master(需先切回主分支)
	- git merge [name]


### 合併衝突
- 不同分支改動同一個檔案(選擇合併方式)[A or B or A+B]
- git merge --aboort (反悔合併)



### 重置指令
- git reset commit-shal[name代碼]
- git reset --head commit-shal[name代碼]
- git reset ORIG_HEAD(恢復)
- git reset --hard Head (重置到最新commit)
- git reset --hard Head~1 (重置到前一個commit)


### 檢視所有歷程
- git reflog
	- 可以觀察 commmit -shal，進行reset(重置指令)

### github
- echo "# git-demo" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin https://github.com/ssss91809/git-demo.git
-git push -u origin main

### 綁定github雲端的倉庫
- git remote add origin https://github.com/ssss91809/git-demo.git
- git remote -v
	- 檢視綁定的雲端倉庫url

### 本地同步雲端
- git push
	- git push --set-upstream origin master
	- git push -u origin master
	- git push

### 複製專案
- git clone https://github.com/ssss91809/git-demo


### 新增/修正/刪除
- git add .
- git commit -m "message"

### 本地端同步雲端
- git push

### 雲端同步到本地端
- git pull