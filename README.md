## 比赛官网

https://data.xm.gov.cn/contest-series/digit-china-2021/#/3/

## 数据下载

百度网盘下载：链接: https://pan.baidu.com/s/1YOObpX4EbhL4AXVx5VjL-w 密码: rcvm

## 赛题分析

**算法分析题**: 题目为第一个大题。

- **什么是共享单车的潮汐现象？**

根据人们生活的规律，如果共享单车调度不到位的话，会导致工作日很多人早上上班的时候，发现某些地方会没有单车可以骑，晚上下班的时候，共享单车会囤积在某些地方。

- **算法分析题的任务是什么？**

任务1：参赛者需基于主办方提供的数据进行数据分析和计算模型构建等工作，识别出工作日早高峰07:00-09:00潮汐现象最突出的40个区域，列出各区域所包含的共享单车停车点位编号名称，并提供计算方法说明及计算模型，为下一步优化措施提供辅助支撑。

任务2：参赛者根据任务一Top40区域计算结果进一步设计高峰期共享单车潮汐点优化方案，通过主动引导停车用户到邻近停车点位停车，进行削峰填谷，缓解潮汐点停车位（如地铁口）的拥堵问题。允许参赛者自带训练数据，但需在参赛作品中说明所自带数据的来源及使用方式，并保证其合法合规。

（城市公共自行车从业者将发生在早晚高峰时段共享单车“借不到、还不进”的问题称之为“潮汐”现象。本题涉及的“潮汐现象”聚焦“还不进”的问题，识别出早高峰共享单车最淤积的40个区域）

- **代码提交格式是什么？如何计算评分？**

请先下载参考手册https://data.xm.gov.cn/image/2021file/userGuide.pdf

- **如何登陆并提交作品？**

**使用命令行登陆sftp，然后进行作品提交**

复制下面命令行，然后输入密码即可，下面是我们队伍的专属sftp传输账号，登陆后就和Linux系统命令行差不多了

**登陆：**

```
命令行：sftp -oPort=57891 comp_3592@sftp.ai.xm.gov.cn
输入密码：VYOiUlRKyps5Mr48
```

**文件处理（put和get）：**

```
下载文件：
登陆sftp账号，然后输入命令
get -r remote_filename local_path
就会将远程文件下载到本地

上传文件：
登陆sftp账号，然后输入命令
put -r local_file remote_path

删除文件：
rm file_name
```

**退出登陆：**

```
exit
```

**当然也可以使用sftp软件提交作品，详细请看参考手册！**

## 算法结果提交

- **算法结果提交地址**

算法运行的结果要**固定输出到sftp的result目录下**，并且**文件命名为result.txt**，文件格式为utf-8。

- **算法预测结果样式**

![image.png](http://ww1.sinaimg.cn/large/005KJzqrgy1goberjvupsj30y40f440t.jpg)

![image.png](http://ww1.sinaimg.cn/large/005KJzqrgy1gobesf6w8cj30x40aedhz.jpg)

- **算法评分计算**

**成绩计算使用召回率和精确率计算，通过两者计算F1-Score。取F1的平均后乘以30的到最后得分**

**任务一输出的算法模型得分占总分的30%，任务二输出的优化方案展总得分70%**

## 相关思路

- **参考视频**

https://www.bilibili.com/video/BV1Af4y1C7fv?zw

- **参考代码**

代码：https://cdn.coggle.club/dcic2021/DCIC-baseline.html

比赛入围代码：https://github.com/610yilingliu/bike_analysis

提交方法：https://data.xm.gov.cn/contest-series-api/file/period_id_1/userGuide.pdf

- **比赛问题记录**

https://shimo.im/docs/dpgWPXRcygjKg9GH/read