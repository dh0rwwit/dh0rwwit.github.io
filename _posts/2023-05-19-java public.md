---
title: java의 접근제어자 public
author: dh0rwwit
date: 2023-05-19 00:00:00 +0900
categories: [Language,JAVA]
tags: [접근제어자,Public]
render_with_liquid: false
---

<!-- HTML generated using hilite.me -->
<div style="background: #272822; overflow:auto;width:auto;border:solid brown;font-size:17px;background:#000000;border-width:.2em .2em .2em .8em;padding:.2em .6em;"><table><tr><td><pre style="margin: 0; line-height: 125%"> 1
 2
 3
 4
 5
 6
 7
 8
 9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78</pre></td><td><pre style="margin: 0; line-height: 125%"><span style="color: #75715e">// 생성자 : 클래스 선언안하고 괄호가 있으면 생성자.</span>
<span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #a6e22e">A</span> <span style="color: #f92672">{</span> <span style="color: #75715e">//</span>
    <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">(){};</span> <span style="color: #75715e">// 생성자는 없어도 된다. </span>
    <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">(</span><span style="color: #66d9ef">int</span> <span style="color: #960050; background-color: #1e0010">매개변수</span><span style="color: #f8f8f2">e</span><span style="color: #f92672">){</span>
        <span style="color: #66d9ef">this</span><span style="color: #f92672">.</span><span style="color: #a6e22e">a</span><span style="color: #960050; background-color: #1e0010">유전자</span><span style="color: #f8f8f2">_pb</span><span style="color: #f92672">=</span><span style="color: #960050; background-color: #1e0010">매개변수</span><span style="color: #f8f8f2">e</span><span style="color: #f92672">;</span>
    <span style="color: #f92672">}</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">a</span><span style="color: #960050; background-color: #1e0010">유전자</span><span style="color: #f8f8f2">_pb</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">private</span> <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">a</span><span style="color: #960050; background-color: #1e0010">유전자</span><span style="color: #f8f8f2">_pv</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">protected</span> <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">a</span><span style="color: #960050; background-color: #1e0010">유전자</span><span style="color: #f8f8f2">_pt</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">class</span> <span style="color: #a6e22e">Inner</span><span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span> <span style="color: #f92672">{}</span> 
<span style="color: #f92672">}</span>

<span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #a6e22e">A</span> <span style="color: #66d9ef">extends</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span> <span style="color: #f92672">{</span> 
    <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">(){</span>
        <span style="color: #66d9ef">this</span><span style="color: #f92672">.</span><span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A0_pb</span><span style="color: #f92672">=</span><span style="color: #e6db74">&quot;자식a의 유전형질은 부모a로부터 물려받음.&quot;</span><span style="color: #f92672">;</span>
	<span style="color: #f92672">};</span>
    <span style="color: #66d9ef">public</span> <span style="color: #f8f8f2">String</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A0_pb</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">int</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A1_pb</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">protected</span> <span style="color: #66d9ef">int</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A_pt</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">private</span> <span style="color: #66d9ef">int</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A_pv</span><span style="color: #f92672">;</span>
<span style="color: #f92672">}</span>
	
<span style="color: #75715e">// 일반 class가 static타입의 변수를 갖고 있는 경우. </span>
<span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #a6e22e">B</span> <span style="color: #f92672">{</span>
    <span style="color: #66d9ef">static</span> <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">a</span><span style="color: #f92672">=</span><span style="color: #ae81ff">0</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">b</span><span style="color: #f92672">;</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #a6e22e">B_pb</span> <span style="color: #f92672">{</span>
        <span style="color: #f8f8f2">String</span> <span style="color: #f8f8f2">d</span><span style="color: #f92672">=</span><span style="color: #e6db74">&quot;static으로 정의된 public 함수에 객체 접근&quot;</span><span style="color: #f92672">;</span>
    <span style="color: #f92672">}</span>
    <span style="color: #66d9ef">static</span> <span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #a6e22e">B_st</span> <span style="color: #f92672">{</span>
        <span style="color: #f8f8f2">String</span> <span style="color: #f8f8f2">d</span><span style="color: #f92672">=</span><span style="color: #e6db74">&quot;static으로 정의된 static 함수에 객체 접근&quot;</span><span style="color: #f92672">;</span>
    <span style="color: #f92672">}</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">static</span> <span style="color: #66d9ef">class</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #a6e22e">B_pbst</span> <span style="color: #f92672">{</span>
        <span style="color: #f8f8f2">String</span> <span style="color: #f8f8f2">d</span><span style="color: #f92672">=</span><span style="color: #e6db74">&quot;static으로 정의된 public static 함수에 객체 접근&quot;</span><span style="color: #f92672">;</span>
    <span style="color: #f92672">};</span>	
<span style="color: #f92672">}</span>

<span style="color: #66d9ef">public</span> <span style="color: #66d9ef">class</span> <span style="color: #a6e22e">just_class</span> <span style="color: #f92672">{</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">static</span> <span style="color: #66d9ef">void</span> <span style="color: #a6e22e">main</span><span style="color: #f92672">(</span><span style="color: #f8f8f2">String</span><span style="color: #f92672">[]</span> <span style="color: #f8f8f2">args</span><span style="color: #f92672">)</span> <span style="color: #f92672">{</span>
		
        <span style="color: #75715e">// 부모0유전자 설계도를 통해 그 기능을 하는 세포 cell0을 탄생시킴</span>
        <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span> <span style="color: #f8f8f2">cell0</span> <span style="color: #f92672">=</span> <span style="color: #66d9ef">new</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">();</span>

        <span style="color: #75715e">// 일반 클래스 안에있는 클래스 하나 선언.</span>
        <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">.</span><span style="color: #a6e22e">Inner</span><span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span> <span style="color: #f8f8f2">Cell1</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">cell0</span><span style="color: #f92672">.</span><span style="color: #a6e22e">new</span> <span style="color: #f8f8f2">Inner</span><span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">();</span>
        <span style="color: #75715e">// 상속을 하면 했지 이런 식의 코딩은 잘 안 쓴다...안 하는게 좋다.</span>
		
        <span style="color: #75715e">// 부모의 유전정보는 자식의 유전정보를 품는게 가능하다.</span>
        <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">A</span> <span style="color: #f8f8f2">cell2</span> <span style="color: #f92672">=</span> <span style="color: #66d9ef">new</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">();</span>
        <span style="color: #75715e">/* 자식A cell3 = new 부모A();</span>
<span style="color: #75715e">		자식의 유전정보는 부모의 유전정보를 담을 수 없다.</span>
<span style="color: #75715e">		자식이 부모를 낳을 수 없는 것과 같다.</span>
<span style="color: #75715e">        */</span>
		
        <span style="color: #75715e">// 자식A의 설계도를 담은 세포 Cell3 만듬</span>
        <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A</span> <span style="color: #f8f8f2">cell3</span> <span style="color: #f92672">=</span> <span style="color: #66d9ef">new</span> <span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A</span><span style="color: #f92672">();</span>
        <span style="color: #f8f8f2">cell3</span><span style="color: #f92672">.</span><span style="color: #960050; background-color: #1e0010">자식</span><span style="color: #f8f8f2">A1_pb</span><span style="color: #f92672">=</span><span style="color: #ae81ff">10</span><span style="color: #f92672">;</span> <span style="color: #75715e">// cell3dml 자식A1_pb값 10으로 셋팅</span>
        <span style="color: #75715e">// cell3.자식A_pv=11; -&gt; private로 선언된 멤버변수 및 클래스는 인스턴스로 다룰 수 없다.</span>
		
		
        <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">B</span> <span style="color: #f8f8f2">cell4</span> <span style="color: #f92672">=</span> <span style="color: #66d9ef">new</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">B</span><span style="color: #f92672">();</span>
        <span style="color: #f8f8f2">cell4</span><span style="color: #f92672">.</span><span style="color: #a6e22e">a</span><span style="color: #f92672">=</span><span style="color: #ae81ff">10</span><span style="color: #f92672">;</span> <span style="color: #75715e">// 인스턴스로 static 멤버변수 제어가능</span>
        <span style="color: #f8f8f2">cell4</span><span style="color: #f92672">.</span><span style="color: #a6e22e">b</span><span style="color: #f92672">=</span><span style="color: #ae81ff">3</span><span style="color: #f92672">;</span> <span style="color: #75715e">// 인스턴스로 멤버변수 제어가능</span>
        <span style="color: #75715e">/* cell4.d=&quot;컴파일에러발생&quot;; --&gt; 컴파일 에러가 발생한다.</span>
<span style="color: #75715e">        부모B클래스의 d의 값은 </span>
<span style="color: #75715e">        내부클래스인 부모B_pbst의 d인지 </span>
<span style="color: #75715e">        내부클래스인 부모B_pb의 d인지</span>
<span style="color: #75715e">        명시해줘야한다.</span>
<span style="color: #75715e">        */</span>
        <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">B</span><span style="color: #f92672">.</span><span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">B_pb</span> <span style="color: #f8f8f2">cell5</span> <span style="color: #f92672">=</span> <span style="color: #f8f8f2">cell4</span><span style="color: #f92672">.</span><span style="color: #a6e22e">new</span> <span style="color: #960050; background-color: #1e0010">부모</span><span style="color: #f8f8f2">B_pb</span><span style="color: #f92672">();</span>
        <span style="color: #75715e">/* static으로 선언된 내부클래스는 인스턴스 선언이 안됨 </span>
<span style="color: #75715e">        부모B.부모B_pbst Cell5 = cell4.new 부모B_pbst(); -&gt; 컴파일 에러</span>
<span style="color: #75715e">        부모B.부모B_st Cell5 = cell4.new 부모B_st(); -&gt; 컴파일 에러발생</span>
<span style="color: #75715e">        */</span>
        <span style="color: #f8f8f2">System</span><span style="color: #f92672">.</span><span style="color: #a6e22e">out</span><span style="color: #f92672">.</span><span style="color: #a6e22e">println</span><span style="color: #f92672">(</span><span style="color: #f8f8f2">cell4</span><span style="color: #f92672">.</span><span style="color: #a6e22e">a</span><span style="color: #f92672">);</span> <span style="color: #75715e">// 10 출력</span>
        <span style="color: #f8f8f2">System</span><span style="color: #f92672">.</span><span style="color: #a6e22e">out</span><span style="color: #f92672">.</span><span style="color: #a6e22e">println</span><span style="color: #f92672">(</span><span style="color: #f8f8f2">cell5</span><span style="color: #f92672">.</span><span style="color: #a6e22e">d</span><span style="color: #f92672">);</span> <span style="color: #75715e">// static으로 정의된 public 함수에 객체 접근 출력</span>
	<span style="color: #f92672">}</span>
<span style="color: #f92672">}</span>
</pre></td></tr></table></div>


