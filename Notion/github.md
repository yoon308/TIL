# 0819

복습: No
작성일시: August 18, 2022 11:41 PM

git commit 수정하는 방법은 ppt92 영상

 링크 있음

work flow 정방향

add → commit → push

work flow 역방향

일 했던 것을 취소하는 방법 : 

rename

**`git`** mv [server.py](http://server.py/) [main.py](http://main.py/) : 그래서 어제 이상했던 거야 → git 없으면 git에 기록이 안돼 → repo 아니면 git 없어도 돼

undo : working dic에서 일했는데 마음에 안들 때. → add 이전

git **restore** [pikachu.py](http://pikachu.py/) → 가장 마지막 상태로 돌아가

git **restore** . 도 있다

unstaging : 내린다고 표현

git add [pikachu.py](http://pikachu.py/) → git reset HEAD [pikachu.py](http://pikachu.py/) ****→ git status

commit 

- git log > commit 보기

git commit `--amend` : 가장 최근의 commit 수정

이전의 commit을 수정할 땐 rebase 쓰긴하는데 추천하지는 않는다. 

 → 시나리오 영상은 있음.

   > git blame [pikachu.py](http://pikachu.py/) : 수정내용 보임

Reset commit : Revert

Reset 방법은 쓰지 않을 것

git revert **`--no-commit`** HEAD~3`..` → 순차적으로

- wayhome25
- 

poetry

gitflow

githubflow. → github에서 merge

git push `-u` origin fizzbuzz