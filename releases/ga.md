---
title: TiDB 1.0 release notes
category: Releases
---

# TiDB 1.0 release notes

10 月 15 日，TiDB 发布 GA 版（TiDB 1.0）。该版本对 MySQL 兼容性、SQL 优化器、系统稳定性、性能做了大量的工作。

## TiDB:

+ SQL 查询优化器
  - 调整代价模型
  - Analyze 下推
  - 函数签名下推

+ 优化内部数据格式，减小中间结果大小
+ 提升 MySQL 兼容性
+ 支持 `NO_SQL_CACHE` 语法，控制存储引擎对缓存的使用
+ 重构 Hash Aggregator 算子，降低内存使用
+ 支持 Stream Aggragator 算子

## PD:

+ 支持基于读流量的热点调度
+ 支持设置 Store 权重，以及基于权重的调度

## TiKV:

+ Coprocessor 支持更多下推函数
+ 支持取样操作下推
+ 支持手动触发数据 Compact，用于快速回收空间
+ 提升性能和稳定性
+ 增加 Debug API，方便调试

## TiSpark Beta Release:

+ 支持可配置框架
+ 支持 ThriftSever/JDBC 和 Spark SQL 脚本入口

## 源码地址

[源码地址](https://github.com/pingcap/tidb)

## 鸣谢

### 特别感谢参与项目的企业和团队

- Archon
- Mobike
- SpeedCloud
- UCloud
- 腾讯云
- 韩国三星研究院

### 感谢以下组织/个人提供出色的开源软件/服务：

- Asta Xie
- CNCF
- CoreOS
- Databricks
- Docker
- Github
- Grafana
- gRPC
- Jepsen
- Kubernetes
- Namazu
- Prometheus
- RedHat
- RocksDB Team
- Rust Team

### 感谢社区个人贡献者 TiDB Contributor

- 8cbx 
- Akihiro Suda
- Akihiro Suda 
- aliyx
- alston111111 
- andelf
- Andy Librian 
- Arthur Yang 
- astaxie 
- Bai, Yang 
- bailaohe
- Bin Liu
- Bin Liu 
- Blame cosmos 
- Breezewish
- Carlos Ferreira
- Ce Gao 
- Changjian Zhang
- Cheng Lian
- Cholerae Hu
- Chu Chao 
- coldwater 
- Cole R Lawrence 
- cuiqiu
- cuiqiu 
- cuiyuan 
- Cwen
- Dagang 
- David Chen
- David Chen 
- David Ding
- dawxy 
- dcadevil
- Deshi Xiao 
- Di Tang 
- disksing
- disksing 
- dongxu
- dongxu 
- dreamquster
- Drogon
- Du Chuan 
- Dylan Wen 
- eBoyy
- Eric Romano 
- Ewan Chou
- Ewan Chou 
- Fiisio
- Fred Wang
- fud 
- fudali 
- gaoyangxiaozhu
- Gogs 
- goroutine
- Gregory Ian
- Guanqun Lu 
- Guilherme Hübner Franco
- Haibin Xie
- Haibin Xie 
- Han Fei
- hanfei1991 
- Hiroaki Nakamura 
- hiwjd 
- Hongyuan Wang
- Hu Ming
- Hu Ziming 
- Huachao Huang
- Huachao Huang 
- HuaiyuXu
- HuaiyuXu 
- Huxley Hu
- iamxy
- iamxy 
- Ian
- insion 
- iroi44
- Ivan.Yang 
- Jack Yu
- jacky liu 
- Jan Mercl 
- Jason W 
- Jay
- Jay 
- Jay Lee 
- Jian Zhang
- Jianfei Wang
- Jiaxing Liang
- Jie Zhou 
- jinhelin 
- Jonathan Boulle 
- Karl Ostendorf 
- knarfeh 
- Kuiba 
- leixuechun
- li 
- Li Shihai 
- Liao Qiang
- Light 
- lijian 
- Lilian Lee
- Liqueur Librazy
- Liqueur Librazy 
- Liu Cong
- Liu Shaohui 
- liubo0127
- liyanan
- lkk2003rty 
- Louis
- louishust
- louishust 
- luckcolors 
- Lynn
- maiyang 
- maxwell 
- mengshangqi
- Michael Belenchenko 
- mo2zie
- morefreeze 
- MQ 
- mxlxm
- Neil Shen
- netroby 
- ngaut
- ngaut 
- Nicole Nie 
- nolouch 
- overvenus 
- PaladinTyrion 
- paulg
- Priya Seth
- qgxiaozhan
- qhsong 
- Qiannan 
- qiuyesuifeng
- Queeny
- queenypingcap
- queenypingcap 
- qupeng
- qupeng 
- Rain Li
- ranxiaolong
- Ray
- Rick Yu 
- shady
- shady 
- ShawnLi 
- Shen Li
- Sheng Tang 
- shenli 
- Shirly 
- Shuai Li
- ShuNing
- ShuNing 
- ShuYu Wang
- ShuYu Wang 
- siddontang
- siddontang 
- silenceper 
- Simon J Mudd
- Simon Xia 
- skimmilk6877
- sllt 
- soup
- Soup 
- Sphinx
- Steffen 
- sumBug
- sunhao2017
- Tao Meng 
- Tao Zhou
- tennix
- tennix 
- tiancaiamao
- tiancaiamao 
- TianGuangyu 
- Tristan Su 
- ueizhou 
- UncP
- Unknwon 
- v01dstar
- v01dstar 
- Van 
- WangXiangUSTC 
- wangyisong1996
- weekface
- weekface 
- wegel 
- Wei Fu
- Wenbin Xiao 
- Wenting Li
- Wenxuan Shi
- winkyao
- woodpenker 
- wuxuelian 
- Xiang Li 
- xiaojian cai
- Xuanjia Yang 
- Xuanwo 
- XuHuaiyu
- Yang Zhexuan
- yang zhexuan
- Yann Autissier 
- Yanzhe Chen 
- Yiding Cui
- Yiding Cui 
- Yim 
- youyouhu
- Yu Jun
- Yuwen Shen 
- Zejun Li
- Zejun Li 
- Zhang Yuning 
- zhangjinpeng1987
- zhangjinpeng1987 
- ZHAO Yijun
- Zhe-xuan Yang 
- ZhengQian
- ZhengQianFang
- zhengwanbo
- ZhiFeng Hu 
- Zhiyuan Zheng
- Zhou Tao
- Zhoubirdblue 
- zhouningnan
- zimulala
- zimuxia 
- Ziyi Yan
- zs634134578 
- zyguan 
- zz-jason
- 仇柯人 
- 王妍军
- 王维真 
- 赵星宇