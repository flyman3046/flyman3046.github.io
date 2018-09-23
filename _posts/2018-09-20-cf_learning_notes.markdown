---
layout: default
title:  "Codeforces笔记"
date:   2018-08-19 10:30:00
categories: main
---

新开一个blog，记录一下codeforces的刷题情况，主要用来总结一些解题经验。

CF512，做了4/7，前三题算比正常简单的题目，第四题出了两个WA，没处理好time limit，想法比较tricky，还是挺灵活的一道题。没来得及做第五题，现在把第五题补上，思路就是怎么找充分必要条件，这个时间需要猜测一下，这题的充分必要是两个：1，subsum bitcount是偶数。2，max <= sum - max。满足条件1的个数比较容易计算，现在可以利用容斥原理计算，cnt(condi1 && condi2) = cnt(condi1) - cnt(cnd1 && !condi2)。选择这个容斥的原因就是会简化计算。

CF511，中国人组织的一次比赛，第一和第二题都比较简单，第三题用的seive nloglogn的解法，但是竟然对n是1。5e7的时候都能通过。第四题是个case analysis的题，暴力解只做出来很少的例子，发现不出来规律。把最小dimen放在n上的想法还是挺好的。正确的check error的方法应该是用graph的matching algorithm，比如hungarian algorithm。所以事先估算一下brute force的复杂度还是很有必要的。

Edu round 51，没来的及参加比赛，线下做出来了4道题，第一题的implementations比正常的复杂，第二题和第三题都比较简单，第四题的dp也算常规，之前出现过类似的tile的题目。还是需要先把大概的题目看一遍，找有思路可以马上提交的来做，不要卡在前面的题目！这次比赛的case analysis比较繁琐，还是挺容易出错的，从大家的提交情况来看也是这样。

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com