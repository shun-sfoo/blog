---
title: "数据结构-链表"
date: 2020-12-16T16:37:11+08:00
categories: ["Java"]
tags: ["data-struct"]
draft: false
---

# linkedList

真正的动态数据结构

- 最简单的动态数据结构
- 更深入的理解引用（或者指针）
- 更深入的理解递归
- 辅助组成其他数据结构
- 优点：真正的动态，不需要处理固定容量的问题
- 缺点：丧失了随机访问的能力

## 数据结构

使用私有的内部 node 类

```java
public class LinkedList<E> {
    private Node head;
    private int size;

    private class Node {
        public E e;
        public Node next;

        public Node(E e, Node next) {
            this.e = e;
            this.next = next;
        }

        public Node(E e) {
            this(e, null);
        }

        public Node() {
            this(null, null);
        }

        @Override
        public String toString() {
            return e.toString();
        }
    }
}

```
