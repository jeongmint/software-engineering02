# 과제 2 보고서📜

## GitHub repository URL

https://github.com/jeongmint/software-engineering02/

---

## ✏️ git 명령어 목록
[git add](##-git-add)<br/>

---

<br>

## ✔️ git 을 최초로 사용할 때 

## git config
Git을 설치하고 나면 Git의 사용 환경을 적절하게 설정해 주어야 합니다. 환경 설정은 한 컴퓨터에서 한 번만 하면 되며 설정한 내용은 Git을 업그레이드 해도 유지됩니다.

```
git config --global user.name "Jeong Min Choi"
git config --global user.email "tangerine_t@naver.com"
```
![git_config](https://user-images.githubusercontent.com/39428260/117537713-cdf7e100-b03d-11eb-8ae8-0a0e10dd4cf8.png)

여기서 --global 옵션은 어느 저장소에든 해당 내용을 유지하며, 프로젝트 마다 다시 설정하고 싶으면 해당 옵션을 제외하면 됩니다.

```
git config --list
```
해당 명령어를 수행하면 다음과 같이 설정이 적용된 리스트를 볼 수 있습니다.
![git_config_list](https://user-images.githubusercontent.com/39428260/117537897-b3723780-b03e-11eb-9700-98a1b5e697f1.png)



<br>

## git init

<br>

---

<br>

## git add
<br>
git add 명령은 stage에 추가하는 작업을 수행합니다. 파일을 새로 추적하는 내용은 status를  실행하면 알 수 있습니다.

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
