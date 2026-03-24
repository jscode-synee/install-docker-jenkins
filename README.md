# Docker Compose를 활용한 Jenkins 설치

이 리포지토리는 Jenkins를 빠르게 설치하기 위한 Docker Compose 구성을 포함함.
이 접근 방식은 대부분 공식 문서를 기반으로 하지만, Docker Compose(`docker-compose.yml` 파일 사용)를 활용하여 Jenkins를 실행하는 데 필요한 단계 수를 줄였음.

## Docker 설치

### 0단계
로컬 환경에 Docker를 설치함 (가장 쉬운 방법인 Docker Desktop 사용을 권장함).

### 1단계
이 리포지토리를 클론(Clone)하거나 콘텐츠를 다운로드함.

### 2단계
이 리포지토리의 `Dockerfile`이 위치한 디렉토리와 동일한 위치에서 터미널 창을 얾. Jenkins Docker 이미지를 빌드함.

```bash
docker build -t my-jenkins .
```

### 3단계
Jenkins를 시작함.

```bash
docker compose up -d
```

### 4단계
`http://localhost:8080/`에 접속하여 Jenkins를 열고 설치 과정을 완료함.

### 5단계
Jenkins를 중지하고 나중에 다시 사용하려면 다음을 실행함.

```bash
docker compose down
```

나중에 Jenkins를 다시 시작하려면 3단계의 명령어를 동일하게 실행함.

## Jenkins 제거

Jenkins 사용이 끝나고 모든 것을 정리하고자 할 때 진행함.
다음 명령어를 실행하여 Jenkins를 종료하고 사용된 모든 볼륨과 이미지를 제거함.

```bash
docker compose down --volumes --rmi all 
```
