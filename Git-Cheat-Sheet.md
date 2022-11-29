## 수업시간에 주로 사용하는  Git 명령어
### 수업을 시작하기전 하는 명령어 세팅
깃명령 별칭 지정 

+ ``` $ git config --global alias.log1 'log --oneline' ```
+ ``` $ git config --global alias.logg1 'log --graph --oneline' ```
+ ``` $ git config --global alias.st 'status' ```
+ ``` $ git config --global alias.sts 'status -s' ```

### 수업시간에 주로 사용한 명령어
+ 저장소를 생성  ``` $ git init 저장소명 ```
+ 저장소 이동 ``` $ cd 저장소명 ```
+ 기존 파일, 이전내용 삭제후 삽입 ``` $ echo '넣을 내용' > 넣을 파일명 ```
+ 내용 확인 ``` $ cat 확인할 파일명 ```
+ 상태 확인 ``` $ git status ```
+ 스테이지에 저장 ``` $ git add 스테이지명 ```
+ 깃 저장소에 저장 ``` $ git commit -m '커밋메시지' ```
+ 커밋 이력 확인 ``` $ git log ```
+ 브랜치 생성 ``` $ git branch 브랜치 명 ```
+ 브랜치 이동 ``` $ git checkout 이동할 브랜치 명 ```
+ 커밋간 차이 확인 ``` $ git diff ```
+ 브랜치 병합 ``` $ git merge ```
+ 브랜치 생성하면서 이동 ``` $ git checkout -b ```
