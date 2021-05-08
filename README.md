# 과제 2 보고서📜

## GitHub repository URL

https://github.com/jeongmint/software-engineering02/

---

## ✏️ git 명령어 목록
[git add](##-git-add)<br/>
[git branch](##-git-branch)<br/>
[git checkout](##-git-checkout)<br/>
[git clone](##-git-clone)<br/>
[git commit](##-git-commit)<br/>
[git config](##-git-config)<br/>
[git init](##-git-init)<br/>
[git log](##-git-log)<br/>
[git merge](##-git-merged)<br/>
[git pull](##-git-pull)<br/>
[git push](##-git-push)<br/>
[git rebase](##-git-rebase)<br/>
[git remote](##-git-remote)<br/>
[git reset --hard](##-git-reset---hard)<br/>
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
이제 branch를 병합해 봅시다! 현재 origin 이라는 branch에서 작업하였으니 main branch로 돌아갑니다.
![merge0](https://user-images.githubusercontent.com/39428260/117540021-28963a80-b048-11eb-9598-93ac58e57f80.png)

```
$ git merge <브랜치 명>
```
다음과 같이 main branch 에 origin branch 를 병합할 수 있습니다. 정상적으로 병합하면 맨 아래 줄 처럼 커밋할 때 나타난 파일 수정 내역과 동일한 내역이 나타나며 실제 파일을 열어보아도 작업 내역이 갱신되어 병합된 것을 확인할 수 있습니다.<br>
![merge3](https://user-images.githubusercontent.com/39428260/117540024-292ed100-b048-11eb-869c-7b8f97800341.png)

<br>

## git log
```
$ git log
```
git log 명령어는 다양한 옵션과 함께 커밋 상태, branch내역 그리고 checksum(커밋마다 부여되는 고유한, 엄청 긴 숫자와 문자의 조합)을 보여줍니다. 이를 커밋 히스토리 라고도 합니다.

![log](https://user-images.githubusercontent.com/39428260/117540730-75c7db80-b04b-11eb-96f4-e47ff63b6f29.png)

<br>

보통 저는 다음과 같이 --oneline, --pretty, --decorate, --graph, -all 옵션 등을 조합하여 커밋 그래프와 branch 상태를 시각적으로 보기 위해 log 명령어를 사용합니다.

```
$ git log --pretty --oneline
$ git log --oneline --decorate --graph --all
```
![pretty](https://user-images.githubusercontent.com/39428260/117540833-fdade580-b04b-11eb-9f38-e5ee13ebdc48.png)


merge의 그래프를 그려보면 다음과 같이 하나의 브랜치로 모아지는 형태가 됩니다.

![merge-branch](https://user-images.githubusercontent.com/39428260/117540582-fcc88400-b04a-11eb-8c5b-852afe7b8d59.png)

---

<br>

## ✔️ 병합 시 충돌 제어하기

![collision-origin](https://user-images.githubusercontent.com/39428260/117541192-ae68b480-b04d-11eb-8b9a-518d246111fe.png)
![Inkedcollision-issue_LI](https://user-images.githubusercontent.com/39428260/117541194-b163a500-b04d-11eb-8356-ae1f9ad8728a.jpg)

일단 origin, issue branch에 각각 동일한 라인에 이모지만 바꿔 두었습니다. 하지만 두 파일을 병합하기 위해 merge를 수행하면 다음과 같이 conflict가 뜹니다. 이는 파일이 서로 동시 작업되었기 때문에 어떤 것을 병합할 지 몰라 충돌한 것이기 때문입니다.

![conflict](https://user-images.githubusercontent.com/39428260/117541294-2931cf80-b04e-11eb-83d4-7822f23efb1b.png)

다음과 같이 나타난 코드에 <<<< HEAD 와 >>>> issue 사이의 작업 내역을 하나로 뭉쳐주고 쓸데 없는 코드 또한 지워준 후 다시 커밋을 수행하면 정상적으로 동작합니다. <br>

![change-conflict](https://user-images.githubusercontent.com/39428260/117541330-5c745e80-b04e-11eb-8697-9754f89ba2bc.png)

이렇게 merge를 수행하고 push를 수행하면 github로 다시 돌아가서 pull request를 수행해야 합니다. 충돌과 관련한 적당한 메시지를 적고 작업 내역을 합쳐도 괜찮을지 request를 남기면 협업에 굉장한 도움이 됩니다. pull request 도 끝났고, merge 도 끝났다면 해당 branch는 삭제해 버리도록 합니다. <br>

![request1](https://user-images.githubusercontent.com/39428260/117541477-fdfbb000-b04e-11eb-973d-0cd2c6236a8a.png)

<br>

## ✔️ 커밋 삭제하기
## git reset --hard

git reset 중에서도 --hard 옵션을 통해서 커밋 기록을 삭제해 보도록 합니다.

![reset0](https://user-images.githubusercontent.com/39428260/117541684-e8d35100-b04f-11eb-83b1-a0667f0603f3.png)

아뿔싸! commit 메시지에 오타가 났습니다😇 커밋 메시지를 삭제해 보겠습니다.
```
$ git reset --hard HEAD^
$ git reset --hard <체크섬>
```

![reset-check](https://user-images.githubusercontent.com/39428260/117541686-e96be780-b04f-11eb-82ca-caba3aaf0f66.png)

reset 명령어를 수행한 후 git log를 확인 해 보면 정상적으로 커밋이 삭제된 것을 확인할 수 있습니다.

<br>

## git rebase
다른 방식으로도 병합을 수행할 수 있는데 rebase 명령어는 merge와 사뭇 결이 다릅니다. merge는 branch를 하나로 모으는 역할을 하는데, rebase는 branch를 살리면서(base로 두고) 같이 뻗어나가는 형식으로 병합을 수행합니다.

![rebase-branch](https://user-images.githubusercontent.com/39428260/117540988-ba07ab80-b04c-11eb-9a2a-23d6b6462a48.png)

merge와 동일하게 brach를 떠서 작업한 후 develop branch, feature branch 각각에 겹치면서 다른 코드 변경을 수행합니다. 
![rebase1](https://user-images.githubusercontent.com/39428260/117541942-5f248300-b051-11eb-9bb6-5bcbfd7ae836.png)
![rebase2](https://user-images.githubusercontent.com/39428260/117541944-5fbd1980-b051-11eb-8858-e0586c00534c.png)

merge 는 덮어 씌우고자 하는 branch에 가서 checkout을 한 반면, rebase 는 덮어 쓰고 싶은 brach에 가서 checkout을 하고 branch 를 병합합니다.
```
git rebase <브랜치 명>
```

![rebase6](https://user-images.githubusercontent.com/39428260/117540994-bbd16f00-b04c-11eb-86ab-c0b419bec8f2.png)

여기서도 충돌을 제어하기 위해 해당 branch로 돌아가 가볍게 코드를 고쳐주도록 합시다.

![rebase-result](https://user-images.githubusercontent.com/39428260/117542081-0ef9f080-b052-11eb-86e4-3d84845cc310.png)

그 후 add 로 stage에 올리면 다음과 같이 main branch 가 (develop | REBASE 1/1) 상태가 된 것을 알 수 있습니다.
<br>


<br>

## ✔️ 동시 작업 후 갱신하기
## git pull


```
$ git pull <리모트> <브랜치 명>
```

git pull 명령어는 원격에 저장된 git 프로젝트의 현재 상태를 다운받고 현재 위치한 브랜치로 병합해 줍니다. 그렇기 때문에 다른 작업 내역과 충돌이 일어나지 않도록 수시로 git pull을 하여 갱신을 해야 협업에 무리가 없습니다.

![pull](https://user-images.githubusercontent.com/39428260/117542383-62b90980-b053-11eb-90e7-fd45761235d8.png)


<br>

---

<br>

## ✔️ 커밋에 태그 달기
## git tag
git tag 명령어는 커밋에 태그를 달아 줍니다. tag는 말 그대로 해당 커밋을 빠르게 찾을 수 있게 도와주며 index와 같은 역할을 합니다. -a 옵션을 활용하면 tag에 메시지를 입력할 수 있습니다. git tag 명령어는 현재 생성된 tag의 목록을 나열합니다.
```
$ git tag <태그 명> <체크섬>
$ git tag -a <태그 명> <체크섬>
$ git tag
```
![tag1](https://user-images.githubusercontent.com/39428260/117542707-a52f1600-b054-11eb-839c-85b17c1da0d0.png)
![tag2](https://user-images.githubusercontent.com/39428260/117542709-a5c7ac80-b054-11eb-9ec5-61b226885e60.png)

```
$ git show <태그 명>
```
show 명령어를 태그 이름과 함께 수행하면 해당 태그의 모든 내역(커밋 메시지, 작성자, 커밋 날짜, 태그 메시지)을 포함하여 표시해 줍니다.

![tag3](https://user-images.githubusercontent.com/39428260/117542712-a5c7ac80-b054-11eb-81bc-0cbc00785643.png)

하지만 tag 명령어는 add 명령어로 staged 되지 않으며 commit 으로 내역을 원격에 전달할 수 없기 때문에 다음과 같이 전체 태그 내역을 push 해주어야 합니다.

```
$ git push --tag
```

![tag4](https://user-images.githubusercontent.com/39428260/117542713-a6604300-b054-11eb-9cbc-6fd6ac123fec.png)

<br>
git log를 수행해 보면 다음과 같이 tag가 커밋 히스토리와 함께 나타나는 것을 볼 수 있습니다.

![tag5](https://user-images.githubusercontent.com/39428260/117542714-a6604300-b054-11eb-8810-8e20cca1783e.png)


<br>

---

## ● git 명령어 사용 여부

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
