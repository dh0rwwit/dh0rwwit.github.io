---
title: ErrorMessage - 문자집합이 일치하지 않습니다...
author: dh0rwwit
date: 2024-07-02 00:00:00 +2300
categories: [SQL, ORACLE]
tags: 
render_with_liquid: false
---

### 1. 문자집합이 일치하지 않습니다.

에러메세지 : "문자집합이 일치하지 않습니다."
<br>
-> SELECT DISTINCT "VARCHAR2타입컬럼","NVARCHAR타입컬럼" FROM TABLENAME ...
<br>
처럼 타입이 다른 컬럼에 집계함수를 적용하여 SELECT 할 때 발생할 수 있는 문제.
<br>
NVARCHAR2 타입을 TO_CHAR() 로 감싸거나 
<br>
VARCHAR2 타입을 UNISTR()로 감싸준다. 


