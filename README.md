# aws-tgw-project
AWS Transit Gateway를 이용한 멀티리전 사설망 구현
>[!NOTE]
> **프로젝트 기간:** 2026.04.23 / **난이도:** ★★★☆☆

## 프로젝트 구성도
![TGW 프로젝트 구성도](AWS_Tgw_Project.png)

## 프로젝트 목표
- AWS 기본 자원을 생성할 수 있다.
- AWS Global Accelerator를 이용한 글로벌 서비스를 배포할 수 있다.
- AWS Transit Gateway를 이용한 멀티리전 사설망을 구현할 수 있다.



## 세부 내용:
1. 멀티리전(서울리전, 상파울루 리전)에 웹 서버를 구성하여 글로벌 웹 서비스를 구현
2. 각 리전 웹서버는 ALB를 이용한 고가용성 서비스 구현
3. 각 리전 웹서버는 Auto Scaling Group을 이용한 탄력적 서비스 구현
4. 서울리전은 NAT장치로 인스턴스를 이용하고, 상파울루 리전은 NAT 게이트웨이를 이용
5. 서울리전에 OpenVPN 인스턴스를 설치하여 프라이빗 망 구현
6. 리전 간 전송 게이트웨이 피어링으로 프라이빗 망 구현
7. OpenVPN 및 전체 웹 서버는 각 리전의 키페어(seoul-key, saopaulo-key)를 통해 SSH 접속 허용
8. 서울 리전에 온프레미스 기업망 VPC를 설치하고 AWS 클라우드 망과 Site-to-Site VPN 연결
9. 고객 개인 정보 같은 민감한 데이터는 온프레미스 DB 서버에 보관을 목적으로 함
10. 웹 클라이언트는 AWS Route53의 DNS로 웹서버 접속
11. 접속자 위치에 따라 서로 다른 리전으로 연결되도록 구현
---
Copyright (C) 2026. WONJUNE
