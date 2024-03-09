---
title: postgreSQL 형변환
author: dh0rwwit
date: 2024-03-10 00:00:00 +0900
categories: [SQL, PostgreSQL]
tags: [PostgreSQL,type ]
render_with_liquid: false
---

<!-- HTML generated using hilite.me -->
<div style="background: #272822; overflow:auto;width:auto;border:solid gray;background:black;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #75715e">-- integer형을 character varying으로 변경</span>
<span style="color: #66d9ef">ALTER</span> <span style="color: #66d9ef">TABLE</span> <span style="color: #f8f8f2">myTableName</span> <span style="color: #66d9ef">ALTER</span> <span style="color: #66d9ef">COLUMN</span> <span style="color: #f8f8f2">myColumnName</span> <span style="color: #66d9ef">TYPE</span> <span style="color: #f8f8f2">character</span> <span style="color: #f8f8f2">varying;</span>

<span style="color: #75715e">-- integer[]타입 컬럼을 integer으로 변경하기</span>
<span style="color: #66d9ef">alter</span> <span style="color: #66d9ef">table</span> <span style="color: #f8f8f2">myTableName</span>  
<span style="color: #66d9ef">alter</span> <span style="color: #66d9ef">column</span> <span style="color: #f8f8f2">myColumnName</span> 
<span style="color: #66d9ef">set</span> <span style="color: #66d9ef">data</span> <span style="color: #66d9ef">type</span> <span style="color: #f8f8f2">integer</span> <span style="color: #66d9ef">USING</span> <span style="color: #f8f8f2">myColumnName[</span><span style="color: #ae81ff">0</span><span style="color: #f8f8f2">];</span> <span style="color: #75715e">-- 0번째 또는 1번째 배열의 요소를 myColumnName의 컬럼 값으로 사용할 지 변경하기</span>
<span style="color: #75715e">-- https://stackoverflow.com/questions/59452011/postgresql-changing-column-type-from-array-to-integer-throwing-casting-error</span>


<span style="color: #75715e">-- integer타입 컬럼을 integer[]으로 변경하기</span>
<span style="color: #66d9ef">ALTER</span> <span style="color: #66d9ef">TABLE</span> <span style="color: #f8f8f2">myTableName</span>
<span style="color: #66d9ef">ALTER</span> <span style="color: #66d9ef">COLUMN</span> <span style="color: #f8f8f2">myColumnName</span> <span style="color: #66d9ef">TYPE</span> <span style="color: #f8f8f2">INTEGER[]</span> <span style="color: #75715e">-- myColumnName컬럼을 integer[]로 변경한다.</span>
<span style="color: #66d9ef">USING</span> <span style="color: #f8f8f2">array[myColumnName]::INTEGER[];</span> <span style="color: #75715e">-- 근데 얜 왜 array[myColumnName]로 변경해줘야할까...</span>
</pre></div>
