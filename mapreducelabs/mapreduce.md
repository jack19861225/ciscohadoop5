# MapReduce 练习

```
1.分析手机号的流量

Java：默认Hadoop是用LongWritable，Text 作为Map输入的数据类型
demo dataset

13121225244 www.baidu.com 80.00 2013-02-03 09:00:02
13121225244 www.baidu.com 80.00 2013-02-03 09:00:02
13121225244 www.baidu.com 80.00 2013-02-03 09:00:02

输出：<key,value> ~ <手机号(Text)，流量(Double)>
输入：<key,value> ~ <偏移量(Long), 文本内容(Text)>

String abc = 'abc'
String abc = new String('abc')

FileInputFormat:

hadoop/hadoop-mapreduce-project/hadoop-mapreduce-client/hadoop-mapreduce-client-core/src/main/java/org/apache/hadoop/mapreduce/lib/input/FileInputFormat.java

TextInputFormat.java:

hadoop/hadoop-mapreduce-project/hadoop-mapreduce-client/hadoop-mapreduce-client-core/src/main/java/org/apache/hadoop/mapreduce/lib/input/TextInputFormat.java

LineRecordReader:

https://github.com/apache/hadoop/blob/trunk/hadoop-mapreduce-project/hadoop-mapreduce-client/hadoop-mapreduce-client-core/src/main/java/org/apache/hadoop/mapreduce/lib/input/LineRecordReader.java

2.分析URL的PV
<key,value> ~ <url,1>

3.分析URL的PV 取出Top 10

value sort
hadoop默认只能对key做sort

适合比较小的url

Job - Url PV
job1 - <url,pv> <pv,url>

二次排序：

<<url,pv>,pv>



```


