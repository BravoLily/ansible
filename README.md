# windows环境：

## pyspark配置：
	在编译环境使用时,需要把 C:/spark-2.2.1-bin-hadoop2.7/python（spark路径）中的pyspark文件夹拷贝到python环境对应的/Lib/site-packages中

## 安装包：
	pip install jieba
	pip install pymongo
	pip install pymssql
	pip install whoosh
	pip install gensim
	pip install py4j

```
如无法安装，可下载whl文件到python安装路径的script文件夹下进行安装：  
	下载地址： http://www.lfd.uci.edu/~gohlke/pythonlibs/  
	安装命令：
	    E:\Python\envs\rank\Scripts>pip install pymssql-2.1.3-cp36-cp36m-win_amd64.whl  
	    E:\Python\envs\rank\Scripts>pip install gensim-3.5.0-cp36-cp36m-win_amd64.whl
```
## 提交命令(win)：
	spark-submit --py-files zipfile bootfile arvg1 arvg2 arvg3
	
	arvg1: kafka配置
	  ZK-quorum:consumer-group-id:topic:number-of-Kafka-partitions-to-consume
	  eg: 192.168.1.225:2181:test_group:Statistic:1
	 
	arvg2: sqlserver配置
	  sqlserver_host:username:password
	  eg: DESKTOP-PSPOMTB\SQL2014:sa:123
	 
	arvg3: mongodb配置
	  mongo_host:mongo_port:username: password
	  192.168.1.225:27017:ycfadmin:123
``` 
eg: 
spark-submit --py-files F:\supersoft.recommendation\supersoft.recommendation.zip F:\supersoft.recommendation\src\main\python\com\supersoft\recommendation\offline\boot.py 192.168.1.225:2181:test_group:Statistic:1 DESKTOP-PSPOMTB\SQL2014:sa:123 192.168.1.225:27017:ycfadmin:123
```	

