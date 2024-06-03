---
{
    "title": "LakeSoul",
    "language": "zh-CN"
}
---

<!-- 
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

## 使用须知

1. 当前适配的 LakeSoul 版本为 2.5.4
2. 支持parquet格式
3. 目前支持Source读操作

## 创建 Catalog

LakeSoul Catalog 当前支持通过Postgres 创建 Catalog,所有元数据通过表格形式进行存储。

### Sql

```
create catalog lakesoul properties (
'type'='lakesoul',
'lakesoul.pg.username'='lakesoul_test',
'lakesoul.pg.password'='lakesoul_test',
'lakesoul.pg.url'='jdbc:postgresql://127.0.0.1:5432/lakesoul_test?stringtype=unspecified'
);
```
需要先启动Postgres服务,创建元数据相关表,然后创建本地环境,具体搭建步骤请参考 https://www.dmetasoul.com/docs/lakesoul/Getting%20Started/setup-local-env/

Doris中在创建Catalog时 需要指定Postgres相关用户名、密码和连接URL