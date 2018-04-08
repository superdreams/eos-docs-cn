# Database API

存储和检索EOS.IO区块链的数据API根据以下广泛结构来组织数据.

# 模块


## Database C API    
 数据库的C语言接口.

### 详细描述


- code - 具有写入权限的帐户名称.
    - scope - 存储数据的帐户.
        - table - 正在存储的表的名称.
            - record - 表中的一排.

每个事务都指定可以读取和/或写入的一组有效范围。正在运行的代码决定了可以写入的内容;因此，写入操作不允许您指定/配置代码。

> 注意   
尝试在有效范围和/或代码部分之外读取和/或写入会导致您的事务失败。

### 表类型

这些是由索引的数量和大小确定的受支持的表类型：
1. dbi64

databaseCpp提供了一个简单的接口，用于将任何固定大小的结构存储为数据库行。