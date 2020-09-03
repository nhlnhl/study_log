# Commit an existing project to a Git repository
이미 생성한 프로젝트를 Git 레포지토리에 commit할 때 사용한 Git 명령어들을 정리합니다.

## Git 설치
[Git 다운로드 URL](https://git-scm.com/)

## 레포지토리 생성
Github에서 레포지토리를 생성할 수 있습니다.  
[Github URL](https://github.com/)  
로그인 후, 나의 레포지토리 목록의 'New' 버튼을 통해 생성 가능합니다.

## Git 명령어
파일탐색기에서 프로젝트 위치로 이동해, Git bash를 띄웁니다.
```bash
git init
```
기존 프로젝트를 Git 저장소로 만듭니다.  
저장소의 구성을 위한 .git 이라는 하위 폴더가 자동적으로 추가됩니다.
```bash
git add $파일의_이름
git add *
```
폴더내의 몇몇 파일 혹은 전체 파일을 스테이징 영역으로 올립니다.  
저장소와 작업 트리 간에 존재하는 가상의 스테이징 영역을 인덱스 (Index) 라고 부릅니다.
```bash
git commit -m "$커밋_메세지"
```
스테이징 영역으로 올린 변경사항들을 확정합니다.  
아직 변경사항들이 외부 레포지토리에 반영되지는 않은 상태입니다.
```bash
git remote add origin $레포지토리의_주소 (e.g. git remote add origin https://github.com/nhlnhl/nearby_restaurants.git)
git remote -v
```
Github에서 생성한 레포지토리의 주소를 origin으로 설정합니다.  
두 번째 명령어를 통해 origin이 제대로 설정되었는지를 확인할 수 있습니다.
```bash
git pull origin master --allow-unrelated-histories
```
레포지토리가 비어 있지 않고 파일이 존재한다면, origin (아까 remote로 설정했던 레포지토리) 을 현재 저장소의 master로 pull하고 merge합니다.
```bash
git push origin master
```
이번에는 반대로 master를 origin으로 push합니다.