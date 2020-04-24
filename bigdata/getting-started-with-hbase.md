Getting started with HBase
=============================

#### To invoke Hbase shell

hbase shell

#### HBase Version - Provides the version of HBase being used.
```bash
hbase(main):001:0> version
```

#### HBase help 
```bash
hbase(main):002:0> help
```

#### HBase Status - Provides the status of HBase, for example, the number of servers.
```bash
hbase(main):003:0> status
```

#### HBase list_namespace
Please note that there are two namespaces - one is default and another one is hbase (system namespace for internal tables)
```bash
hbase(main):004:0> list_namespace
```

#### HBase create_namespace
```bash
hbase(main):005:0> create_namespace 'datacouch'
```
**Note-** To drop Namespace [ drop_namespace <name of namespace> ] will drop namespace 

#### HBase create user
```bash
hbase(main):006:0> create 'user', {NAME=>'profile', VERSIONS=>5} , {NAME=>'pics'}
```
Please note that Table name and Column Family name are mandatory and rest everything is optional

#### HBase list - Lists all the tables in HBase.
```bash
hbase(main):007:0> list
```

#### Describe table
```bash                 
hbase(main):008:0> describe 'user'
```

#### HBase put - Puts a cell value at a specified column in a specified row in a particular table.
```bash
hbase(main):009:0> put 'user', 'user1', 'profile:fname', 'Tom'
hbase(main):010:0> put 'user', 'user1', 'profile:lname', 'Mathew'
```

#### HBase get - Fetches the contents of row or a cell.
```bash
hbase(main):011:0> get 'user', 'user1', {COLUMN => 'profile:fname'}
```

#### scan - Scans and returns the table data.
```bash
hbase(main):012:0> scan 'user'
```
