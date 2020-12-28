---
title: "数据结构-并查集"
date: 2020-12-26T13:19:07+08:00
categories: ["Java"]
tags: ["data-struct"]
math:
  enable: true
draft: false
---

# 解决连接问题

## 数据结构

```java
public class UnionFind implements UF {

    // rank[i]表示以i为根的集合所表示的树的层数
    // 在后续的代码中, 并不会维护rank的语意, 也就是rank的值在路径压缩的过程中, 有可能不在是树的层数值
    // 这也是rank不叫height或者depth的原因, 它只是作为比较的一个标准
    private int[] rank;
    private int[] parent; // parent[i]表示第i个元素所指向的父节点

    // 构造函数
    public UnionFind(int size) {

        rank = new int[size];
        parent = new int[size];

        // 初始化, 每一个parent[i]指向自己, 表示每一个元素自己自成一个集合
        for (int i = 0; i < size; i++) {
            parent[i] = i;
            rank[i] = 1;
        }
    }

    @Override
    public int getSize() {
        return parent.length;
    }

}
```

将每一个元素，看作是一个节点
由孩子指向父节点

## 基于 rank 的优化

`rank[i]` 表示树的高度

## 路径压缩

发生在 `find()` 操作时
`parent[p] = parent[parent[p]]`

## 时间复杂度

`o(log*n)` -> iterated logarithm

$ log\*n = \begin{cases} 0 &\text{if } (n <= 1) \\\ 1+log\*(logn) &\text{if } (n > 1) \end{cases} $

近乎是 O(1) 级别的
