---
layout: post
#标题配置
title:  "Bismark: paired-end low mapping efficiency"
#时间配置
date:   2019-03-03 10:16:27 +0800
#大类配置
categories: Bioinfo
#小类配置
tag: software
---

* content
{:toc}

模拟数据问题的问题，下载的数据比对正常（SRR5343780）
1，--min_score L,0,-1.9 可以解决；
2，排除质量值分布问题（trim-glaore；fastqc正常）；
3，排除 reads 顺序不一致问题；
4，排除 reference 用错
5， 排除 directionial | non-dicret 文库问题
6, http://seqanswers.com/forums/showthread.php?t=40496 
