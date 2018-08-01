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

## 测试环境：

```
dependencies:
- certifi=2016.2.28=py36_0
- pip=9.0.1=py36_1
- python=3.6.2=0
- setuptools=36.4.0=py36_1
- vc=14=0
- vs2015_runtime=14.0.25420=0
- wheel=0.29.0=py36_0
- wincertstore=0.2=py36_0
- pip:
  - boto==2.49.0
  - boto3==1.7.67
  - botocore==1.10.67
  - bz2file==0.98
  - chardet==3.0.4
  - docutils==0.14
  - gensim==3.5.0
  - idna==2.7
  - jieba==0.39
  - jmespath==0.9.3
  - numpy==1.15.0
  - py4j==0.10.7
  - pymongo==3.7.1
  - pymssql==2.1.3
  - python-dateutil==2.7.3
  - requests==2.19.1
  - s3transfer==0.1.13
  - scipy==1.1.0
  - six==1.11.0
  - smart-open==1.6.0
  - urllib3==1.23
  - whoosh==2.7.4
```
