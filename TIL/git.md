

# Git

> Git은 분산버전관리시스템(DVCS)의 일종이다.
>
> 소스코드의 이력을 남기고 관리할 수 있다.



## 준비사항

윈도우에서 git을 쓰기 위해서는 [git bash](https://gitforwindows.org/)를 설치한다.

컴퓨터에 처음 설치하는 경우 커밋을 작성하는 사람(author)를 global로 설정해야 한다.

```bash
$ git config --global user.name 'user'
$ git config --global user.email 'user'@'localhost.com'
```



## 로컬 저장소 활용하기

### 1. 저장소 생성

```bash
$ git init
Initialized empty Git repository in
C:/Users/HPE/Desktop/TIL/.git/
(master) $
```

* git 저장소를 생성하면, 해당 디렉토리에 `.git`폴더가 생성된다
* `(master)`는 현재 작업 중인 브랜치가 master라는 의미를 가지고 있다.



## 2. `add`

* working directory(작업 공간) 에서 Staging area로 해당 파일을 이동시키기 위해서는 아래의 명령어를 사용한다.



* `add` 전

```bash
$ git add markdown.md # 특정 파일
$ git add images/ #특정 폴더
$ git add . # 현재 디렉토리
```

```bash
$ git status
On branch master

No commits yet
# 트래킹이 되지 않고 있는 파일들
# => commit 이력에 한번도 저장되지 않은 파일들, 즉 새로 생성된 파일.
Untracked files:
# 커밋이 될 것들에 포함시키기 위해서는 add
# => staging area에 담으려면 add
 (use "git add <file>..." to include in what will be committed)
 			git.md
 			images/
 			markdown.md
 			
 nothing added to commit but untracked files present (use "git add" to track)
```

* `add` 후

``` bash
$ git status
On branch master

No commits yet
# 커밋 될 변경사항들
# => staging area에 있는 파일들
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    a.txt
# working directory에 있는 파일들
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        images/
        markdown.md

```



## 3. `commit`

* 이력을 남기기 위해서는 아래의 명령어를 활용한다.

```bash
$ git commit -m '커밋메시지'
[master (root-commit) 76ddcf5] markdown 활용법 추가'
 3 files changed, 125 insertions(+), 1 deletion(-)
 delete mode 100644 a.txt
 create mode 100644 "images/\353\270\214\353\243\250\353\213\210.gif"
 create mode 100644 markdown.md
```

* 커밋메시지는 해당 이력을 나타낼 수 있도록 작성하는 것이 중요하고, 항상 일관적으로 작성하자.
* 커밋 내역은 아래의 명령어로 확인 가능하다

```bash
$ git log
$ git log --oneline
$ git log -1
```



