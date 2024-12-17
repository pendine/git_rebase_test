# git_rebase_test


진행순서
```
1)main - MD 작성
		\
		2)branch1  - A - B - C
			\
			3)branch2
					\         
					4)branch3 - D	-	- - - H`
										/			        \
										E - F - G - H - H1
									(깃 로그 리베이스)
H-1 <- (지금 여기)
깃 로그 리베이스를 사용할때
별도의 브랜치인 로컬 브랜치 branch3-local 만들고
작업이 끝난후 branch3-local에서 
git rebase -i branch3 명령어를 사용하면 

branch3-local에서 작업했던 로그들만 나오지만
git rebase -i HEAD~정수 를 입력하게 되면
헤드에서 입력한 정수까지의 모든 깃로그를 관리하게됨.

따라서 내가 작업하려던 방식대로 간다면 git rebase -i "내가 뻗어나온 브랜치" 로 관리하는게 맞음
HEAD~정수 <= 비 권장
```