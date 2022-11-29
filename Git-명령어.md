# add
새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기

``` $ git add <파일명> ```
# commit
파일의 일부를 스테이징 하기

``` $ git commit -m <메시지> ```
# log
모든 이력 보기

``` $ git log ```
# show
커밋 정보를 확인 하는 명령어

``` $ git show ```

# clone
저장소 복제하기

``` $ git clone <저장소> ```

마지막 200개의 커밋만 포함하여 저장소 복제

``` $ git clone --depth 200 <저장소> ```

새로운 원격 저장소 추가

``` $ git remote add <원격 저장소> <저장소 url> ```

# push
지역 브랜치를 원격 브랜치에 푸싱하기

``` $ git push <원격 저장소><지역 브랜치>:<원격 브랜치> ```

지역 브랜치를 동일한 이름의 원격 브랜치에 푸싱하기

``` $ git push <원격 저장소><지역 브랜치> ```

새로운 로컬 브랜치를 원격 저장소에 푸싱하기

``` $ git push <원격 저장소><지역 브랜치> ```
# pull
원격 저장소에서 변경사항을 가져와 현재 브랜치에 합치기

``` $ git pull <원격 저장소> ```

origin 저장소에서 변경사항을 가져와 현재 브랜치에 합치기

``` $ git pull ```
# fetch/merge
origin 저장소에서 합치지 않고 지역 브랜치 변경사항 가져오기

``` $ git fetch ```

원격 저장소에서 합치지 않고 지역 브랜치로 변경사항 가져오기

``` $ git fetch <원격저장소> ```

# remote
원격 저장소에서 쓸모가 없어진 원격 브랜치 제거

``` $ git remotee prune <원격 저장소> ```

원격 저장소를 제거하고 관련된 브랜치도 제거

``` $ git remote rm <원격 저장소> ```
# branch, checkout
지역 브랜치 목록 보기

``` $ git branch ```

원격 브랜치 목록 보기

``` $ git branch -r ```

지역과 원격을 포함한 브랜치 목록 보기

``` $ git branch -a ```

브랜치 생성하기

``` $ git branch <브랜치명> ```

다른 브랜치로 이동하기

``` $ git checkout <브랜치명> ```

브랜치 생성하면서 이동하기

``` $ git checkout -b <브랜치명> ```

다른 시작 지점에서 브랜치 생성

``` $ git branch <새로운 브랜치> <브랜치 생성할 위치> ```

브랜치 덮어쓰기

``` $ git branch -f <기존 브랜치> <브랜치를 생성할 위치> ```

브랜치 옮기기 or 이름 변경

``` $ git checkout -m <기존 브랜치> <새로운 브랜치> ```

브랜치 삭제하기

``` $ git branch -d <브랜치명> ```
# switch
> checkout 기능에서 브랜치 변경하는 부분만을 담당하는 명령어

``` $ git switch <브랜치명> ```
# fast forward merge
> 현재 브랜치의 HEAD가 대상 브랜치의 HEAD까지로 옮기는 merge

``` $ git swich <현재 브랜치> ```
``` $ git merge <대상 브랜치> ```
> 순서대로 사용 
# 3-way mergee
여러 개발자와 협업을 할 때 사용하는 병합법이다. 이 병합을 하려면 우선

1. 나의 브랜치 커밋
2. 남의 브랜치 커밋
3. 두 브랜치의 공통 조상이 되는 커밋
> git은 공통 조상 커밋을 자동으로 찾아준다.

``` $ git merge <대상 브랜치> ```
# rebase
커밋된 브랜치의 변경사항을 Patch로 만들고 변경사항을 merge하는 것

``` $ git rebase <대상 브랜치> ```
# reset
시간을 아예 과거 특정 커밋으로 되돌린다.

![image](https://user-images.githubusercontent.com/112995660/204544784-d9fb2b29-b820-4d12-bad6-fcd7c03891c6.png)

위 그림에서

``` $ git reset --hard a0fvf8 ```

을 하면 'a0fvf8' commit으로 돌아간다는 뜻이다.

![image](https://user-images.githubusercontent.com/112995660/204545016-74c49835-b3b0-4b7e-a463-e020c65adc6d.png)

commit 히스토리에 C, D 커밋이 아예 사라진다.

# revert
현재에 있으면서 과거의 특정 커밋들만 없던 일로 만든다.

![image](https://user-images.githubusercontent.com/112995660/204545204-c8ba72a5-d7fb-4890-9cf4-6255cb900a9d.png)

revert를 이용해 B 커밋으로 돌아가려면

``` $ git revert 5lk4er ``` 
> D 커밋 revert

``` $ git revert 76sdeb ```
> C 커밋 revert 

위와 같이 뒤 커밋부터 순차적으로 revert 해준다.

![image](https://user-images.githubusercontent.com/112995660/204545622-d8b6835b-6edd-453b-bfcb-530714c1d954.png)

이렇게 revert한 내용의 커밋 이력을 남기면서 B로 돌아갈 수 있음을 확인할 수 있다.
