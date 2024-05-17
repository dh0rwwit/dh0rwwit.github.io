---
title: json타입 update insert in pgsql
author: dh0rwwit
date: 2024-05-18 00:00:00 +0600
categories: [SQL, PostgreSQL]
tags: 
render_with_liquid: false
---

<!-- HTML generated using hilite.me --><div style="background: #000000; overflow:auto;width:auto;border:solid brown;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">select</span> <span style="color: #f92672">*</span> <span style="color: #66d9ef">from</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span>

<span style="color: #75715e">-- JSON INSERT</span>
<span style="color: #66d9ef">INSERT</span> <span style="color: #66d9ef">INTO</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span> <span style="color: #f8f8f2">(sc_name,</span> <span style="color: #f8f8f2">tbl_name,</span> <span style="color: #f8f8f2">deleted_json</span> <span style="color: #f8f8f2">)</span>
<span style="color: #66d9ef">VALUES</span>
<span style="color: #f8f8f2">(</span>
    <span style="color: #e6db74">&#39;스키마0&#39;</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;테이블&#39;</span>
    <span style="color: #f8f8f2">,JSON_BUILD_OBJECT</span>
    <span style="color: #f8f8f2">(</span>
        <span style="color: #e6db74">&#39;키0&#39;</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;값0&#39;</span>
        <span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;키1&#39;</span><span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;값1&#39;</span>
        <span style="color: #f8f8f2">,</span><span style="color: #e6db74">&#39;키2&#39;</span><span style="color: #f8f8f2">,</span><span style="color: #ae81ff">0</span>
        <span style="color: #f8f8f2">,</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">,</span><span style="color: #ae81ff">1</span>
    <span style="color: #f8f8f2">)</span>	
<span style="color: #f8f8f2">)</span>

<span style="color: #75715e">-- 배열 UPDATE</span>
<span style="color: #66d9ef">update</span> <span style="color: #f8f8f2">dhkimsch</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span>
<span style="color: #66d9ef">set</span> <span style="color: #f8f8f2">deleted[</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">]</span> <span style="color: #f92672">=</span> <span style="color: #e6db74">&#39;dsfff&#39;</span>
<span style="color: #66d9ef">where</span> <span style="color: #e6db74">&quot;IDX&quot;</span> <span style="color: #f92672">=</span> <span style="color: #ae81ff">2</span> 

<span style="color: #75715e">-- JSON 추가</span>
<span style="color: #66d9ef">INSERT</span> <span style="color: #66d9ef">INTO</span>
    <span style="color: #f8f8f2">DHKIMSCH</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">DEL_LOG</span> <span style="color: #f8f8f2">(DELETED_JSON)</span>
<span style="color: #66d9ef">VALUES</span>
<span style="color: #f8f8f2">(</span>
    <span style="color: #f8f8f2">JSON_BUILD_OBJECT(</span>
        <span style="color: #e6db74">&#39;key&#39;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #e6db74">&#39;value&#39;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #e6db74">&#39;array&#39;</span><span style="color: #f8f8f2">,</span>
        <span style="color: #f8f8f2">JSON_BUILD_ARRAY(</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">,</span> <span style="color: #ae81ff">2</span><span style="color: #f8f8f2">,</span> <span style="color: #ae81ff">3</span><span style="color: #f8f8f2">)</span>
    <span style="color: #f8f8f2">)</span>
<span style="color: #f8f8f2">)</span>
	

<span style="color: #75715e">-- JSON SELECT</span>
<span style="color: #66d9ef">SELECT</span> <span style="color: #f92672">*</span>
<span style="color: #f8f8f2">,deleted_json</span><span style="color: #f92672">-&gt;&gt;</span><span style="color: #e6db74">&#39;키0&#39;</span> <span style="color: #66d9ef">AS</span> <span style="color: #f8f8f2">KEY1</span>
<span style="color: #f8f8f2">,deleted_json</span><span style="color: #f92672">-&gt;&gt;</span><span style="color: #e6db74">&#39;키1&#39;</span> <span style="color: #66d9ef">AS</span> <span style="color: #f8f8f2">KEY2</span>
<span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span> 
<span style="color: #66d9ef">WHERE</span> <span style="color: #f8f8f2">seq</span> <span style="color: #f92672">=</span> <span style="color: #ae81ff">2</span>

<span style="color: #75715e">-- UPDATE</span>
<span style="color: #66d9ef">UPDATE</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span>
<span style="color: #66d9ef">SET</span> <span style="color: #f8f8f2">deleted_json</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">jsonb_set(deleted_json</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb,</span> <span style="color: #e6db74">&#39;{키2}&#39;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&#39;&quot;2&quot;&#39;</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb)</span>
<span style="color: #66d9ef">WHERE</span> <span style="color: #f8f8f2">seq</span> <span style="color: #f92672">=</span> <span style="color: #ae81ff">2</span><span style="color: #f8f8f2">;</span>
<span style="color: #75715e">-- jsonb_set(컬럼이름::jsonb, &#39;{키이름}&#39;, (0::text)::jsonb)</span>

<span style="color: #75715e">-- integer UPDATE</span>
<span style="color: #66d9ef">UPDATE</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span>
<span style="color: #66d9ef">SET</span> <span style="color: #f8f8f2">deleted_json</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">jsonb_set(deleted_json</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb,</span> <span style="color: #e6db74">&#39;{1}&#39;</span><span style="color: #f8f8f2">,</span> <span style="color: #f8f8f2">(</span><span style="color: #ae81ff">0</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">text)</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb)</span>
<span style="color: #66d9ef">WHERE</span> <span style="color: #f8f8f2">seq</span> <span style="color: #f92672">=</span> <span style="color: #ae81ff">2</span><span style="color: #f8f8f2">;</span>
<span style="color: #75715e">-- jsonb_set(컬럼이름::jsonb, &#39;{키이름}&#39;, (0::text)::jsonb)</span>

<span style="color: #75715e">-- 키:값 추가</span>
<span style="color: #66d9ef">UPDATE</span> <span style="color: #f8f8f2">scm</span><span style="color: #ae81ff">.</span><span style="color: #f8f8f2">del_log</span>
<span style="color: #66d9ef">SET</span> <span style="color: #f8f8f2">deleted_json</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">jsonb_set(deleted_json</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb,</span> <span style="color: #e6db74">&#39;{키3}&#39;</span><span style="color: #f8f8f2">,</span> <span style="color: #f8f8f2">(</span><span style="color: #ae81ff">3</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">text)</span><span style="color: #f92672">::</span><span style="color: #f8f8f2">jsonb)</span>
<span style="color: #66d9ef">WHERE</span> <span style="color: #f8f8f2">seq</span> <span style="color: #f92672">=</span> <span style="color: #ae81ff">2</span><span style="color: #f8f8f2">;</span>
</pre></div>