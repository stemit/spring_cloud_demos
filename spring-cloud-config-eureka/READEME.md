# 说明：
### [问题由来]
前面案例中client直接调用server的相关信息来获取配置文件，两者耦合。耦合的坏处大家都懂，server由1生多，
后者进行变动，连带这client端要进行大量运维修改操作，复杂效率低。这也违反了spring cloud的服务治理理念。
### [改进方案]
将server做成服务，注册到Eureka供client调用即可。
本章将在"SC Git 配置中心"基础上进行重构和改进。