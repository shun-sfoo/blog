---
title: '使用 rust 实现web server'
date: 2021-03-18T15:12:08+08:00
categories: ['Rust']
tags: ['Rust']
draft: false
---

因为 rust 是一个系统编程语言， 我们能够选择处理什么层次的抽象，
并能够选择比其他语言可能或可用的层次更低的层次。

# 目的

1. 学习一些 TCP 与 HTTP 知识
2. 在套接字上监听 TCP 请求
3. 解析少量的 HTTP 请求
4. 创建一个合适的 HTTP 响应
5. 通过线程池改善 server 的吞吐量

