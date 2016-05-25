#Hadoop 集群规划

 ```
 Hadoop依赖的技术环境
 
      Java,Linux（CentOS),数据库（MySQL,Postgresql, Oracle）,Python 2.7.X\2.6.X
      安全：Kerberos
      
      JDK1.7.0_55, CentOS 6.5,建议Postgresql, Python 2.7.X,SSH

 Hadoop软件:
 
 MapR,Cloudera,Hortonworks
 
 Hadoop常见安装方式:Yum,RPM,Parcels(Cloudera 特有)
 
 硬件规划
 
 服务器：管理节点，计算节点
       
       CPU: 1 core ~ 1 Task
       MEM: 1 core ~ 2~4G MEM
       DISK: SSD，SAS，SATA 1 core～ 1～2T存储
       Network: 千兆，万兆但是一定要做网卡绑定

 交换机：影响，数据在网络中的传输速度
         注意：Spark项目，或者集群任务量非常大，
         关心：同时运行的任务量，每一个任务大概需要访问多少数据        
  防火墙：
  FTP服务器: 
  文件服务器:

  Namenode 内存是96G
    
  OS:8G
  NameNode : 非堆 8G
               堆：80G

  Datanode 64G ，Zookeeper 
    
  OS:8G
  Datanode:4G
  Zookeeper :8G
  
```
