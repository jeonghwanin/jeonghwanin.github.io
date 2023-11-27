---
layout: single
title:  "분할정복(Devide and conquer)"
categories: algorithm 
tag: [Devide and conquer, recursive, problem, subproblem]
toc: true
author_profile: false
sidebar:
    nav: "docs"
search: true
---
![Divide   conquer](https://github.com/jeonghwanin/jeonghwanin.github.io/assets/99806622/9358e889-bc84-4810-a1d4-6870b3472f85)



## 1.분할정복이란
문제를 같은 크기의 부분문제로 분할하여 문제를 정복하고 다시 병합하여 문제를 해결하는 방법.
문제를 해결하는 과정에서 효율적인 부분이 존재해야한다.

## 2.분할 정복 구성
1. 분할(divide)
문제를 더 작은 문제로 분할하는 과정

2. 기저사례(base case)
더이상 답을 **분할하지 않고** 곧장 풀 수 있는 매우 작은 문제

3. 병합(merge)
부분 문제들을 해결하고 부분문제의 답들을 원래문제의 답으로 **병합하는 과정**

## 3.무식하게 풀기 vs 분할 정복
수열의 합 sum[n] = 1 + 2 + 3 + ... + n 을 함수를 만들자.

### 3.1 무식하게 풀기
sum[n]을 n개의 조각으로 나누고 sum[n] = sum[n-1] + n으로 생각할 수 있음.
시간복잡도는 n번 호출되므로 O(n)이 된다.

### 3.2 분할 정복
sum[n]을 n개의 조각으로 나누고 조각들을 같은 크기로 나누어줌.
sum[n] = (1+2+3+...+n/2) + (n/2+1 + n/2+2 + ... + n/2+n/2) = sum(n/2) + n^2/4*sum(n/2)
무식하게 풀기와는 달리 문제의 크기가 같고 sum(n/2)가 중복되어 계산을 한번만 하면 되는 효율적인 부분이 존재함.
시간복잡도는 log(n)이 된다.

## 결론
1. 접근 자체는 무식하게 풀기와 같다. 문제들을 부분문제들로 분할한다.
2. 분할한 문제를 같은 크기로 분할할 수 있고 효율적인 부분이 존재하는지 확인한다.
3. 분할정복은 선형시간복잡도를 log 시간 복잡도로 바꾸어주는 트리구조, 새그먼트 트리, 이진 탐색 등과 비슷한 원리가 존재함.
 