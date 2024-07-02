---
title: SELECT 형식의 프로시저 출력
author: dh0rwwit
date: 2024-07-02 00:00:00 +2300
categories: [SQL, ORACLE]
tags: 
render_with_liquid: false
---
### 1. SELECT 형식의 프로시저 출력
<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #75715e">-- 프로시저 실행</span>
<span style="color: #66d9ef">VARIABLE</span> <span style="color: #f8f8f2">RC</span> <span style="color: #f8f8f2">REFCURSOR;</span>
<span style="color: #66d9ef">EXECUTE</span> <span style="color: #f8f8f2">SELECT_PROCEDURENAME(</span><span style="color: #e6db74">&#39;변수값0&#39;</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;변수값1&#39;</span><span style="color: #f8f8f2">,:RC);</span>
<span style="color: #f8f8f2">PRINT</span> <span style="color: #f8f8f2">RC;</span>
</pre></div>


<BR>

- 
- 근데 그냥 프로시저 편집 상태에서 CTRL+F10(실행) 해서 변수에 값 넣고 출력변수 값 보는게 낫다.