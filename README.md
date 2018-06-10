# fds10-cowoking
fds10기 수강생분들이 정리한 수업내용

---
### git fork한 repository 최신으로 동기화하기

참고 사이트 : [[Git] Fork 한 repository 최신으로 동기화하기](https://json.postype.com/post/210431)

- 원본 repository를 remote repository로 추가
```
$ git remote -v
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
```
- 동기화해오고 싶은 원본 repository를 upstream 이름으로 추가
```
$ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
- upstream repository가 제대로 추가되었는지 확인
```
$ git remote -v
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```
- git fetch로 upstream repository의 내용 불러오기
```
$ git fetch upstream
remote: Counting objects: 75, done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 62 (delta 27), reused 44 (delta 9)
Unpacking objects: 100% (62/62), done.
From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
 * [new branch]      master     -> upstream/master
```
- upstream repository의 master branck로부터 나의 local master branch로 merge한다.
```
$ git checkout master
Switched to branch 'master'
```
```
$ git merge upstream/master
Updating a422352..5fdff0f
Fast-forward
 README                    |    9 -------
 README.md                 |    7 ++++++
 2 files changed, 7 insertions(+), 9 deletions(-)
 delete mode 100644 README
 create mode 100644 README.md
```
 - local repository에서 한 과정을 remote repository로 push
```
 $ git push origin master
```