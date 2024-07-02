---
title: WHERE 조건절에서 변수에 NULL값이 들어올 때
author: dh0rwwit
date: 2024-07-02 00:00:00 +2300
categories: [SQL, ORACLE]
tags: 
render_with_liquid: false
---

### 1. WHERE 조건절에서 변수에 NULL값이 들어올 때

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">SELECT</span> <span style="color: #f8f8f2">COL_NAME</span>
<span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">DUAL</span>
<span style="color: #66d9ef">WHERE</span>
    <span style="color: #f8f8f2">NVL(COL_NAME,</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">)</span> <span style="color: #66d9ef">LIKE</span> <span style="color: #f8f8f2">DECODE(I_VALUE,</span><span style="color: #66d9ef">NULL</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;%&#39;</span><span style="color: #f8f8f2">,I_VALUE)</span>
</pre></div>


