# 과제 2 보고서📜

## GitHub repository URL

https://github.com/jeongmint/software-engineering02/

---

## ✏️ git 명령어 목록
[git add](##-git-add)<br/>
[git branch](##-git-branch)<br/>
[git checkout](##-git-checkout)<br/>
[git clone](##-git-clone)<br/>
[git commit](##-git-add)<br/>
[git config](##-git-config)<br/>
[git init](##-git-init)<br/>
[git log](##-git-log)<br/>
[git merge](##-git-merge)<br/>
[git pull](##-git-pull)<br/>
[git push](##-git-push)<br/>
[git rebase](##-git-rebase)<br/>
[git remote](##-git-remote)<br/>
[git reset](##-git-reset-)<br/>
[git status](##-git-status)<br/>
[git tag](##-git-tag)<br/>

---

<br>

## ✔️ git 을 최초로 사용할 때 
<br>

## git config
Git을 설치하고 나면 Git의 사용 환경을 적절하게 설정해 주어야 합니다. 환경 설정은 한 컴퓨터에서 한 번만 하면 되며 설정한 내용은 Git을 업그레이드 해도 유지됩니다.

```
$ git config --global user.name "Jeong Min Choi"
$ git config --global user.email "tangerine_t@naver.com"
```
![git_config](https://user-images.githubusercontent.com/39428260/117537713-cdf7e100-b03d-11eb-8ae8-0a0e10dd4cf8.png)

여기서 --global 옵션은 어느 저장소에든 해당 내용을 유지하며, 프로젝트 마다 다시 설정하고 싶으면 해당 옵션을 제외하면 됩니다.

```
$ git config --list
```
해당 명령어를 수행하면 다음과 같이 설정이 적용된 리스트를 볼 수 있습니다.
![git_config_list](https://user-images.githubusercontent.com/39428260/117537897-b3723780-b03e-11eb-9700-98a1b5e697f1.png)

<br>

## git clone
github 사이트에서 생성한 repository를 로컬 PC로 가져오는 작업을 수행합니다. "sotfware-engineering02" 라는 저장소를 만든 후 초록색 code 버튼을 눌러 주소를 복사할 수 있습니다.

![clone](https://user-images.githubusercontent.com/39428260/117538005-2085cd00-b03f-11eb-91a9-243c6e0c3e64.png)

복사한 주소를 다음과 같이 git clone 뒤에 "" 를 사용하여 붙여 넣습니다.

```
$ git clone "https://github.com/jeongmint/software-engineering02.git"
```

![copy](https://user-images.githubusercontent.com/39428260/117538076-70fd2a80-b03f-11eb-9d37-bd3acded6e1c.png)


<br>

## git init
git init 의 init은 "initialize(초기화)"를 뜻합니다. 이 명령어를 입력하기 전까지는 일반 디렉토리였지만, git init 으로 초기화를 시키면 해당 디렉토리를 로컬 깃 저장소로 등록합니다.
```
$ git init
```
저는 다음과 같이 cd 명령어로 software-engineering02 저장소의 폴더로 이동을 한 후 초기화를 해 주었습니다.

![init](https://user-images.githubusercontent.com/39428260/117538151-cfc2a400-b03f-11eb-8c33-52bb3f225255.png)

<br>

## git remote
git remote 명령은 프로젝트의 리모트 저장소를 관리하는 명령어입니다. -v 옵션으로 등록된 저장소 이름과 github URL을 표시할 수 있습니다.
```
$ git remote
$ git remote -v
```

![remote](https://user-images.githubusercontent.com/39428260/117538474-4f04a780-b041-11eb-90a0-6bbe141527a7.png)


<br>

---

<br>

## ✔️ 커밋(commit) 수행하기

## git add
git add 명령은 stage에 "unstaged" 상태로 수정 후 저장만 되어 있는 파일을 "staged" 상태로 추가하는 작업을 수행합니다. 파일을 새로 추적하는 내용은 status를  실행하면 알 수 있습니다.<br>


```
$ git add .
$ git add <파일명>
```
여기서 git add . 명령어를 수행하면 우리 저장소에는 .gitignore 파일이 없지만, .gitignore 파일에서 제어된 파일을 제외하고 stage에 올릴 수 있습니다.<br>

![add](https://user-images.githubusercontent.com/39428260/117538701-57111700-b042-11eb-8e6a-d14e6428276f.jpg)

<br>

## git commit
add 명령어로 staged 상태로 파일을 올려두었다면 바로 수행해야 할 작업은 commit 입니다. commit은 번역하면 "-을 보내다" 정도로 해석될 수 있는데 협업 상황에서 현재 파일을 github에 올림(사실은 올리기 직전)과 동시에 코드 변경과 관련된 메시지를 덧붙여 줍니다.<br>
```
$ git commit -m "Set my project"
$ git commit -a -m "Set my project"
```
-a -m 옵션을 동시에 붙여주면 add 명령을 따로 수행하지 않고, git add 명령과 git commit 명령을 동시에 수행할 수 있습니다. <br>
![commit](https://user-images.githubusercontent.com/39428260/117538606-eec23580-b041-11eb-93f3-e4a26dbf3716.png)

<br>

## git push
커밋을 하는 방법은 단순하게 [add-commit-push] 로 이어진다고 할 수 있습니다. git push를 수행하면 그동안 로컬 저장소에서 commit된 이력들이 원격 저장소(github repository)로 전송이 됩니다.

```
$ git push <원격 저장소명> <브랜치명>
```
![push](https://user-images.githubusercontent.com/39428260/117539124-24681e00-b044-11eb-9969-c2e0171206f4.png)
<br><br>

## git status


---

## git 명령어 사용 여부

<br>

| 명령어 | 사용 여부 |
| --- | --- |
| add | ○ |
| branch | ○ |
| checkout | ○ |
| clone | ○ |
| commit | ○ |
| config | ○ |
| init | ○ |
| log | ○ |
| merge | ○ |
| pull | ○ |
| push | ○ |
| rebase | ○ |
| remote | ○ |
| reset --hard | ○ |
| status | ○ |
| tag | ○ |
