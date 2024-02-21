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
비선형 자료구조는 자료들 간에 계층 구조나 네트워크 형태로 서로 연결되지 않은 자료 구조를 의미합니다. 이러한 자료구조는 선형 자료구조와는 달리 각 원소들 간에 일정한 순서가 없으며, 서로 다른 원소들 간에 부모-자식, 형제, 또는 더 복잡한 연결 관계를 가질 수 있습니다. C#에서는 여러 비선형 자료구조를 구현할 수 있습니다.

1. 트리(Tree)
- 트리는 계층 구조를 가지는 비선형 자료구조로, 루트 노드에서 시작하여 각 노드가 여러 자식 노드를 가질 수 있습니다.
- 트리는 이진 트리, 이진 탐색 트리, AVL 트리 등 다양한 형태가 있습니다.
```cs
public class TreeNode<T>
{
    public T Data { get; set; }
    public List<TreeNode<T>> Children { get; set; }
 
    public TreeNode(T data)
    {
        Data = data;
        Children = new List<TreeNode<T>>();
    }
}
```


</details>

