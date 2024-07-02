---
title: ErrorMessage 문자집합이 일치하지 않습니다...
author: dh0rwwit
date: 2024-07-02 00:00:00 +2300
categories: [SQL, ORACLE]
tags: 
render_with_liquid: false
---

### 1. 문자집합이 일치하지 않습니다.

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #ffffff">에러메세지 : &quot;문자집합이 일치하지 않습니다.&quot;</span>

<span style="color: #ffffff">-&gt; SELECT DISTINCT &quot;VARCHAR2타입컬럼&quot;,&quot;NVARCHAR타입컬럼&quot; FROM TABLENAME ...</span>

<span style="color: #ffffff">처럼 타입이 다른 컬럼에 집계함수를 적용하여 SELECT 할 때 발생할 수 있는 문제.</span>

<span style="color: #ffffff">NVARCHAR2 타입을 TO_CHAR() 로 감싸거나 </span>

<span style="color: #ffffff">VARCHAR2 타입을 UNISTR()로 감싸준다. </span>
</pre></div>



