---
title: Temp(코딩테스트)
author: dh0rwwit
date: 2023-07-05 00:00:00 +2300
categories: [Language/Framework, C#]
tags: [.NET]
render_with_liquid: false
---


<!-- HTML generated using hilite.me -->
<div style="background: #272822; overflow:auto;width:auto;border:solid gray;font-size:18px;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #66d9ef">using</span> <span style="color: #f8f8f2">System;</span>
<span style="color: #66d9ef">using</span> <span style="color: #f8f8f2">System.Collections.Generic;</span>
<span style="color: #66d9ef">using</span> <span style="color: #f8f8f2">System.Collections.Immutable;</span>

<span style="color: #66d9ef">public</span> <span style="color: #66d9ef">class</span> <span style="color: #a6e22e">Solution</span>
<span style="color: #f8f8f2">{</span>
    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">string</span><span style="color: #f8f8f2">[]</span> <span style="color: #a6e22e">solution</span><span style="color: #f8f8f2">(</span><span style="color: #66d9ef">string</span><span style="color: #f8f8f2">[]</span> <span style="color: #f8f8f2">players,</span> <span style="color: #66d9ef">string</span><span style="color: #f8f8f2">[]</span> <span style="color: #f8f8f2">callings)</span>
    <span style="color: #f8f8f2">{</span>
        
        <span style="color: #66d9ef">string</span><span style="color: #f8f8f2">[]</span> <span style="color: #f8f8f2">answer</span> <span style="color: #f8f8f2">=</span> <span style="color: #66d9ef">new</span> <span style="color: #66d9ef">string</span><span style="color: #f8f8f2">[]</span> <span style="color: #f8f8f2">{</span> <span style="color: #f8f8f2">};</span>
        <span style="color: #66d9ef">return</span> <span style="color: #f8f8f2">answer;</span>
    <span style="color: #f8f8f2">}</span>

    <span style="color: #66d9ef">public</span> <span style="color: #66d9ef">static</span> <span style="color: #66d9ef">void</span> <span style="color: #a6e22e">Main</span><span style="color: #f8f8f2">(String[]</span> <span style="color: #f8f8f2">args)</span>
    <span style="color: #f8f8f2">{</span>
        <span style="color: #f8f8f2">String[]</span> <span style="color: #f8f8f2">players</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">{</span> <span style="color: #e6db74">&quot;mumu&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;soe&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;poe&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;kai&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;mine&quot;</span> <span style="color: #f8f8f2">};</span>
        <span style="color: #f8f8f2">String[]</span> <span style="color: #f8f8f2">callings</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">{</span> <span style="color: #e6db74">&quot;kai&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;kai&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;mine&quot;</span><span style="color: #f8f8f2">,</span> <span style="color: #e6db74">&quot;mine&quot;</span> <span style="color: #f8f8f2">};</span>
        <span style="color: #f8f8f2">Dictionary&lt;String,</span> <span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;</span> <span style="color: #f8f8f2">dicPlay0</span> <span style="color: #f8f8f2">=</span> <span style="color: #66d9ef">new</span> <span style="color: #f8f8f2">Dictionary&lt;</span><span style="color: #66d9ef">string</span><span style="color: #f8f8f2">,</span> <span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;();</span>
        <span style="color: #75715e">// ForEach문 사용하여 Player 이름, 인덱스 정보 저장</span>
        <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">idx0</span> <span style="color: #f8f8f2">=</span> <span style="color: #ae81ff">0</span><span style="color: #f8f8f2">;</span>

        <span style="color: #66d9ef">foreach</span> <span style="color: #f8f8f2">(</span><span style="color: #66d9ef">string</span> <span style="color: #f8f8f2">player</span> <span style="color: #66d9ef">in</span> <span style="color: #f8f8f2">players)</span>
        <span style="color: #f8f8f2">{</span>
            <span style="color: #f8f8f2">dicPlay0.Add(player,</span> <span style="color: #f8f8f2">idx0);</span>
            <span style="color: #f8f8f2">idx0++;</span>
        <span style="color: #f8f8f2">}</span>
        <span style="color: #f8f8f2">Console.WriteLine(</span><span style="color: #e6db74">&quot;// --- ForEach로 입력된 Dictionary 값들 ---//&quot;</span><span style="color: #f8f8f2">);</span>
        <span style="color: #66d9ef">foreach</span> <span style="color: #f8f8f2">(KeyValuePair&lt;String,</span><span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;</span> <span style="color: #f8f8f2">player</span> <span style="color: #66d9ef">in</span> <span style="color: #f8f8f2">dicPlay0)</span> <span style="color: #f8f8f2">{</span> 
            <span style="color: #f8f8f2">Console.Write(player.Key+</span><span style="color: #e6db74">&quot;    &quot;</span><span style="color: #f8f8f2">);</span>
            <span style="color: #f8f8f2">Console.WriteLine(player.Value);</span>
        <span style="color: #f8f8f2">}</span>

        <span style="color: #75715e">// forEach문 사용하지 않고, Player의 이름값,인덱스 정보를 Dictionary형태의 변수에 입력하기 --- 1</span>
        <span style="color: #f8f8f2">Dictionary&lt;String,</span> <span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;</span> <span style="color: #f8f8f2">dicPlay</span> <span style="color: #f8f8f2">=</span> <span style="color: #66d9ef">new</span> <span style="color: #f8f8f2">Dictionary&lt;</span><span style="color: #66d9ef">string</span><span style="color: #f8f8f2">,</span> <span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;();</span>
        <span style="color: #f8f8f2">dicPlay</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">players.Select((plName,</span> <span style="color: #f8f8f2">plidx)</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #66d9ef">new</span> <span style="color: #f8f8f2">{</span> <span style="color: #f8f8f2">name</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">plName,</span> <span style="color: #f8f8f2">index</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">plidx</span> <span style="color: #f8f8f2">}).ToDictionary(d</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #f8f8f2">d.name,</span> <span style="color: #f8f8f2">d</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #f8f8f2">d.index);</span>

        <span style="color: #75715e">// forEach문 사용하지 않고, Player의 이름값,인덱스 정보를 Dictionary형태의 변수에 입력하기 --- 2</span>
        
        <span style="color: #66d9ef">var</span> <span style="color: #f8f8f2">dictPlayer</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">players.Select((plName,</span> <span style="color: #f8f8f2">plidx)</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #66d9ef">new</span> <span style="color: #f8f8f2">{</span> <span style="color: #f8f8f2">name</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">plName,</span> <span style="color: #f8f8f2">index</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">plidx</span> <span style="color: #f8f8f2">}).ToDictionary(d</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #f8f8f2">d.name,</span> <span style="color: #f8f8f2">d</span> <span style="color: #f8f8f2">=&gt;</span> <span style="color: #f8f8f2">d.index);</span>
        <span style="color: #75715e">// 1. Players의 </span>

        <span style="color: #66d9ef">foreach</span> <span style="color: #f8f8f2">(KeyValuePair&lt;String,</span> <span style="color: #66d9ef">int</span><span style="color: #f8f8f2">&gt;</span> <span style="color: #f8f8f2">it</span> <span style="color: #66d9ef">in</span> <span style="color: #f8f8f2">dicPlay)</span> <span style="color: #f8f8f2">{</span>
            <span style="color: #f8f8f2">Console.WriteLine(it.Value</span> <span style="color: #f8f8f2">+</span><span style="color: #e6db74">&quot;, &quot;</span><span style="color: #f8f8f2">+</span> <span style="color: #f8f8f2">it.Key);</span>
        <span style="color: #f8f8f2">}</span>



        <span style="color: #66d9ef">foreach</span> <span style="color: #f8f8f2">(String</span> <span style="color: #f8f8f2">cal</span> <span style="color: #66d9ef">in</span> <span style="color: #f8f8f2">callings)</span> <span style="color: #f8f8f2">{</span>
            <span style="color: #75715e">// players 안에 원소와 일치하는 cal의 값의 인덱스</span>
            <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">intCallingsIndex</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">Array.IndexOf(players,</span> <span style="color: #f8f8f2">cal);</span>
            <span style="color: #f8f8f2">Console.WriteLine(intCallingsIndex);</span>

            <span style="color: #75715e">// call한 선수의 앞에 있는 선수의 인덱스</span>
            <span style="color: #66d9ef">int</span> <span style="color: #f8f8f2">intFormerPlayer</span> <span style="color: #f8f8f2">=</span> <span style="color: #f8f8f2">intCallingsIndex</span> <span style="color: #f8f8f2">-</span> <span style="color: #ae81ff">1</span><span style="color: #f8f8f2">;</span>
            

        <span style="color: #f8f8f2">}</span>






        <span style="color: #75715e">// var로 정의된 변수는 {}안에서 정의된 값을 {}밖에서도 사용할 수 있다.</span>
        <span style="color: #75715e">// let으로 정의된 변수는 {}안에서 정의된 값은 밖에서 적용되지 않는다.</span>
        <span style="color: #75715e">// let varName = &quot;정의&quot;;</span>
        <span style="color: #75715e">// let varName = &quot;이렇게 재선언하면 에러난다.&quot;</span>
        <span style="color: #75715e">// varName = &quot;업데이트는 가능하다&quot;;</span>

<span style="color: #75715e">/*        Solution sol = new Solution();</span>

<span style="color: #75715e">        String[] arrSolve = sol.solution(players, callings);</span>
<span style="color: #75715e">        foreach (String ply in arrSolve)</span>
<span style="color: #75715e">        {</span>

<span style="color: #75715e">        }*/</span>

    <span style="color: #f8f8f2">}</span>
<span style="color: #f8f8f2">}</span>




<span style="color: #75715e">// Func 제너릭 대리자는 0개 이상의 인수를 가지며 마지막에 반환타입을 작성한다.</span>
<span style="color: #75715e">/*</span>
<span style="color: #75715e">Func&lt;int, double, int&gt; FuncMethod0</span>
<span style="color: #75715e">- 매개변수 int, double</span>
<span style="color: #75715e">- 반환타입은 int</span>

<span style="color: #75715e">Func&lt;int, int&gt; FuncMethod1</span>
<span style="color: #75715e">- 매개변수 int</span>
<span style="color: #75715e">- 반환타입 int</span>

<span style="color: #75715e">Func&lt;int&gt; FuncMethod2</span>
<span style="color: #75715e">- 매개변수 없음</span>
<span style="color: #75715e">- 반환 타입은 int형</span>
<span style="color: #75715e"> */</span>
<span style="color: #75715e">/* Func 활용</span>

<span style="color: #75715e">static int className(int ParaName) {</span>
<span style="color: #75715e">    return 2;</span>
<span style="color: #75715e">}</span>

<span style="color: #75715e">static int className1(int ParaName, int ParaName1) {</span>
<span style="color: #75715e">    return ParaName+ParaName1;</span>
<span style="color: #75715e">} </span>

<span style="color: #75715e">static void Main(String[] args) {</span>
<span style="color: #75715e">    Func&lt;string,int&gt; 인스턴스 = className;    </span>
<span style="color: #75715e">    // 그런데 매개변수가 2개인 경우에는 소괄호를 사용해야 한다.</span>
<span style="color: #75715e">    Func&lt;int, int&gt; 인스턴스 = (a,b) =&gt; (a+b).ToString();</span>
<span style="color: #75715e">    </span>
<span style="color: #75715e">}</span>

<span style="color: #75715e"> </span>
<span style="color: #75715e"> </span>
<span style="color: #75715e"> </span>
<span style="color: #75715e"> */</span>
</pre></div>
