---
title: PostgreSQL 설치 후 버전 확인 방법
author: dh0rwwit
date: 2024-02-19 00:00:00 +0900
categories: [SQL, PostgreSQL]
tags: [Postgresql]
render_with_liquid: false
---
## 사용자 변수 path 설정
### 제어판 > 시스템 및 보안 > 시스템 > 고급 시스템 설정 > 고급 > 환경 변수 <br>
### '사용자 변수'란의 새로만들기 클릭해서 Path 변수 생성 또는,
### Path라는 이름의 변수를 찾는다.
### Path 변수 더블클릭
### C:\Program Files\PostgreSQL\버전번호\bin 입력 후 확인

## cmd창을 열어서 psql --version 입력

## cmd창에서 postgresql 실행
- psql -U postgres

![Desktop View](/assets/img/PostgreSQL/PostgreSQL_SystemPath check.png){: .normal }


