---
title: Create Procedure
author: dh0rwwit
date: 2024-01-29 00:00:00 +0900
categories: [SQL, PostgreSQL]
tags: [Postgresql,Procedure]
render_with_liquid: false
---
MSSQL과는 달리, <br>
스키마,\"",\'' 등의 문법이 좀 더 까다로운 거 같다.
<br>
\""로 감싸줘야 하는 것 : 컬럼이름, 테이블이름 <br>
\''로 감싸줘야 하는 것 : 입력하려는 값 <br>
그리고 프로시저에서는 반환값 확인을 위해 select 도중에 into로 값을 넣어줘야하는 것도 상이하다.<br>
MSSQL에서는 <br>
SET int_MaxNumb = (SELECT ColumnName FROM TableName)<br>
과 같은 형태로 가능하다만, <br>
여기선 <br>
<div class="colorscripter-code" style="color:#f0f0f0;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#272727;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #4f4f4f"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#aaa;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#f0f0f0;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><font color="#ff3399">SELECT</font>&nbsp;ColumnName</div><div style="padding:0 6px; white-space:pre; line-height:130%"><font color="#ff3399">INTO</font>&nbsp;ValueName</div><div style="padding:0 6px; white-space:pre; line-height:130%"><font color="#ff3399">FROM</font>&nbsp;<font color="#ffd500">"NS"</font>.<font color="#ffd500">"Table_A"</font>;</div></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#4f4f4f;color:white;border-radius:10px;padding:1px">cs</span></a></td></tr></table></div>
<br>
의 형태로 만들어줘야한다.
