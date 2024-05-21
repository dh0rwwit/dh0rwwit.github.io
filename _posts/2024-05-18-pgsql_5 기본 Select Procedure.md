---
title: 기본 Select Procedure
author: dh0rwwit
date: 2024-05-18 00:00:00 +0500
categories: [SQL, PostgreSQL]
tags: 
render_with_liquid: false
---

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">CREATE</span> <span style="color: #66d9ef">OR</span> <span style="color: #66d9ef">REPLACE</span> <span style="color: #66d9ef">PROCEDURE</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">s_masuser</span>
<span style="color: #f8f8f2">(</span>
    <span style="color: #66d9ef">INOUT</span> <span style="color: #f8f8f2">io_result</span> <span style="color: #f8f8f2">refcursor</span>
<span style="color: #f8f8f2">)</span>
<span style="color: #66d9ef">LANGUAGE</span> <span style="color: #e6db74">&#39;plpgsql&#39;</span>
<span style="color: #66d9ef">AS</span> <span style="color: #e6db74">$BODY$</span>
<span style="color: #66d9ef">BEGIN</span>
    <span style="color: #66d9ef">OPEN</span> <span style="color: #f8f8f2">io_result</span> <span style="color: #66d9ef">FOR</span>
    <span style="color: #66d9ef">SELECT</span> <span style="color: #f92672">*</span> <span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #e6db74">&quot;MASUser&quot;</span><span style="color: #f8f8f2">;</span>
<span style="color: #66d9ef">END</span><span style="color: #f8f8f2">;</span>
<span style="color: #e6db74">$BODY$</span><span style="color: #f8f8f2">;</span>
</pre></div>



<br>

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #f8f8f2">CALL</span> <span style="color: #f8f8f2">s_masuser(</span><span style="color: #e6db74">&#39;ans&#39;</span><span style="color: #f8f8f2">);</span>
<span style="color: #66d9ef">FETCH</span> <span style="color: #66d9ef">ALL</span> <span style="color: #66d9ef">IN</span> <span style="color: #f8f8f2">ans;</span>
<span style="color: #75715e">-- FETCH ALL IN 구문은 PostgreSQL에서 refcursor를 사용하여 커서의 모든 행을 가져올 때 사용</span>
<span style="color: #75715e">-- INOUT 타입 쓰면 커서 선언 필요없음.</span>
</pre></div>



<BR>
1. MSSQL의 프로시저와는 많이 다르다. <BR>
과장 좀 보태서 그냥 다 잊어버려도 되는 정도...
2. 프로시저 삭제는

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .6em;padding:.2em .4em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">DROP</span> <span style="color: #66d9ef">PROCEDURE</span> <span style="color: #66d9ef">IF</span> <span style="color: #66d9ef">EXISTS</span> <span style="color: #f8f8f2">get_user_by_id;</span>
</pre></div>
