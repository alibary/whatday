### 日期计算程序 V1.2.2 
#### 蒋农 

本程序可以按指定的基准日期计算今天、昨天、明天、月初、月末、年初、年末等日期，并按YYYYMMDD格式返回，也可以取得指定日期的年、月、日。

语法：
```
whatday [关键字]...
```

关键字：
```
(无)或today 今天
yesterday   昨天
tomorrow    明天
+N(N为整数) N天以后
-N(N为整数) N天以前
lastyear    上年同期
nextyear    下年同期
lastmon     上月同期
nextmon     下月同期
beginyear   年初
endyear     年末
beginqtr    季初
endqtr      季末
beginmon    月初
endmon      月末
beginday    日初（0点0分0秒）
endday      日末（23点59分59秒）
monday      星期一
tuesday     星期二
wednesday   星期三
thursday    星期四
friday      星期五
saturday    星期六
sunday      星期日
year        年份
month       月份
day         日
-	    从标准输入读入日期
(YYYYMMDD)   指定日期
help        显示帮助信息
```

示例：
1. 没有任何参数，返回当天的日期
```
whatday #返回当天的日期
```
2. 使用一个参数
```
whatday lastyear #返回上年同期的月末
```
3. 使用多个参数，从右至左依次执行关键字
```
whatday endmon lastyear #返回上年同期的月末
```
4. 参数如果为 - ，从标准输入读一个基准日期
```
whatday beginmon | whatday +7 - #返回月初后的7天
```
5. 参数如果为日期，返回指定的日期
```
whatday endday 20140326 #返回2014-03-26 23:59:59
```
