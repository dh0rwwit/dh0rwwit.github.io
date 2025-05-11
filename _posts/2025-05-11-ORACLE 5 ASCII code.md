---
title: ascii code in Oracle
author: dh0rwwit
date: 2025-05-11 00:00:00 +2300
categories: [SQL, ORACLE]
tags: [ORACLE]
render_with_liquid: false
---


<!-- HTML generated using hilite.me -->
<div style="background: #272822; overflow:auto;width:auto;border:solid gray;background:black; border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">SELECT</span> <span style="color: #f8f8f2">CHR(ASCII(</span><span style="color: #e6db74">&#39;Z&#39;</span><span style="color: #f8f8f2">)</span><span style="color: #f92672">+</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">)</span> <span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">DUAL;</span> <span style="color: #75715e">-- 결과 : ]</span>
<span style="color: #66d9ef">SELECT</span> <span style="color: #f8f8f2">CHR(ASCII(</span><span style="color: #e6db74">&#39;B&#39;</span><span style="color: #f8f8f2">)</span><span style="color: #f92672">+</span><span style="color: #ae81ff">1</span><span style="color: #f8f8f2">)</span> <span style="color: #66d9ef">FROM</span> <span style="color: #f8f8f2">DUAL;</span> <span style="color: #75715e">-- 결과 : C</span>
</pre></div>
