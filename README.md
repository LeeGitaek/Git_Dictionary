#### Git_Dictionary
깃 명령어 모음집 
###### 작성자 : 이기택 / 틀린 사항 있으면 이슈로 알려주세요!

> * git 상태를 확인하는 명령어이다.
>	```
>	$ git status
>	```


> * git 의 스테이지 영역에서만 등록된 파일을 삭제하는 명령어이다.
>	```
>	$ git rm --cached index.html ---- 스테이지 삭제 
>	```



> * git 스테이지에 다시 등록하는 명령어이다. tracked 상태로 변경 
>	```
>	$ git add index.html 또는 git add * 등 사용 가능 
>	```

> * git 로그를 확인하는 명령어이다. 
>	```
>	$ git log 
>	```

> * git 간략 로그를 확인하는 명령어이다. 
>	```
>	$ git log --pretty=short
>	```

> * git 특정 커밋 로그를 확인하는 명령어이다.
>	```
>	$ git show 커밋 ID 
>	```

> * git 특정 파일의 로그를 확인하는 명령어이다.
>	```
>	$ git log index.html 
>	```

> * git 의 스테이지와 워킹 디렉토리를 비교하는 명령어이다.
>	```
>	$ git diff
>	```

> * git 커밋 간 차이를 확인하는 명령어 
>	```
>	$ git diff head 
>	```

> * 커밋 후 삭제는 파일이 삭제 또는 변화된 것으로 간주한다. 따라서 커밋된 파일은 리셋으로 삭제한 후 정리해 주어야 함. 아래는 리셋 명령어 이다. 
>	```
>	$ git reset HEAD index.html
>	```

> * git 에서 파일 이름을 변경하는 명령어이다. git mv 기존 파일 이름 새로운 파일 이름 
>	```
>	$ git mv index.html home.html  
>	```

> * git 에는 HEAD 라는 포인터 개념이 있음. HEAD 는 커밋을 가리키는 묵시적 참조 포인터이다. HEAD 는 최종적인 커밋 작업의 위치를 가리킨다. 처음 커밋할 때는 HEAD 의 포인터가 없음.

> * SNAPSHOT => 스냅샷은 헤드가 가리키는 커밋을 기반으로 사진을 찍고, 이를 스테이지 영역과 비교하여 새로운 커밋으로 기록한다. 빠르게 버전의 차이점을 처리하고 용량을 적게 사용한다. 


> * 파일 등록과 커밋을 동시에 하는 명령어 
>	```
>	$ git commit -a 
>	```

> * 커밋메세지를 등록하는 명령어 
>	```
>	$ git commit -m "message" 
>	```

> * 파일 등록과 커밋메세지 동시에 등록하는 명령어 
>	```
>	$ git commit -am "message" 
>	```

> * 빈 커밋 메세지를 작성할때 명령어 
>	```
>	$ git commit --allow-empty-message -m ""
>	```

> * 방금 전에 작성한 커밋 메세지를 수정해야 할 때 쓰는 명령어이다.
>	```
>	$ git commit --amend
>	```

> * 커밋 메세지를 작성할 때 -v 옵션을 사용하여 diff 내용을 추가할 수 있는 명령어이다.
>	```
>	$ git commit -v
>	```

> * 깃을 이용하면 수정한 파일을 커밋 전 마지막 내용으로 쉽게 되돌릴 수 있다. 바로 이전 커밋으로 되돌리는 명령어는 아래와 같다.
>	```
>	$ git checkout -- 수정파일이름
>	```

> * 원격 저장소의 이름 출력 
>	```
>	$ git remote 
>	```

> * 원격 저장소의 이름을 -v 옵션을 같이 사용하면 원격저장소의 별칭 이름과 URL 을 확인할 수 있음. 
>	```
>	$ git remote -v 
>	```

> * 로컬 저장소를 서버로 이용할 때 
>	```
>	$ git remote add 원격저장소별칭 폴더경로
>	```

> * 원격 저장소 연결 ( fetch 는 서버에서 가져옴, push 는 서버로 전송함)
>	```
>	$ git remote add 원격저장소별칭 원격저장소URL 
>	```

> * 별칭 이름 변경 및 정보 명령어 
>	```
>	$ git remote rename 변경전 변경후 
>	```

> * 원격저장소 상세한 정보 명령어 
>	```
>	$ git remote show 원격저장소별칭 
>	```

> * 원격 서버 삭제 
>	```
>	$ git remote rm 원격저장소별칭
>	```

> * push 서버에 전송  
>	```
>	$ git push 원격저장소별칭 브랜치이름 
>	```


> * push 서버에 전송  
>	```
>	$ git push 원격저장소별칭 브랜치이름 
>	```

> * 복제할 때 clone  
>	```
>	$ git clone 원격저장소URL 
>	```

> * pull 서버에서 내려받는 명령어 ( 원격 서버에서 현재 커밋보다 더 최신 커밋 정보가 있을 때 내려받음. )
>	```
>	$ git pull 
>	```


> * fetch 서버에서 수동으로 내려받는 명령어 ( fetch 명령어는 실행한 후에는 커밋이 추가된 것을 확인할 수 없습니다. )
>	```
>	$ git fetch 원격저장소URL 
>	```


> * fetch 는 자동병합을 하지 않기 때문에 내려받은 커밋을 로컬 저장소에 적용하려면 병합명령 merge 를 실행해야 함.
>	```
>	$ git merge 원격저장소별칭/브랜치이름
>	```


> * 협업에서 충돌을 피하기 위한 순서 
>	```
>	$ pull -> coding -> commit -> pull -> push 
>	```



> * branch 브랜치 목록 확인 
>	```
>	$ git branch
>	```


> * 브랜치이름만 입력할 경우, 현재 헤드 포인터를 기준으로 새로운 브랜치를 생성함. 직접 커밋 ID 까지 지정할 경우, 지정된 커밋ID를 기준으로 브랜치를 생성 (중복된 브랜치이름 안됨)
>	```
>	$ git branch 브랜치이름 커밋ID 
>	```


> * 브랜치 해시 - 깃의 저수준 명령어 rev-parse 를 사용하면 현재 브랜치가 어떤 커밋 해시 값을 가리키는지 확인가능 
>	```
>	$ git rev-parse 브랜치이름 
>	```

> * 브랜치 세부사항 확인 
>	```
>	$ git branch -v 
>	```

> * 브랜치 체크아웃 
>	```
>	$ git checkout 브랜치이름 
>	```

> * 파일로 체크아웃 
>	```
>	$ git checkout -- 파일이름 
>	```

> * 이전 브랜치로 이동 (대시(-) 기호는 이전 디렉터리를 의미) 
>	```
>	$ git checkout - 
>	```

> * 브랜치 로그내역 
>	```
>	$ git log --graph --all
>	```

> * 브랜치 로그 제한 출력 ( --more 옵션을 통해 출력될 커밋 개수를 제한)
>	```
>	$ git show-branch --more=10
>	```

> * 브랜치 생성과 체크아웃 동시에 하는 명령어 
>	```
>	$ git checkout -b 브랜치이름 
>	```

> * 리모트 브랜치 목록 
>	```
>	$ git branch -r 
>	```


> * 모든 브랜치 정보 
>	```
>	$ git branch -a
>	```

> * 복제 저장소의 트래킹 브랜치 정보 
>	```
>	$ git branch -vv
>	```

> * 헤드포인터 종류 
>	```
>	$ AHEAD 는 서버로 전송되지 않은 로컬 커밋이 존재할 경우이고, BHEAD는 로컬 저장소로 내려받지 않은 커밋이 있는 것.
>	```

> * 커밋 이동 
>	```
>	$ git checkout 커밋해시키 
>	```

> * 커밋 이동 (헤드포인터 기준) 
>	```
>	$ git checkout HEAD-1  (헤드를 기준으로 한 단계 전으로 이동 대시 기호 뒤에 있는 숫자를 바꾸면 원하는 단계로 이동할 수 있음.)
>	```

> * 커밋 돌아오기  
>	```
>	$ git checkout -
>	```


