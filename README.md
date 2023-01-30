# 利用Python对招聘信息数据分析

> 作者：何翔 				 
>
> 学院：计算机学院
>
> 学号：04191315		
>
> 班级：软件1903
>
> 项目全部文件的下载地址：https://download.csdn.net/download/HXBest/21700279
>
> 转载或引用请标注本文链接：https://blog.csdn.net/HXBest/article/details/119973217
>
>如有问题，欢迎在 [issues](https://github.com/hexiang10/recruitment-data-analysis/issues) 中反馈，其他问题联系方式：
[![Bilibili](https://img.shields.io/badge/-Bilibili-blue?style=flat&logo=Bilibili&logoColor=pink)](https://space.bilibili.com/495642569)
[![QQ](https://img.shields.io/badge/-172837855-white?style=flat&logo=tencentqq&logoColor=black)](javascript;)

# 一、开发环境准备

**导入开发所需相应的类库**
![image](https://img-blog.csdnimg.cn/img_convert/e021ab9dee8666b6ecbddc3ebb7555a2.png)

# 二、项目设计与开发

## 2.1. 数据归纳整理

![image](https://img-blog.csdnimg.cn/img_convert/00b7eaebeb579959e99fad9dcb877786.png)

### 2.1.1 文件合并

![image](https://img-blog.csdnimg.cn/img_convert/d2c2494e862e07146a91d8910a04d14d.png)

**合并后的CSV文件如下，包含了所有给定的数据：**

**合并文件后将合并后的文件上传，合并好的数据表名字为：data.csv**

![image](https://img-blog.csdnimg.cn/img_convert/457b44bc0555ffe1d41dd532e0beb4f1.png)

## 2.2.  载入数据，获取数据

![image](https://img-blog.csdnimg.cn/img_convert/6255dc2db0cbe3ee850a6ab5e9dce58e.png)

### 2.2.1 预览数据

![image](https://img-blog.csdnimg.cn/img_convert/ddfcc50338eb3c77fd45ecfb06d11daa.png)

## 2.3. 数据处理与加工

![image](https://img-blog.csdnimg.cn/img_convert/b33242cfd0fb8c96e24c31f27d0fb375.png)
一般而言salary列的值比较混乱，有数字有字符串，我们需要加工薪水数据，把薪水的上限下限隔离出来，以便于统计。观察可得，大部分的薪水是含有上下限的，单位为小写的千或万，中间用“-”作为连接的字符串，个别职位会出现“面议”的描述。这里用apply方法传入自定义的函数进行数据加工。


### 2.3.1 处理薪资字段

**处理后以千(K)作为基本单位**

![image](https://img-blog.csdnimg.cn/img_convert/5a794c3a3dddab9240d01bf53a8a650d.png)

### 2.3.2 获取薪资的上下界限值

![image](https://img-blog.csdnimg.cn/img_convert/d7ce2f2f957a569caf435591c157c682.png)

### 2.3.3 增加平均薪资

![image](https://img-blog.csdnimg.cn/img_convert/6d64101abbdf47e2cd8b128f55936675.png)

### 2.3.4 将公司的规模数据化

![image](https://img-blog.csdnimg.cn/img_convert/0919943c51444aef4fe5732c68706e5a.png)

![image](https://img-blog.csdnimg.cn/img_convert/dd8315b553b6ff8991fb80f1bc6758a1.png)

### 2.3.5 增加公司的平均规模

![image](https://img-blog.csdnimg.cn/img_convert/17219d253a6939dd35b14a24c78ff73f.png)

![image](https://img-blog.csdnimg.cn/img_convert/1cca35f6e1b7079dc1fbc456542484f9.png)

## 2.4. 数据分析与可视化

### 2.4.1岗位和人才需求分析

#### 2.4.1.1 分析岗位需求量排名前10的职业

![image](https://img-blog.csdnimg.cn/img_convert/0472af9d2bc96fcba58f02f4d62800ef.png)

![image](https://img-blog.csdnimg.cn/img_convert/b263ac751b1ec8206cc3fce7b1ba6885.png)

#### 2.4.1.2 岗位需求城市分布

![image](https://img-blog.csdnimg.cn/img_convert/183949c6d9168823adb94cd2969e706a.png)

#### 2.4.1.3 分析各地区招聘的人才需求

![image](https://img-blog.csdnimg.cn/img_convert/bb00e811b4e1ca6c0e938ca57f45c0aa.png)

![image](https://img-blog.csdnimg.cn/img_convert/900c9fe7013d0d761d86da7ccac55fd3.png)

### 2.4.2 职位和学历的分析

![image](https://img-blog.csdnimg.cn/img_convert/bcbec1c0d526fac2e2c8f6f66fca4116.png)

### 2.4.3 薪资分析

![image](https://img-blog.csdnimg.cn/img_convert/2a2a5cb5e87327e97174dd963652c1ce.png)

#### 2.4.3.1 平均薪资柱状图

![image](https://img-blog.csdnimg.cn/img_convert/fe71cef5453aa007fd5233231f1597c4.png)

#### 2.4.3.2 箱线图—不同城市的平均薪资分布情况

![image](https://img-blog.csdnimg.cn/img_convert/205106306194393fc83a18573be2f8a5.png)

#### 2.4.3.3 各地区岗位需求前10的平均薪资情况

![image](https://img-blog.csdnimg.cn/img_convert/d9c75f042282885f00d073ace360404b.png)

### 2.4.4 公司类型分析

![image](https://img-blog.csdnimg.cn/img_convert/ab49bd879b597a3399aad9f15a6a6677.png)

### 2.4.5 公司职位分析

![image](https://img-blog.csdnimg.cn/img_convert/9813e3b0839cdbc34db78fba05330dd4.png)

![image](https://img-blog.csdnimg.cn/img_convert/c53dbb4470f4321b5d94140437258094.png)

### 2.4.5公司人数规模分析

![image](https://img-blog.csdnimg.cn/img_convert/4e76854d4ec86c33981f1a3d0d550cd1.png)

# 三、分析总结

**1.就业去向可以根据当地的人才需求和岗位需求量作为指引方向之一，人才需求越大，就业的机会也就越大**

**2.根据岗位排名的分析已经知道，从事计算机，管理等工程师或经理，其待遇和薪资都比较丰厚**

**3.民营企业占大多数招聘公司的比重**

# 四、附录：项目文件

![image](https://img-blog.csdnimg.cn/img_convert/13296f22f09d3585ca76e878171f341e.png)

**下载地址：https://download.csdn.net/download/HXBest/21700279**

