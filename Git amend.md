# Git

> amend를 통해 commit 날짜 바꾸기
>
> 기존에 존재하고 있는 repository에서 만들기

## 1. add & commit

* 먼저 파일을 추가한 뒤 `add`를 한다

* 그 다음 `commit`

  ```bash
  $ git add .
  $ git commit -m 'add'
  
  [master 79f8a25] add
   1 file changed, 15 insertions(+), 34 deletions(-)
   rewrite "AlgorithmJobs/2.\353\260\260\354\227\264/2_11binary_solution.c" (89%)
  
  
  ```


## 2. amend & push

* git commit --amend --no-edit --date "원하는 날자"
* git push origin master

```bash
$ git commit --amend --no-edit --date "31 July 2020 09:00:00 KST"

[master 8714f5c] add
 Date: Fri Jul 31 09:00:00 2020 +0900
 1 file changed, 15 insertions(+), 34 deletions(-)
 rewrite "AlgorithmJobs/2.\353\260\260\354\227\264/2_11binary_solution.c" (89%)



```

```bash
$ git push origin master

Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 8 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (18/18), 1.58 KiB | 540.00 KiB/s, done.
Total 18 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), completed with 2 local objects.
To https://github.com/dragontls123/algorithm.git
   7f79563..8714f5c  master -> master

```

## 3. 안되는 경우

> 주소가 뒤틀려서 안될 경우가 생긴다
>
> 
>
> * git remote add origin 원하는 repository의 주소
> * git push -u origin master

```bash
$ git remote add origin https://github.com/dragontls123/c.git
$ git push -u origin master
```

주소를 맞춰주면 잘 된다

잔디밭도 변경된 날짜에 심어진다.

