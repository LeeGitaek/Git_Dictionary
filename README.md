#### Git_Dictionary
깃 명령어 모음집 
###### 작성자 : 이기택 / 틀린 사항 있으시면 알려주세요!

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

> * 커밋 후 삭제는 파일이 삭제 또는 변화된 것으로 간주한다. 따라서 커밋된 파일은 리셋으로 삭제한 후 정리해 주어야 함. 아래는 리셋 명령어 이다. 
>	```
>	$ git reset HEAD index.html
>	```

> * git 에서 파일 이름을 변경하는 명령어이다. git mv 기존 파일 이름 새로운 파일 이름 
>	```
>	$ git mv index.html home.html  
>	```

> * HEAD 
>	```
> $ git 에는 HEAD 라는 포인터 개념이 있음. HEAD 는 커밋을 가리키는 묵시적 참조 포인터이다. HEAD 는 최종적인 커밋 작업의 위치를 가리킨다. 처음 커밋할 때는 HEAD 의 포인터가 없음.
>	```

> * SNAPSHOT
>	```
> $ 스냅샷은 헤드가 가리키는 커밋을 기반으로 사진을 찍고, 이를 스테이지 영역과 비교하여 새로운 커밋으로 기록한다. 빠르게 버전의 차이점을 처리하고 용량을 적게 사용한다. 
>	```

