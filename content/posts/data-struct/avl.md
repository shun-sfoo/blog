---
title: "数据结构-avl树"
date: 2020-12-28T15:29:41+08:00
draft: false
categories: ["Java"]
tags: ["data-struct"]
---

# 平衡二叉树和 AVL 树

对于任意一个节点，左子树和右子树的高度差不能超过 1

平衡二叉树的高度和节点数量之间的关系也是 O(logn)的

## 平衡因子

## 判断一棵树是否为 BST

利用 BST 中序遍历过程中访问元素是顺序的特点来判断一棵树是否为 BST

## AVL 的左旋转和右旋转

### 右旋转

旋转前:
`T1 < z < T2 < x < T3 < y < T4 `
旋转操作：
`x.right = y`
`y.left = T3`

### 左旋转

`T4 < y < T3 < x < T1 < z < T2`
旋转操作：
`x.left = y`
`y.right = T3`
