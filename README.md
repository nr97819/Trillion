(진행중)
# 보안 프로젝트를 위한 대상 웹 구성 
##(의료 마이데이터 서비스 제공 웹 사이트)

본 레포지토리에 포함된 항목들:

## 프로젝트 목차

- [배경 내용](#배경-설명)
- [실행 및 테스트 방법](#실행-및-테스트-방법)
- [결과물](#결과물)

## 배경 설명

> 프로젝트 선정 배경

의료 마이데이터 서비스에 대해 보안 적용을 위해 대상 웹이 필요한데
이를 위해 웹 사이트를 flask 기반으로 구축

> 프로젝트 목적

라이프월릿, 마이헬스웨이 등 의료 마이데이터를 활용한 기업의 클라우드 마이그레이션 
이 중 라이프월릿은 사용자의 의료 기록을 공단으로부터 제공받아 관련 서비스와 상품을 추천해주는 서비스이다.
따라서 우리는 의료 마이데이터를 활용하는 "라이프월릿"이라는 서비스를 데이터 3법을 준수하여 마이그레이션하고 
안전한 클라우드 보안 참조 모델을 제시하고자 한다.(flow chart)

1. 라이프 케어 웹 서비스는 대상 서비스로서 직접 구현하였다.
2. Docker Compose를 사용하여 Web, Was 각각의 컨테이너에 나누어 코드가 분배되었다. Web은 nginx 1.18를, Was는 flask를 사용해 구축하였다.
3. UI/UX를 향상시키기 위해 CSS, Javascript를 사용하였다. (상세한 건 다음 페이지에서 직접 보면서 알아보자)

## 실행 및 테스트 방법

아래 디렉토리로 이동 후, 도커 컴포즈 실행

web 인스턴스 구성
```sh

sudo rm * -rf

sudo rm .git -rf

git init
git config core.sparsecheckout true
echo 06.SourceCode/04.docker-nginx_#/* >> .git/info/sparse-checkout
git pull origin final-pjt-branch
git remote add origin https://github.com/nr97819/Trillion.git
git pull origin healers_test

cd 06.SourceCode/04.docker-nginx_#/
docker-compose up -d --build
```
was 인스턴스 구성
```sh
git init
git config core.sparsecheckout true
echo 06.SourceCode/03.flask_one_two_harmony_#/* >> .git/info/sparse-checkout
git pull origin final-pjt-branch
git remote add origin https://github.com/nr97819/Trillion.git
git pull origin healers_test

cd 06.SourceCode/03.flask_one_two_harmony_#/
docker-compose up -d --build
```

### 결과물

<a href="" />프로젝트 결과물 캡처 파일</a>

### 참여자들

본 프로젝트에 참여한 조원들<br/>
<a href="https://github.com/nr97819/Trillion/graphs/contributors"><br/>
<img src="https://user-images.githubusercontent.com/55518121/144660712-0a05fa2b-de57-4312-85f8-e0a64eecf4a6.png" /></a>

## License

[SK infosec Academy]

# 최종 프로젝트: Nginx + Flask (Docker Compose)
    # Python version : 3.9
    # Docker version : 20.10.7
    # Docker Compose version : 2.0.0-beta.6
