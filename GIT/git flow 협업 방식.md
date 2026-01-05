# git flow 협업 방식이란?
협업시 branch들의 효율적 관리를 위한 브랜치 관리 전략

## git repository

### 원격 저장소
``Upstream Repository`` : 
개발자들이 공유하는 원격 저장소로 최신 코드가 저장되어 있다
``Origin Repository`` :
Upstream Repository를 Fork한 원격 개인 저장소

### 로컬 저장소
``Local Repository`` : 
내 컴퓨터에 저장되어 있는 개인 저장소

## git branch
git flow 방식에서 사용하는 branch들은 5가지의 종류가 있다.

``master``, ``develop`` : 항상 유지되는 메인 브랜치들
``feature``, ``release``, ``hotfix`` : 일정 기간 동안만 유지되는 보조 브랜치들

- ``master`` : 제품으로 출시될 수 있는 브랜치
- ``develop`` : 다음 출시 버전을 개발하는 브랜치
- ``feature`` : 기능을 개발하는 브랜치
- ``release`` : 이번 출시를 준비하는 브랜치
- ``hotfix`` : 출시 버전에서 발생한 버그를 수정하는 브랜치

### git branch 작업 방법 

## 1. 로컬 저장소 생성

1. git chore : 중앙 원격 저장소(remote reposiotry)를 복제
2. init : 현재 디렉토리를 빈 git 저장소로 만들기
3. remote add : 현재 작업 중인 git 저장소에 팀의 중앙 원격 저장소(origin)를 추가
4. fetch/pull : master 브랜치 데이터를 로컬에 가져오기

## 2. 로컬 저장소에 develop 브랜치를 만들어 작업
1. 팀원 중 한 명이 develop 브랜치를 만들고 중앙 저장소로 push한다.
2. develop 브랜치 pull request 하기
3. 프로젝트 관리자는 해당 pull request를 merge하기
4. 팀원들은 각자 작업할 브랜치 생성 후 작업

## 3. 개인 작업이 끝나면 develop에 브랜치 병합하기
- pull request<br>
작업한 내용 push하기<br>
1. git add. : 변경된 파일을 스테이징 영역에 추가<br>
2. git commit -m : 커밋하여 로컬에 변경된 사항 저장하기<br>
3. git push origin/main : mian 브랜치에 push하기
4. pull request하기
5. 팀원이 merge 해주면 main에 pull됨