# 과제 2 보고서📜

## GitHub repository URL

https://github.com/jeongmint/software-engineering02/

---

## ✏️ git 명령어 목록
[git add](##-git-add)ㅇ<br/>
[git branch](##-git-branch)ㅇ<br/>
[git checkout](##-git-checkout)ㅇ<br/>
[git clone](##-git-clone)ㅇ<br/>
[git commit](##-git-commit)d<br/>
[git config](##-git-config)d<br/>
[git init](##-git-init)d<br/>
[git log](##-git-log)<br/>
[git merge](##-git-merge)d<br/>
[git pull](##-git-pull)<br/>
[git push](##-git-push)d<br/>
[git rebase](##-git-rebase)<br/>
[git remote](##-git-remote)ㅇ<br/>
[git reset](##-git-reset)<br/>
[git status](##-git-status)d<br/>
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

---

<br>

## ✔️ 분기점을 사용하여 동시 작업하기
## git branch
branch를 뜬다 는 표현은 작업할 때 다시 돌아올 분기점을 만드는 것과 같습니다. git branch 뒤에 branch 명을 지정하여 생성할 수 있으며 branch 명을 지정하지 않으면 지금까지 생성된 branch 목록을 열람할 수 있습니다.
## git checkout
checkout 명령어는 branch를 지정한 branch를 사용할 수 있도록 셋팅해 주는 역할(orchid 색으로 최우측에 표시)을 합니다. -b 옵션을 통해서 branch 생성과 동시에 checkout을 수행할 수 있습니다.
```
$ git branch <브랜치명>
$ git branch -v <브랜치명>
$ git branch -a <브랜치명>
$ git branch
$ git checkout -b <브랜치명>
```
![branch](https://user-images.githubusercontent.com/39428260/117539360-41512100-b045-11eb-9c16-8a10b4ebe20d.png)
![checkout](https://user-images.githubusercontent.com/39428260/117539432-93924200-b045-11eb-8418-11b1377cc92d.png)
위와 같이 status 명령어를 수행하여 branch 가 origin이 된 것을 알 수 있습니다. <br>

branch 명령어의 -v 옵션은 커밋과 함께 branch 목록을 나열해 주고, -a 옵션은 로컬/리모트 저장소의 모든 branch 정보를 보여줍니다.

![branch commit](https://user-images.githubusercontent.com/39428260/117539757-09e37400-b047-11eb-8675-13268e1ee810.png)

하지만 현재 branch 는 origin 이라는 remote에 있는 origin branch 가 된 것이므로 "origin"이라는 branch 이름은 별로 좋지 않습니다(...) branch 이름은 역할에 따라 release, develop, hotfix, feature ... 등 규칙적인 형태로 팀원과 합의하여 이름을 작성하는 것이 건강합니다💪 

![branch2](https://user-images.githubusercontent.com/39428260/117539433-942ad880-b045-11eb-9da4-9c6c72a25861.png)

---

<br>

## ✔️ 작업 병합하기
## git status
먼저 git status를 통해 파일의 작업 상태를 확인할 수 있습니다. 파일 상태를 확인하는 작업은 자신이 어떤 명령어를 수행해야 할 지 초석이 되어 줍니다. 작업은 origin이라는 branch 에서 수행하였습니다. 작업한 파일을 병합하기 전에 add 하여 staged 해줍니다. <br>
![merge1](https://user-images.githubusercontent.com/39428260/117540022-28963a80-b048-11eb-984c-38a777d3052a.png)
![status1](https://user-images.githubusercontent.com/39428260/117540003-13211080-b048-11eb-846f-a58b81a67a7f.png)

여기서 commit 을 수행합니다. commit 내역을 자세히 보면 23 줄이 추가 되었으며 1 줄이 삭제되었다는 것을 알 수 있습니다. 이는 merge를 수행하기 위해 파일을 수정하였기 때문입니다. 이후에 git status 를 쳐보면, 커밋할 것이 없으며 working 내역이 깨끗하다는 상태를 알려줍니다.
![status2](https://user-images.githubusercontent.com/39428260/117540020-27fda400-b048-11eb-9d73-69e79ad2bab1.png)

<br>

## git merge
이제 작업을 병합해 봅시다! 현재 origin 이라는 branch에서 작업하였으니 main branch로 돌아갑니다.
![merge0](https://user-images.githubusercontent.com/39428260/117540021-28963a80-b048-11eb-9598-93ac58e57f80.png)

```
$ git merge <브랜치 명>
```
다음과 같이 main branch 에 origin branch 를 병합할 수 있습니다. 정상적으로 병합하면 맨 아래 줄 처럼 커밋할 때 나타난 파일 수정 내역과 동일한 내역이 나타나며 실제 파일을 열어보아도 작업 내역이 갱신되어 병합된 것을 확인할 수 있습니다.<br>
![merge3](https://user-images.githubusercontent.com/39428260/117540024-292ed100-b048-11eb-869c-7b8f97800341.png)


---

<br>

## ✔️ 작업 병합하기

## git reset

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
