# SSAFY 내 TIL 정리 
## 2025/07/08~2025/07/18
---

- ## cli 관련
  - `mv`, `cp`, `touch`, `mkdir`

- ## markdown 관련
  - `---` : 줄긋기
  - `###` : 제목, 본문 등 폰트 사이즈
  - `![image](image.url)` :  이미지 업로드 (깃헙 리드미에서는 파일로 넣어두기)
  - `[link](link.url)`: url 업로드
  
- ## github 관련
  - git >> `add` >> `commit` >> `push` 순서
  - 반드시 `push` 전에 git status, git log 등 관련 이슈 확인하기
  - commit 메세지를 되돌리는 방법
    - `git commit --amend`
  - `git remote remove` >> 원격 저장소 연결 해제
  - `git remote -v` >> 연결된 원격 저장소 관련 정보
  - `git config list` >> config 관련 정보
  - `git remote add origin [master] [원격저장소url]`

  - git staging >> `WD(Working Directory)` >> `Staging Area` >> `Repository`
  - ### Revert 
    - commit을 실행취소 시키는 명령어
    - `git revert hashID` >> 띄어쓰기로 여러 개, 순서대로 가능
  - ### Reset
    - `git reset [옵션] <commit id>`
    - 특정 commit으로 되돌아 갔을 떄, 되돌아간 commit 이후의 commit은 모두 삭제
    - options
      - soft, mixed, hard
      - 삭제되는 commit들의 기록을 어떤 영역에 남겨둘지
      - default는 mixed
        - soft
          - 삭제된 commit의 기록을 staging area에 남김
        - mixed
          - 삭제된 commit의 기록을 working directory에 남김(기본 옵션 값)
        - 💀 hard 
          - 삭제된 commit의 기록을 남기지 않음
          - `git reflog` 를 활용해 삭제된 commit으로 돌아갈 수 있음
            - HEAD가 이전에 가리켰던 모든 commit을 보여줌