---
title: Raise Notice
author: dh0rwwit
date: 2024-05-18 00:00:00 +1200
categories: [SQL, PostgreSQL]
tags: 
render_with_liquid: false
---

### 1. RAISE NOTCE는 ssms의 PRINT와 같다.
<!-- HTML generated using hilite.me -->
<div style="background: #111111; overflow:auto;width:auto;border:solid gray;border-width:.em .1em .1em .4em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #fb660a; font-weight: bold">DO</span> <span style="color: #ffffff">$$</span> <span style="color: #fb660a; font-weight: bold">BEGIN</span>
<span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;FDS&#39;</span><span style="color: #ffffff">;</span>
<span style="color: #fb660a; font-weight: bold">END</span><span style="color: #ffffff">;</span> <span style="color: #ffffff">$$</span>
</pre></div>


<br>

### 2. PGSQL의 '' 과 NULL의관계
<!-- HTML generated using hilite.me -->
<div style="background: #111111; overflow:auto;width:auto;border:solid gray;border-width:.em .1em .1em .4em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #fb660a; font-weight: bold">DO</span> <span style="color: #ffffff">$$</span>
<span style="color: #fb660a; font-weight: bold">DECLARE</span>
    <span style="color: #ffffff">v_nullchk0</span> <span style="color: #ffffff">boolean;</span>
    <span style="color: #ffffff">v_nullchk1</span> <span style="color: #ffffff">boolean;</span>
    <span style="color: #ffffff">v_if</span>	   <span style="color: #ffffff">boolean;</span>
<span style="color: #fb660a; font-weight: bold">BEGIN</span>
    <span style="color: #ffffff">v_nullchk0</span> <span style="color: #ffffff">:=</span> <span style="color: #0086d2">&#39;&#39;</span> <span style="color: #fb660a; font-weight: bold">is</span> <span style="color: #fb660a; font-weight: bold">null</span><span style="color: #ffffff">;</span>
    <span style="color: #ffffff">v_nullchk1</span> <span style="color: #ffffff">:=</span> <span style="color: #0086d2">&#39;&#39;</span> <span style="color: #fb660a; font-weight: bold">is</span> <span style="color: #fb660a; font-weight: bold">not</span> <span style="color: #fb660a; font-weight: bold">null</span><span style="color: #ffffff">;</span>
    <span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;Value of v_nullchk0: %&#39;</span><span style="color: #ffffff">,</span> <span style="color: #ffffff">v_nullchk0;</span>	
    <span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;Value of v_nullchk1: %&#39;</span><span style="color: #ffffff">,</span> <span style="color: #ffffff">v_nullchk1;</span>
    <span style="color: #008800; font-style: italic; background-color: #0f140f">-- 조건문 출력</span>
    <span style="color: #ffffff">v_if</span> <span style="color: #ffffff">:=</span> <span style="color: #fb660a; font-weight: bold">false</span><span style="color: #ffffff">;</span>
    <span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;Value of v_bt1: %&#39;</span><span style="color: #ffffff">,</span> <span style="color: #ffffff">v_if;</span>
    <span style="color: #ffffff">if</span> <span style="color: #ffffff">v_if</span> <span style="color: #fb660a; font-weight: bold">then</span>
        <span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;true&#39;</span><span style="color: #ffffff">;</span>
    <span style="color: #fb660a; font-weight: bold">else</span> 
        <span style="color: #ffffff">RAISE</span> <span style="color: #ffffff">NOTICE</span> <span style="color: #0086d2">&#39;false&#39;</span><span style="color: #ffffff">;</span>
    <span style="color: #fb660a; font-weight: bold">end</span> <span style="color: #ffffff">if;</span>
<span style="color: #fb660a; font-weight: bold">END</span> <span style="color: #ffffff">$$;</span>
</pre></div>

<!-- HTML generated using hilite.me -->
<div style="background: #111111; overflow:auto;width:auto;border:solid gray;border-width:.em .1em .1em .4em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #ffffff">-- 출력결과 --</span>
<span style="color: #ffffff">NOTICE:  Value of v_nullchk0: f</span>
<span style="color: #ffffff">NOTICE:  Value of v_nullchk1: t</span>
<span style="color: #ffffff">NOTICE:  Value of v_bt1: f</span>
<span style="color: #ffffff">NOTICE:  false</span>
<span style="color: #ffffff">DO</span>
</pre></div>




### 3. ''과 null
<br>
- ORACLE에서는 길이 0의 string인 ''도 null로 인식했는데, 그래도 pgsql이나 mssql은 각자 다르게('', NULL) 구분한다.