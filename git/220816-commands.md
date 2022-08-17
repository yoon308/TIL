
<학습목표>

`CLI` 기반으로 수업을 진행하면서 ` CLI`를 사용해본다.
CLI 반대 개념은 `GUI` 기반으로 마우스를 사용해서 finder나 파일탐색기를 통해 file과 directory에 접근하는 것이다. CLI는 키보드로만 제어한다. 

CLI : Command-Line Interface
GUI : Graphical User Interface


 * 데이터 사이언티스트가 왜 git을 사용해야할까?
  > 데이터 분석에 대한 소스코드를 남길 수 있기 때문이다.

 * `git`은 도구, `github`는 웹서비스로 저장소 역할



<간단한 용어 정리>

`~` :  틸드라고하고, 지금 로그인한 사용자가 권한없이 사용할 수 있는 최상위 폴더 위치를 나타낸다.
'cd' : 마우스에서 더블 클릭 기능과 같다.
`ls` : 하위 파일을 나타낸다.
`..` : 상위 폴더를 나타낸다.

> flag, 옵션들

`-a` : 숨긴 파일 모두 나타낸다. ex) .test 
`-l` : 디테일한 내용까지 모두 나타낸다.



<디렉토리>
`mkdir` 디렉토리 이름 : 새 디렉토리 만들기
`rm -r` 디렉토리 이름 : 디렉토리 삭제
    > r : ricursive (되풀이하는)


<파일>
`touch` 파일 이름.확장자 : 새 파일 만들기
    > .txt, .md, .py, .js 같이 텍스트 기반 파일만 가능 
	    *md : markboard
    > .db, .hwp, .xlsx 같은 확장자는 응용프로그램이 필요하기 때문에 불가능
`mv` 파일 디랙토리 : 파일을 원하는 디렉토리로 이동하기
    > mv ../test.txt . :  상위 디렉토리에 있던 파일을 현재 디렉토리로 이동
`cp` 파일 : 파일 복제
    > cp ../server.py . : 상위 디렉토리에 있던 파일을 현재 디렉토리로 복제
`rm` 파일 : 파일 삭제
    > *(와일드카드) 사용가능
'mv' 파일 새파일이름 : 파일 이름 바꾸기


<Vim>
로그를 남길 때 vim을 사용하는데 노트같은 기능이다.
로그를 남길 때 normal 모드에서 `i`를 눌러서 insert 모드로 변환한 뒤 로그를 작성한다.
다시 normal 모드 돌아갈 때는  `esc` 키로 돌아간다.
저장하고 나갈 때는 `shift + ;` -> :wq
저장하지 않고 나갈 때는 `shift + ;` -> :q!

<cat>
`cat` 파일이름 : 들어가지 않고 텍스트 파일을 shell에서 뿌려 보고싶을 때 사용한다.
    > cat : concatenated(?) (연결의)


<2가지 가상환경>
staging과 localrepo
									
working directory -------------> `staging` --------------> `localrepo` -------------> remote repo
		    `git add`		    `git commit`    		`git push`	

<git의 환경설정>
$ git config --global user.name "당신의유저네임"
$ git config --global user.email "당신의메일주소"
$ git config --global core.editor "vim"
$ git config --global core.pager "cat"
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --"

<repo 만들기>
<1. git init>
shell에서 repo 만들기
	주의> Do not `git init` on any other directories : 한 디렉토리를 git 전용으로 써버린다.
<2. git clone>
github에서 저장소(remote)를 만들고 통째로 내 컴퓨터로 복사

<git status>
untracked files : git이 여태까지 모르던 새로운 파일이 생겼다는 의미

<git add status>

<first git push origin main>
github에서 token만들기, 체크박스 모두 체크
shell에서 username & password(token값 입력)


* repo에서 파일만들고 저장하기
git add 파일 -> git status > new file ->  vim 파일 열고 작성 -> git commit -> git status -> git push origin main > main 성공





