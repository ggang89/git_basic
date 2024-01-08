깃과 깃허브 첫 실습
=>책 "MUST HAVE 박미정의 깃&깃허브 입문' 참조

\*README의 확장자 md는 마크다운 형식의 파일을 의미한다. -마크다운 파일에서는 간단한 마크다운 문법구조를 이용해 들여쓰기,글꼴,헤더 등을 표현할 수 있다 -깃허브 원격 저장소에 README.md파일을 생성하면 해당 원격 저장소의 메인 페이지로 작동한다.
이러한 이유로 프로젝트에 대한 설명, 설치 방법 등을 설명하는데 README.md파일을 사용한다.

git init
---->깃 지역 저장소로 지정함
git config user.name "깃네임"
git config user.email "이메일 주소"
---->깃 지역 저장소에 사용자를 등록한다

VS code에서 새로운 파일을 생성한다.

git add 파일명
----> 터미널에서 git add 파일명을 입력하여 git에 파일을 추가한다

git commit -m "메시지 작성"

git log
----> 커밋이 잘 생성되었는지 확인

깃허브 페이제에서 새로운 원격 저장소 생성하기
new repositiry 클릭 후, Repository name(저장소 이름)을 짓고
Description에 간략한 설명을 적고 레퍼지토리 생성하기

생성된 원격 저장소의 주소를 복사하여
터미널에 git remote add origin 입력 후 붙여 넣기 (enter)

git push origin main
--->지역 저장소에 생성한 커밋을 원격 저장소에 등록한다
origin은 리모트 저장소 이름, main은 리모트 저장소 브랜치 이름이다

    >여기서 문제 발생
    error:src refspec main does not match any
    error: failed to push some refs to 'https://github.com/ggang89/git_basic.git'

    >push 뒤에 다른 이름으로 바꿔주거나
    >git romote -v로 연결을 확인해주고 다시 연결해주고 시도하고
    >git pull로 불러보고
    여러 시도를 하다가

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master

    이런 메시지가 떳고,
    >git push origin master 로 입력하니까 깃에 폴더가 생성됨
    확인해 보니 깃에 브랜치 이름이 master가 되었다

    그런데 이유를 모르겠다.
    다른 브랜치들은 main으로 다 생성되었는데, 왜 이것만 이런것인지

?? 브랜치가 main으로 바껴서 추가한 내용은 이제 main에 저장되는 것인가
