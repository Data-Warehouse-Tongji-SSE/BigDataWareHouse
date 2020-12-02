# BigDataWarehouse

> 2020年数据仓库大项目
### 数据集信息
**原始数据来源**：http://snap.stanford.edu/data/web-Movies.html 

该数据集包含来自亚马逊的电影评论。数据的使用期超过10年，包括截至2012年10月的所有约800万条评论。评论包括产品和用户信息，评分以及纯文本评论。

**数据扩充**：爬取原始数据集中涉及到的所有产品ID对应的亚马逊网页

### 数据仓储

使用Neo4j, Mysql 和 Hive 三种类型数据库进行仓储，并进行查询性能比较。

## Folder Structure

```
.
├── ETL                         # ETL脚本项目
│   ├── processedData           # 处理后的数据
│   │   └── neo4jcsv            # neo4j入库需要的csv文件
│   ├── rawData                 # 存放原始数据集(movies.txt)
│   └── utils                   # ETL工具模块
│       ├── deduplicate         # 原始数据去重的模块
│       └── neo4jPreprocess     # 处理数据为neo4j所需的csv格式的模块
│           ├── csvData
│           └── model
├── neo4j
│   ├── conf
│   ├── data
│   │   ├── databases
│   │   │   ├── neo4j
│   │   │   └── system
│   │   │       └── schema
│   │   └── transactions
│   │       ├── neo4j
│   │       └── system
│   ├── import
│   ├── logs
│   └── plugins
└── ...
```

## Requirements

### ETL Project

```shell
pip install -r requirements.txt
```

## Usage

### ETL Project

```shell
python run.py
```


