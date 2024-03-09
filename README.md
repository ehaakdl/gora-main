# 프로젝트 설정 및 빌드 가이드

## 서브모듈 연결

메인 프로젝트에 서브모듈을 연결합니다. 아래 명령어를 `gora-main` 폴더 위치에서 실행하세요.

```
git submodule add https://github.com/ehaakdl/gora-backend.git gora-backend
git submodule add https://github.com/ehaakdl/gora-common.git gora-common
git submodule add https://github.com/ehaakdl/gora-common.git gora-server
```

## 빌드 파일 제거

```./gradlew :gora-common:clean :gora-backend:clean :gora-server:clean```

## common 모듈 빌드 
```./gradlew :gora-common:build```

## 모듈 Docker 이미지 제거

```docker rmi backend:latest backend:1.0.0 server:latest server:latest```

## 모듈 빌드 및 Docker 이미지 생성

```./gradlew :gora-common:build :gora-backend:build :gora-backend:jibDockerBuild :gora-server:build :gora-server:jibDockerBuild```
