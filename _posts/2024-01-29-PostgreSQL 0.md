---
title: Create Procedure
author: dh0rwwit
date: 2024-01-29 00:00:00 +0900
categories: [SQL, PostgreSQL]
tags: [Postgresql,Procedure]
render_with_liquid: false
---
MSSQL과는 달리, <br>
스키마,\" \",\' \' 등의 문법이 좀 더 까다로운 거 같다.
<br>
\"\"로 감싸줘야 하는 것 : 컬럼이름, 테이블이름 <br>
\'\'로 감싸줘야 하는 것 : 입력하려는 값 <br>
그리고 프로시저에서는 반환값 확인을 위해 select 도중에 into로 값을 넣어줘야하는 것도 상이하다.<br>
MSSQL에서는 <br>
SET int_MaxNumb = (SELECT ColumnName FROM TableName)<br>
과 같은 형태로 가능하다만, <br>
여기선 <br>

<!-- HTML generated using hilite.me --><div style="background: #272822; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">SELECT</span> <span style="color: #f8f8f2">ColumnName</span>
<span style="color: #66d9ef">INTO</span> <span style="color: #f8f8f2">ValueName</span>
<span style="color: #66d9ef">FROM</span> <span style="color: #e6db74">&quot;NS&quot;</span><span style="color: #f8f8f2">.</span><span style="color: #e6db74">&quot;Table_A&quot;</span><span style="color: #f8f8f2">;</span>
</pre></div>

의 형태로 만들어줘야한다.
