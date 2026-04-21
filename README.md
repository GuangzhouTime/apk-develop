• 介绍

本项目基于Android原生框架开发，集桌面时钟、微博热搜、记账与备忘录于一体，重点探索 AppWidget、小组件刷新机制、本地数据管理及跨进程通信技术实现

开发语言：Java

UI框架：Android原生 + AppWidget

网络与解析：Jsoup

本地存储：Room（软件内建SQLite,可离线查看）

架构特点：模块化设计（Widget/数据层/UI层分离）便于后续更新与代码维护


• 桌面小组件AppWidget

桌面端时钟与热搜信息展示,精确到秒

特别针对系统刷新限制设计更新策略以实现数据的准实时展示

桌面组件与应用数据联动更新

• 热搜数据抓取
基于 Jsoup 解析网页数据，获取微博热搜榜

数据本地缓存，可提供离线查看


• 本地数据管理
使用 Room 构建本地数据库，实现账单与备忘数据持久化

可按日期维度查询,以CalendarNote框架为主

实现按月/年统计的收支分析

• 跨进程数据访问
由于 AppWidget 与主应用运行在不同进程,通过设计缓存容器作为中间层

实现了小组件对主程序数据库的间接访问


• 软件部分界面展示
<p align="center">
  <img src="https://github.com/user-attachments/assets/3cd287c2-cdbd-4347-9553-c8535c8832f4" width="150"/>
  <img src="https://github.com/user-attachments/assets/55f3ded8-49c4-43c5-b569-9414463557a5" width="150"/>
  <img src="https://github.com/user-attachments/assets/231081c3-9b19-4fcf-ac4a-7f35f19a2dae" width="150"/>
  <img src="https://github.com/user-attachments/assets/d31d06b7-ca86-4a5f-aca9-cefd06e09355" width="150"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/70873d1c-8a0a-4bfb-b338-68427ef5033f" width="200"/>
  <img src="https://github.com/user-attachments/assets/968cf149-3c7b-457c-8271-ce8453b30de8" width="200"/>
  <img src="https://github.com/user-attachments/assets/17da0d64-b994-4ff0-8dae-07314ae90759" width="200"/>
</p>


