# 2nd day

1. Github

2. gitignore

> 특정 파일 혹은 폴더에 대해 Git이 버전 관리를 하지 못하도록 지정하는 것

(1) gitignore 작성 시 주의 사항

- 반드시 이름을 **.gitignore**로 작성합니다. 앞의 점(.)은 숨김 파일이라는 뜻입니다.

- .gitignore 파일은 .git 폴더와 동일한 위치에 생성합니다.

- 제외 하고 싶은 파일은 반드시 git add 전에 .gitignore에 작성합니다.

3. clone, pull

(1) git clone

- 원격 저장소의 커밋 내역을 모두 가져와서, 로컬 저장소를 생성하는 명령어

- clone은 "복제"라는 뜻으로, git clone 명령어를 사용하면 원격 저장소를 통째로 복제해서 내 컴퓨터에 옮길 수 있습니다.

- **git clone <원격 저장소 주소>**의 형태로 작성합니다.

```bash
$ git clone https://github.com/edukyle/TIL.git

Cloning into 'TIL'...

remote: Enumerating objects: 3, done.

remote: Counting objects: 100% (3/3), done.

remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0

Receiving objects: 100% (3/3), done.
```

위에 작성한 대로 실행하면, Github의 edukyle이라는 계정의 TIL 원격 저장소를 복제하여 내 컴퓨터에 TIL이라는 이름의 로컬 저장소를 생성하게 됩니다.

- git clone을 통해 생성된 로컬 저장소는 git init과 git remote add가 이미 수행되어 있습니다.

(2) git pull

- 원격 저장소의 변경 사항을 가져와서, 로컬 저장소를 업데이트하는 명령어

- 로컬 저장소와 원격 저장소의 내용이 완전 일치하면 git pull을 해도 변화가 일어나지 않습니다.

- **git pull <저장소 이름> <브랜치 이름>**의 형태로 작성합니다.