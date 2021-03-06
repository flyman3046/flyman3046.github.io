---
layout: default
title:  "Codeforces笔记"
date:   2018-08-19 10:30:00
categories: main
---

新开一个blog，记录一下codeforces的刷题情况，主要用来总结一些解题经验。

CF542，做了3/6。做的还可以，毕竟是比较正常的div1的比赛，虽然提交的时间有点慢，但是差不多把能做的都做出来了。后面的可以在有时间的时候再回来看看，感觉后面的题目想法远远超过现在的水平。

CF541，做了4/7。做的一般，第六题出乎意料的简单，第四题很有希望做出来的，只是考虑问题的方向有点问题，应该先把相等的元素union起来，然后再考虑其他不等的条件。是个很好的topological sort和union find的题目。第五题看着解答试了很多次还是有case通不过，估计还是自己对问题的理解有偏差。

Edu60，做了3/7。做的很一般，第四题之前遇到过类似的，第三题是个很不错的题目，刚开始觉着是BS，后来发觉不太像，最后其实确实是BS的题目。并且很早之前遇到过类似的BS的题目，看来还是总结的不到位。第五题一直没看懂需要的方法，需要总结一下，然后看看最后一题能不能做出来。最后一题还是可以从题目中提取一些有用信息的，思路大概是，最后的目标是找一个permutation，但是这个长度可以是4000。怎么unique的label [0 - 3999]，这里用到了如何用a-z来encode信息，只要用长度为3的string就可以encode，比如aaa表示0，aab表示1等等。拿到这些数组之后就可以做query，然后重新拼凑出来这个permutation。

CF538，做了5/6。这次做的还不错。其中在第二题和第三题上花了比较多的时间，反而在第四题和第五题上花的时间比较少。第三题在forloop的时候有溢出，亏着pretest比较全面，要不还是挺容易出错的。第五题是个比较标准的binary search加random的题目。试着upsolve最后一题。最后通过用C++做了最后一题，看来还是java在这种类型的题目上速度不给力，并且C++的语法小细节特别多，很容易犯错。

CF537，做了2/5。这次又是很差，pretest不好，其实应该是个很好的机会。在第三题上花了几乎所有的时间，用了之前一个code，但是没经过测试。所以在可以的话，还是自己写binary search比较好，不要依赖于Arrays.binarySearch()。前两题可以hack很多，但是时间都花在了第三题上。upsolve了第三题，第四题和第五题看似很难的样子。

Edu59，做了5/7。这次还不错，主要因为第五题在leetcode上有类似的题目。第四题花了很长时间来想优化空间，其实是不必的。主要瓶颈在时间复杂度上，用了BS来快速搜索一下。有个trick是，怎么快速判断一个给定正方形里面是不是全部都是1或者0。这个问题可以事先计算subsum，然后根据subsum来快速判断。看看能不能upsolve第七题吧。

CF532，做了3/6。前三题都比较简单。第二题稍微多花了点时间，但是也算很快写出来了。然后一直在hack别人的case，成功了一个。第五题多花点时间还是可以写出来的。后来有思路了之后就也没时间了，已经upsolved了。

Avito 2018，做了2/8。第二题就卡了很长时间，最后也没看出来规律，这种Ad Hoc的题目稍微复杂点，就很棘手。第四题没找到MST这种规律，第五题最后WA了，大致思路已经有了，需要upsolve很多。最后第五题错在一个非常小的地方，没主意边界变化。第五题是个很好的数学题。相对来说自己更喜欢这种数学题，第二题也补充了，要换位思考一下，把跟自己不是一个颜色的人的数量转换成跟自己相同颜色的数量。第四题没看出来跟MST的联系，还是需要多建立对图这类题目的直觉。MST有一个性质是可以minimize任意两点之间path中的最大值，然后这个题目就转换成了一个disjoint set的题目。

Edu 56，做了4/7。这次CD的WA太多次了，所以做的一般。EFG题目都是关于array的，值得多看看如果利用segtree来优化。最后一题的思路很好，就是把多维问题简化到一维问题，通过扩展搜索空间来保证答案的正确性。这个题目java很容易就会TLE，遇到这种题目最好还是用c++。

CF526，做了4/6。这次还可以，遇到的题目都是比较容易发现规律的，第四题是个dfs不错的题目。看看尽量upsolve第五题，第六题看似很难的样子。

CF525，做了3/6。做的又是很不好，第一二题都是简单题，第三题耗了绝大部分时间，是个constructive的题目。也来不及看第四题和第五题了。继续补充和努力吧。第三题有个很简单直观的解法，就是让a[i] = k * n + i，这样从后往前就可以很快的找到办法，然后用一个mod就可以了。第五题也是个tree的题，需要用到点dp的想法，归结到简易版的问题就是如何计算一个tree里面的最大的connected component，然后问有几个non-overlapped的component有最大的sum。这里面的想法还是挺好的，值得多学习学习，是个比较general的technique。

Edu 55，做了3/7。做的还是不好，这次题目的case比较多，第三题纠结了很长时间。主要是因为自己没理解题意造成的，尤其是加黑的地方，下次吸取教训。upsolve第四题和第五题吧。第四题有个degree的条件没注意，题目大部分思路都是对的。第五题是个很好的题目，虽然是个array的题，貌似没有太多办法，但是最终可以归结于一个如何计算最大subarray的sum，这个可以用dp，可以用各种办法来解决。这个题目最重要的是如何把问题简化，这个简化的过程没想到。碰到这种区间计算的问题应该是一类问题。

Mail.Ru Cup Rnd 3，做了4/8。这次题目不错，前面有写简单的题加上需要一些思考的数学题，还有简单的interactive的题，还有稍微需要找规律的graph的题。第五题有初步的想法，但是不会优化时间复杂度，需要upsolve一下。第五题的想法其实是对的，只是没算对时间复杂度，估计也没时间去code。这里遇到了如何快速比较substring，这里用到的trick是rolling hash，这样只是计算区间的hash值就够了，就不再需要每个字母进行对比。最后总结了一个string hash的模板，下次遇到类似的string的题目，尽量往hash方面想想。

CF524，做了3/6。这次做的一般，比赛时间比较晚。第五题是个好题，找到了解法，但是没有manacher’s algorithm的模板，最后没时间coding。第四题是个找规律的题，自己一直不太擅长这种题目。需要把这两个题补充一下，顺便弄一个manacher’s algorithm的模板。虽然rating降低了，但是确实感觉自己进步了一些，尤其对需要一些思考的题目。有些类型的题目，比如找规律的，interactive这些类型的题目还是需要多锻炼。第五题upsolve了一下，整理了一个manacher的模板，还有一个trick就是如何hash一个string来比较两个string经过sort之后是不是相等，其中的思路还是挺不错的。

CF523，做了2/6。这次做的很差，第三题的时间卡的很厉害，应该是对java不利的，看看别人有什么更好的想法吧，第四题看了一眼没什么想法就一直卡在第三题上。这次需要总结的东西比较多，不过也是个很好的教训，毕竟这是个长期的过程。也能看出来自己比之前更好了。第三题的思路一开始是对的，时间和空间复杂度的考虑也是对的，但是优化的时候思考的方向错了。还有一个应该记住的点就是如果1e6的List<List<Integer>>，很有可能会超时，因为List毕竟还是比array慢。然后1e6之内，divisor最多的数是720720，以后这个可以做为stress test的例子。

CF520，做了4/6。相对来说这次简单一些，题目需要思考的比较多，如果思路对的话，可以很快的写完。第四题的规律挺有趣的，需要联系到seive，graph，euler path。第五题是个很不错的题目，后来upsolve了，难点在于快速查找一个区间所有点的lca。这里用到了euler tour里面start time的性质。[l, r]的lca就是这个区间里面start time最小和最大两个点的lca。如果能找到这个结论的话基本题目就解决了，其他的可以用segment tree和lca的模板来解决。

Edu 54，做了4/7。题目挺好的，在第二题上花了比较多的时间，是个挺好的数学题，需要发现点规律。第四题是个图的题，提交的时候不是完全确定对不对，不过还是AC了。第五题之前没遇到过，考察的点挺多的，是个不错的题目，应该对这类题目多总结一下，看看还有没有其他的类似的。尽量把第六题补充上来。

Mail.Ru Cup，做了2/7。这次的题目比较难，第二题刚开始思路不对，想太复杂了。第三题就开始不会了，想了挺长时间也没找到规律，是个数学题，基本上属于如果不会差不多就是不会想出来的那种。第三题是个完全的数学题，需要找到两个点怎么才能离的最近。两个点可以通过加减gcd(t1, t2)来让距离最近，比赛的时候离这个结论比较接近了，但是当时没找到这个结论。

Level 5 final，做了3/6。第一题比较直观，第二题是binary search，第三题也是binary search，但是需要仔细发现规律。第四题是个interactive的题，对这种题没有想法，从来没AC过。看着答案把第四题提交了。第五题是个非常好的题，需要仔细考虑规律。对于n大于四的时候有统一的规律，但是对于n是3的时候，需要考虑选取哪三个点。其中extreme的点不超过8个，最优解一定有至少两个extreme点组成，所以可以用优化过的暴力解就行。第六题也是个好题，需要很大的转化，根本想不到会转换到图，然后用dsu来解决，这个需要仔细琢磨琢磨。

CF519，做了4/7。这次题目相对来说简单一些，第一题和第二题都比较直观，虽然第二题有点绕。第三题花了一些时间在dp解法上，后来发现直接用greedy就可以，也不需要像dp那样保留中间状态。第四题挺不错的，也不用特别繁琐的解法。就是需要快速的查找一个序列中一个数的前一个数是什么，需要用一个额外的数组事先计算一下。第五题没时间做了，需要补充。第五题是个很好的题，类似个图的题目，需要计算所有边的和，但是N^2的复杂度太多，需要找到这么一个规律，就是怎么快速计算某个点的所有权重，我们可以对点进行sort，然后某个点的所有左边可以用presum快速计算，同样也试用于某个点的右边。sort的标准需要很好的理解。

Edu53，做了4/7。前两题都比较简单。第三题是binary search，跟之前的类似，需要很小心各种初始条件，边界条件。还写了一个brute foce解来验证一下答案。第四题是个有个简单的解法，就是在暴力解的基础上稍微优化一下。第五题是个digital dp题，如果不熟练会很繁琐，需要考虑的状态转移很麻烦，但是也是有规律可寻的。这种类型的需要多练习练习。

CF518，只做出来2/6。第一题题意太难理解，不过好在没直接跳过做其他的。第三题用了很长时间找规律。第四题是个dp，时间允许的话应该可以做出来的，所以有机会还是得多训练训练dp，最好一次提交成功。第五题貌似比第四题简单，但是不怎么会tree的题，这次比赛需要好好总结总结。把第四题的补充一下，有个需要特别小心的是，如果要分配很大的多维内存，把小的dimension放在前面会省很多时间。比如这样dp[2][1000]就会比dp[1000][2]快很多。

Mail.ru Round1，只做出来了3/8，并且第三题卡的时间太长，一直没找到好的规律可寻，在没希望的情况下提交了，虽然过了，但是还是很冒险，其实自己并不会。还是可以看看提交情况来判断一下题目难度，大量正确的提交基本就是代表有一些规律还没发现。第四题非常好，花了很长时间也没理清思路，虽然离答案比较接近了，关键步骤还是欠缺，比如presum怎么由改变ai形成。如何改变presum的内容来让匹配的个数最小，这个题目值得仔细考虑考虑。

Level5，做了3/7。前三题算比较正规的题目，第三题是个挺好的递归问题。在第四题上花了很多时间，有很多细节需要考虑清楚。在质数分解上一直卡着，一直在找一个可以快速质数分解的算法，到最后也没找出来。这个题目从开始的出发角度就不对，需要后来补充上去。现在把第四题补充上去，这个需要一个比较好的切入点，归根结底是要求所有质数对应的指数。但是两个很大质数的乘积没办法快速质数分解，这个时候可以利用它跟其他数的gcd，看看会不会是1或者它本身，如果都不是的话，这个gcd就一定是其中的一个质数。

CF514，做了3/5。前三题也算是正常题，第二题implementation比较麻烦，第三题可以很快的bruteforce找到规律，但是中间出现问题，导致bruteforce程序有问题，纠结了很长时间在找规律上，第四题还剩半个小时，仔细分析的话还是可以做出来的，应该要找一个圆心的坐标，一直想着应该怎么固定x轴位置，其实可以固定y轴坐标，然后查找有没有合适的x轴坐标。第四题还会有precision error的问题，也需要注意。

CF512，做了4/7，前三题算比正常简单的题目，第四题出了两个WA，没处理好time limit，想法比较tricky，还是挺灵活的一道题。没来得及做第五题，现在把第五题补上，思路就是怎么找充分必要条件，这个时间需要猜测一下，这题的充分必要是两个：1，subsum bitcount是偶数。2，max <= sum - max。满足条件1的个数比较容易计算，现在可以利用容斥原理计算，cnt(condi1 && condi2) = cnt(condi1) - cnt(cnd1 && !condi2)。选择这个容斥的原因就是会简化计算。

CF511，中国人组织的一次比赛，第一和第二题都比较简单，第三题用的seive nloglogn的解法，但是竟然对n是1.5e7的时候都能通过。主要原因是在计算的时候还确定是不是prime，只对prime的进行计算。如果每个都计算的话，复杂度会是nlogn。第四题是个case analysis的题，暴力解只做出来很少的例子，发现不出来规律。把最小dimen放在n上的想法还是挺好的。正确的check error的方法应该是用graph的matching algorithm，比如hungarian algorithm。所以事先估算一下brute force的复杂度还是很有必要的。

Edu round 51，没来的及参加比赛，线下做出来了4道题，第一题的implementations比正常的复杂，第二题和第三题都比较简单，第四题的dp也算常规，之前出现过类似的tile的题目。还是需要先把大概的题目看一遍，找有思路可以马上提交的来做，不要卡在前面的题目！这次比赛的case analysis比较繁琐，还是挺容易出错的，从大家的提交情况来看也是这样。

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com