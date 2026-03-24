# Docker Compose를 활용한 Jenkins 설치

이 리포지토리는 Jenkins를 빠르게 설치하기 위한 Docker Compose 구성을 포함함. 이 설정은 프로덕션 시스템용이 아님.
참고: 이 접근 방식은 대부분 공식 문서를 기반으로 하지만, Docker Compose(`docker-compose.yml` 파일 사용)를 활용하여 Jenkins를 실행하는 데 필요한 단계 수를 줄였음.

## Docker 설치

### 0단계
로컬 환경에 Docker를 설치함 (가장 쉬운 방법인 Docker Desktop 사용을 권장함).

### 1단계
이 리포지토리를 클론(Clone)하거나 콘텐츠를 다운로드함.

### 2단계
이 리포지토리의 `Dockerfile`이 위치한 디렉토리와 동일한 위치에서 터미널 창을 얾. Jenkins Docker 이미지를 빌드함:

```bash
docker build -t my-jenkins .
