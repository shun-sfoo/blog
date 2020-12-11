---
title: "Stack"
date: 2020-12-11T21:57:46+08:00
categories: ["Java"]
tags: ["data-struct"]
draft: false
---

# Stack

- 栈也是一种线性结构
- 相比数组，栈对应的操作是数组的子集
- 只能从一段添加元素，也只能从一段取出元素
- 这一端称为栈顶

栈是一种 _后进先出_ 的数据结构
Last In First Out(LIFO)

## 栈的应用

- 无处不在的 Undo 操作（撤销）
- 程序调用的系统栈

## 栈的接口

```java
public interface Stack<E> {
    void push(E e);

    E pop();

    E peek();

    int getSize();

    boolean isEmpty();
}
```
