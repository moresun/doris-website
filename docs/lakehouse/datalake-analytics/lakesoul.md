---
{
    "title": "LakeSoul",
    "language": "en"
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

## Instructions for use

1. The currently adapted version of the LakeSoul is 2.5.4
2. Spports Parquet format
3. Supports Doris source

## Create Catalog

LakeSoul Catalog uses postgres tables to store all the metadata.

### Sql

```
create catalog lakesoul properties (
'type'='lakesoul',
'lakesoul.pg.username'='lakesoul_test',
'lakesoul.pg.password'='lakesoul_test',
'lakesoul.pg.url'='jdbc:postgresql://127.0.0.1:5432/lakesoul_test?stringtype=unspecified'
);
```
You need to set up lakesoul environment from https://www.dmetasoul.com/docs/lakesoul/Getting%20Started/setup-local-env/
and set postgres username,passoword and url where creating catalog
