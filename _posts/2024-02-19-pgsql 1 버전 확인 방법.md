---
title: PostgreSQL 설치 후 버전 확인 방법
author: dh0rwwit
date: 2024-02-19 00:00:00 +0900
categories: [SQL, PostgreSQL]
tags: [Postgresql]
render_with_liquid: false
---

### 1. 사용자 변수 path 설정
- 제어판 > 시스템 및 보안 > 시스템 > 고급 시스템 설정 > 고급 > 환경 변수 <br>
- '사용자 변수'란의 새로만들기 클릭해서 Path 변수 생성 또는, Path라는 이름의 변수를 찾는다. <br>
- Path 변수 더블클릭 <br>
- C:\Program Files\PostgreSQL\버전번호\bin 입력 후 확인 <br>

### 2. cmd창을 열어서 psql --version 입력

### 3. cmd창에서 postgresql 실행
- psql -U postgres <br>
여기서 -U 뒤의 postgres는 사용자 계정 이름이 들어간다.<br>
![Desktop View](/assets/img/PostgreSQL/PostgreSQL_SystemPath check.png){: .normal }

- 쉘을 켰을 때 나오는 postgres=#의 postgres는 데이터베이스 이름이다.<br>
보통 쉘에 처음 접속하면 자동으로 postgres 데이터 베이스에 접속된다.
- cmd창에서는 psql을 따로 입력해야 되지만, shell에서는 그럴 필요 없다.
