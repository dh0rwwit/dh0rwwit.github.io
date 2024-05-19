---
title: 기본 Select FUNCTION
author: dh0rwwit
date: 2024-05-19 00:00:00 +2100
categories: [SQL, PostgreSQL]
tags: 
render_with_liquid: false
---

<!-- HTML generated using hilite.me -->
<div style="background: #000000; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">CREATE</span> <span style="color: #66d9ef">or</span> <span style="color: #66d9ef">replace</span> <span style="color: #66d9ef">function</span> <span style="color: #f8f8f2">masuser_fx(_parameter</span> <span style="color: #f8f8f2">varchar)</span> 
<span style="color: #66d9ef">RETURN</span> <span style="color: #66d9ef">TABLE</span><span style="color: #f8f8f2">(col1</span> <span style="color: #f8f8f2">varchar,</span> <span style="color: #f8f8f2">col2</span> <span style="color: #f8f8f2">varchar,</span> <span style="color: #f8f8f2">col3</span> <span style="color: #f8f8f2">varchar)</span> 
<span style="color: #66d9ef">LANGUAGE</span> <span style="color: #f8f8f2">plpgsql</span> 
<span style="color: #66d9ef">as</span> <span style="color: #e6db74">$$</span> 
<span style="color: #66d9ef">BEGIN</span>
    <span style="color: #66d9ef">RETURN</span> <span style="color: #66d9ef">QUERY</span> 
    <span style="color: #66d9ef">SELECT</span> <span style="color: #f8f8f2">phone_no,</span><span style="color: #e6db74">&quot;name&quot;</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&quot;ReceiptCode&quot;</span> <span style="color: #75715e">-- RETURN 타입/개수와 맞춰야 한다.</span>
    <span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #e6db74">&quot;MASUser&quot;</span><span style="color: #f8f8f2">;</span>
<span style="color: #66d9ef">END</span><span style="color: #f8f8f2">;</span>
<span style="color: #e6db74">$$</span><span style="color: #f8f8f2">;</span>

<span style="color: #75715e">-- 함수 삭제 : DROP FUNCTION IF EXISTS masuser_fx(varchar);</span>

<span style="color: #66d9ef">SELECT</span> <span style="color: #f92672">*</span> <span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">masuser_fx(</span><span style="color: #e6db74">&#39;Alice&#39;</span><span style="color: #f8f8f2">);</span>
</pre></div>


