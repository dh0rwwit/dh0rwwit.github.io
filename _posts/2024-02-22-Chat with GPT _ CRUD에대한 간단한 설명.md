---
title: c# 자료구조
author: dh0rwwit
date: 2024-02-22 00:00:00 +0900
categories: [Chat with AI, with GPT]
tags: [ChatGPT, c# 자료구조]
render_with_liquid: false
---


<details>
<summary> Que 1. c# 자료구조중에 비선형 자료구조 설명해봐 </summary>
<br>
비선형 자료구조는 자료들 간에 계층 구조나 네트워크 형태로 서로 연결되지 않은 자료 구조를 의미합니다. <br>
이러한 자료구조는 선형 자료구조와는 달리 각 원소들 간에 일정한 순서가 없으며,<br>
서로 다른 원소들 간에 부모-자식, 형제, 또는 더 복잡한 연결 관계를 가질 수 있습니다. <br>
C#에서는 여러 비선형 자료구조를 구현할 수 있습니다.<br>
<br>
1. 트리(Tree)
- 트리는 계층 구조를 가지는 비선형 자료구조로, 루트 노드에서 시작하여 각 노드가 여러 자식 노드를 가질 수 있습니다.
- 트리는 이진 트리, 이진 탐색 트리, AVL 트리 등 다양한 형태가 있습니다.
<div class="colorscripter-code" style="color:#73E1F7;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#000000;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #4f4f4f"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#aaa;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div><div style="line-height:130%">8</div><div style="line-height:130%">9</div><div style="line-height:130%">10</div><div style="line-height:130%">11</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#73E1F7;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#FE05F2">public</span>&nbsp;<span style="color:#FE05F2">class</span>&nbsp;TreeNode<span style="color:#FEF705"></span><span style="color:#FE05F2">&lt;</span>T<span style="color:#FEF705"></span><span style="color:#FE05F2">&gt;</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#FE05F2">public</span>&nbsp;T&nbsp;Data&nbsp;{&nbsp;get;&nbsp;set;&nbsp;}</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#FE05F2">public</span>&nbsp;<span style="color:#FEF705">List</span><span style="color:#FE05F2">&lt;</span>TreeNode<span style="color:#FEF705"></span><span style="color:#FE05F2">&lt;</span>T<span style="color:#FEF705"></span><span style="color:#FE05F2">&gt;</span><span style="color:#FEF705"></span><span style="color:#FE05F2">&gt;</span>&nbsp;Children&nbsp;{&nbsp;get;&nbsp;set;&nbsp;}</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#FE05F2">public</span>&nbsp;TreeNode(T&nbsp;data)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Data&nbsp;<span style="color:#FEF705"></span><span style="color:#FE05F2">=</span>&nbsp;data;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Children&nbsp;<span style="color:#FEF705"></span><span style="color:#FE05F2">=</span>&nbsp;<span style="color:#FE05F2">new</span>&nbsp;<span style="color:#FEF705">List</span><span style="color:#FE05F2">&lt;</span>TreeNode<span style="color:#FEF705"></span><span style="color:#FE05F2">&lt;</span>T<span style="color:#FEF705"></span><span style="color:#FE05F2">&gt;</span><span style="color:#FEF705"></span><span style="color:#FE05F2">&gt;</span>();</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;}</div><div style="padding:0 6px; white-space:pre; line-height:130%">}</div></div><div style="text-align:right;margin-top:-13px;margin-right:5px;font-size:9px;font-style:italic"><a  target="_blank" style="color:#4f4f4ftext-decoration:none"><br></a></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#4f4f4f;color:white;border-radius:10px;padding:1px"></span></a></td></tr></table></div>


</details>

