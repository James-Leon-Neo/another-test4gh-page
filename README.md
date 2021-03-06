Project Facing-NKUs-ZiXiuKe
===========================

### 项目描述

针对于2013年新出台的“南开大学研究生学术规范学习测试系统”的前端脚本项目<br />
项目名取自轻小说《机巧少女不会受伤》的各卷副标题命名格式（**Facing ......**），详见维基百科<a href="http://ja.wikipedia.org/wiki/%E6%A9%9F%E5%B7%A7%E5%B0%91%E5%A5%B3%E3%81%AF%E5%82%B7%E3%81%A4%E3%81%8B%E3%81%AA%E3%81%84#.E5.B0.8F.E8.AA.AC" target="_blank">词条相关部分</a>

#### 实现功能

* [“多重学习”功能](#%E5%A4%9A%E9%87%8D%E5%AD%A6%E4%B9%A0%E5%8A%9F%E8%83%BD)
* [可选择的题面](#%E5%8F%AF%E9%80%89%E6%8B%A9%E7%9A%84%E9%A2%98%E9%9D%A2)
* ~~[1000分钟考试时间](#1000%E5%88%86%E9%92%9F%E8%80%83%E8%AF%95%E6%97%B6%E9%97%B4)~~（现已取消）
* [显示答案功能](#%E6%98%BE%E7%A4%BA%E7%AD%94%E6%A1%88%E5%8A%9F%E8%83%BD)（目前尚有Bug，详见下注）
* [自动完成功能](#%E8%87%AA%E5%8A%A8%E5%AE%8C%E6%88%90%E5%8A%9F%E8%83%BD)

#### 系统需求

请使用Mozilla Firefox或Google Chrome等支持W3C标准的浏览器，暂时不支持M$ IE浏览器

#### 使用方法

采用客户端脚本注入的方式来使用，具体说明详见下文中的[说明](#%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)

***

### 功能说明

#### “多重学习”功能

正常情况下，点击学习页面中的“保存学习时间”按钮只能保存当前节的学习时间，而所谓“多重学习”，<br />
就是在使用本脚本后，“保存学习时间”按钮功能增强到了可以一直保存学习时间到应学习的最后一节

**补充说明：**由于学习时间**似乎**是在服务器处完成保存设置，**暂时**无法从前台伪造<br />
**　　　　　**因此尽管可以同时保存多节的学习时间，但还是需要在至少一节的学习中经历**真实的一段时间**

**请注意：**系统会自动记录各节的最后学习时间，而使用“多重学习”功能将导致各节的最后学习时间是**连续的**，<br />
**　　　　**因此还请**注意时间间隔、按顺序访问一下各节学习页面**，以达到最后学习时间**有序化**的目的

附<a href="http://zixiuke.nankai.edu.cn/StudyProgress/StudyList/1" target="_blank">学习进度查询页面链接</a>（**请在登录南开大学研究生学术规范学习测试系统后再访问**）

[回到页首](#project-facing-nkus-zixiuke)

***

#### 可选择的题面

解除原先试卷中对于题目内容禁止选择的限制，使得题目内容可以选择并轻易复制<br />
结合左侧的教材，则可以复制题目中的关键字，然后查找相关上下文来回答题目

**注：**对于答案获取不全的填空题，仍需要利用此方法来作答

[回到页首](#project-facing-nkus-zixiuke)

***

#### ~~1000分钟考试时间~~

~~将考试的时间从原来的3/10/30分钟统一增加到1000分钟，以便用户在左侧的教材中去寻找答案。<br />
窃以为1000分钟应该够用了，笑~~<del>~</del>

**说明：**在某次使用中发现系统会自动记录每次的测试时长，由于当考试超时时会自动提交试卷，<br />
**　　　**如果继续保留该功能可能会造成测试时间过长，因此**取消**该功能

附<a href="http://zixiuke.nankai.edu.cn/StudyProgress/ExamList/1" target="_blank">测试时间记录页面链接</a>（**请在登录南开大学研究生学术规范学习测试系统后再访问**）

[回到页首](#project-facing-nkus-zixiuke)

***

#### 显示答案功能

将当前测试试卷的答案显示在对应题目下方，方便试卷的完成

**注意：**此方式有一个**Bug**，也就是部分填空题的答案可能获取不全，即空数多于显示答案条数；<br />
**　　　**测试中，出现此情况时缺少的答案都是**位于第一个空的位置**，填空题的答案是有序的；<br />
**　　　**因而如果出现此情况，仍需要通过手动查询方式来补足缺失的**第一个空格**<br />
**　　　**所谓“手动查询方式”，详见前文“[可选择的题面](#%E5%8F%AF%E9%80%89%E6%8B%A9%E7%9A%84%E9%A2%98%E9%9D%A2)”一节

[回到页首](#project-facing-nkus-zixiuke)

***

#### 自动完成功能

只需点击试卷中新出现的“自动完成”按钮，即可自动完成试卷答案的填写<br />

**注意：**如果出现填空题答案获取不全（即未获取到第一个空答案）的情况时，<br />
**　　　**本功能将只会完成已获取答案的对应填写，仍需要手动查询来填写空位的答案

**补注：**由于系统会记录每次测试的成绩，因此可以故意改错几个题目来避免全满分，笑~

**补充说明：**由于**似乎**测试时间是由服务器在后台判定，目前还**暂无**测试时间的伪造方法，<br />
**　　　　　**因此请在测试时自行延迟一段时间之后再提交试卷；<br />
**　　　　　**或者等待考试超时后自动提交（现已取消1000分钟考试时间功能）

附<a href="http://zixiuke.nankai.edu.cn/StudyProgress/ExamList/1" target="_blank">测试时间记录页面链接</a>（**请在登录南开大学研究生学术规范学习测试系统后再访问**）

[回到页首](#project-facing-nkus-zixiuke)

***

### 使用说明

进入课程的学习页面后，打开在Firefox或者Chrome的“开发者工具”栏（一般是按下F12键后出现的）<br />
在工具栏中的控制台处（英文为**Console**）输入以下代码后回车执行即可

```
script=document.createElement("script");
script.src="https://raw.github.com/James-Niu/Facing-NKUs-ZiXiuKe/master/latest.js";
head=document.getElementsByTagName("head")[0];
head.appendChild(script);
```

[回到页首](#project-facing-nkus-zixiuke)

***
