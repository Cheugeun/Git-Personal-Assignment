# PR의 기능과 사용평가
## PR의 기능

+ 자신이 작업한 내용을 다른 사람들과 공유가 가능

+ 코드 리뷰의 기반이 됨

+ 오픈 소스 프로젝트에 기여가능

+ Merge를 신중하게 할 수 있으며, 규칙을 정할 수 있음

+ 위 과정으로 코드 안정성을 높일 수 있음

## PR 보내는 방법

### 1. 기여하려는 저장소를 fork 한다.

![pr](https://user-images.githubusercontent.com/112995660/202906629-1bacc163-739a-46d8-b6b6-b94c240528fd.png)

### 2. 내 컴퓨터에 저장소를 Clone 한다.
Git bash에서 아래 명령어를 사용한다.

+ $ git clone [https://github.com/YOUR_FORK_USERNAME/YOUR_FORK.git ]

### 3. 원격 저장소 Remote 설정
Clone 해 온 저장소에 원격 저장소 설정 (PR 보낼곳을 추가해주는 것)

+ $ git remote add 원격저장소명 fork를 하기 전 원래 저장소 주소

> 주의할 점: 이 작업은 fork저장소를 원격저장소의 최신 커밋으로 내용을 변경해야 함

### 4. PR용 branch 생성
main브랜치가 아닌 코드를 수정하고 PR을 보낼 용도로만 사용할 브랜치를 생성해야 합니다.

+ $ git checkout -b 원하는 브랜치명

### 5. 코드 수정하기
새로만든 브랜치로 들어왔으니 오픈소스에서 기여할 부분을 코딩합니다.
    이후 명령어로 커밋합니다.

+ $ git add .
+ $ git commit -m "커밋메시지"

### 6. PR용 branch에 Push하기
이 부분에서 중요한 점은 꼭 PR용 branch에서 Push를 해야 합니다.

+ $ git push origin PR용 브랜치명

### 7. Fork한 Github 사이트
fork해온 나의 저장소로 이동 후

![fork](https://user-images.githubusercontent.com/112995660/203065435-a7010b57-a3cd-4bfc-a4dc-f027b8da6e74.png)

위에 사진속 활성화된 초록 버튼을 누르면 

![20221121_222221](https://user-images.githubusercontent.com/112995660/203065830-9d4cf16d-d5b5-4815-9c09-431c115e969d.png)

이 처럼 기여할 프로젝트 쪽 미리 설정된 양식이 있다면 양식과 규칙에 맞추어서 자신이 기여한 부분을 작성하면 된다.

이후 merge가 될때 까지 대기합니다.

### 8. PR 승인이후 필요없어진 branch 삭제하기
내가 보낸 PR이 승인이 되었다면 위에서 생성했던 브랜치는 삭제해도 됩니다

다음과 같은 명령어로 삭제합니다.

+ $ git branch -D 삭제할 브랜치 명
+ $ git push origin :삭제할 브랜치 명 (혹은 --delete 삭제할 브랜치 명)

각각 local과 remote branch를 삭제해주는 명령어 입니다.

### 9. 사용평가
저는 OSS수업과 팀과제를 위하여 PR을 많이 사용해보았습니다. 
    우선 협업을 하면서 별다른 소통없이 빠르게 작업물을 보낼 수 있는 것이 좋았고, PR을 받아주는 입장에선 내용을 확인하고 빠르게 merge 할 수 있는 것이 좋았습니다
    
