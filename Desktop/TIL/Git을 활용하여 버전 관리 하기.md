# Git을 활용하여 버전 관리 하기

- ### GUI(Graphic user Interface)

- ### CLI(Command Line Interface)

  ```python
  ls               # 파일 확인
  pwd              # 현재 있는 디렉토리 (print working directory)
  mkdir            # 디렉토리 만들기 (make directory)
  cd test          # changing directory
  cd ..            # 상위 디렉토리 
  cd .             # 현재 디렉토리
  touch b.txt      # (텍스트) 파일 생성
  echo             # print 역할
  ```

  - git 기본 흐름

    - working directory (modified)

      `add`

    - stage area (staged)

      `commit`

    - .git directory

  - 기본 명령어

    - ```python
      git init
      ```

      - .git 폴더가 생김
      - repository가 생성됨

    - ```python
      git add <file>
      ```

      - untracted  상태의 파일을 staged로 변경
      - modified 상태의 파일을 staged로 변경

    - ```python
      git commit -m '<커밋메시지>'
      ```

      - staged 상태의 파일들을 커밋을 통해 버전으로 기록
      - 스냅샷으로 관리
      - 변경된 사항만 새로 저장함
      - 기존의 델타 기반 버전 관리시스템과 가장 큰 차이를 가짐

    - ```python
      git status
      ```

      - git 저장소에 있는 파일의 상태를 확인하기 위하여 활용

    - ```python
      git log
      ```

      - 현재 저장소에 기록된 커밋을 조회
        - `git lod -1`
        - `git log -1 —oneline` # 최근 2개만 한줄로 표현하겠다

      