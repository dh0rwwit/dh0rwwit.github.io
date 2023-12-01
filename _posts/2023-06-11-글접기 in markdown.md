---
title: 글 접기 in markdown
author: dh0rwwit
date: 2023-06-11 00:00:00 +2300
categories: [Others, 글쓸때참고사항]
tags: [글 접기]
render_with_liquid: false
---


[HTML로 글 접기 코드](https://dh0rwwit.github.io/posts/%EA%B8%80-%EC%A0%91%EA%B8%B0-in-html/)
   
깃 블로그 작성할 때 markdown을 사용하면 해당 문법을 사용할 수 있지만, css사용이 잘 안된다.      
markdown에서 글 접기 기능을 사용하려면 그냥 아래처럼 단순 html코드 형식을 사용해야 할 거 같다.
<br>
<div class="colorscripter-code" style="color:#f0f0f0;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#272727;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #4f4f4f"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#aaa;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#f0f0f0;font-family:Consolas,font-size:'20px' ,'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><font color="#f0f0f0">&lt;</font><font color="#ff3399">details</font><font color="#f0f0f0">&gt;</font></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;<font color="#f0f0f0">&lt;</font><font color="#ff3399">summary</font><font color="#f0f0f0">&gt;</font>참고&nbsp;블로그&nbsp;확인&nbsp;<font color="#f0f0f0">&lt;</font><font color="#f0f0f0">/</font><font color="#ff3399">summary</font><font color="#f0f0f0">&gt;</font></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;<font color="#f0f0f0">&lt;</font><font color="#ff3399">p</font><font color="#f0f0f0">&gt;</font></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;-&nbsp;https://noexpect.tistory.com/201&nbsp;<font color="#f0f0f0">&lt;</font><font color="#ff3399">br</font><font color="#f0f0f0">&gt;</font></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;-&nbsp;https://moonhouse.co.kr/html/529065?order_type=desc&amp;sort_index=readed_count&amp;l=en&amp;m=1&amp;page=2&amp;listStyle=webzine</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;<font color="#f0f0f0">&lt;</font><font color="#f0f0f0">/</font><font color="#ff3399">p</font><font color="#f0f0f0">&gt;</font></div><div style="padding:0 6px; white-space:pre; line-height:130%"><font color="#f0f0f0">&lt;</font><font color="#f0f0f0">/</font><font color="#ff3399">details</font><font color="#f0f0f0">&gt;</font></div></div><div style="text-align:right;margin-top:-13px;margin-right:5px;font-size:9px;font-style:italic"></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"></td></tr></table></div>

   
이걸 활용하면 
<details>
   <summary> 참고한 블로그 확인 </summary>
   <p>
   - https://noexpect.tistory.com/201 <br>
   - https://moonhouse.co.kr/html/529065?order_type=desc&sort_index=readed_count&l=en&m=1&page=2&listStyle=webzine
   </p>
</details>