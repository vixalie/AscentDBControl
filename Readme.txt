AscentDBControl Project (ADBC)

AscentDBControl是一个轻型的数据库控制器，可以作为MVC框架中的模型使用。ADBC运行于PHP环境中，要求使用PHP 5.3+。
ADBC目前设计支持Mysql、SQLite与MongoDB。为了统一数据查询，ADBC将MongoDB的JSON查询使用SQL重新封装，并同时提供
JSON查询接口。使用常规的SQL语句即可查询MongoDB，但SQL的指令将受到限制。

ADBC还将集成查询结果遍历功能，查询运行后不必输出查询结果，即可在ADBC的结果集缓存中直接使用。

ADBC项目结构分为核心与适配器。适配器采用统一接口设计，核心通过接口访问适配器，由适配器调用PHP中的方法进行数
据库操作，核心自身不直接调用PHP的方法。

数据库连接采用“数据库类型://用户名:密码@数据库地址/数据库名”的连接串，支持多数据库连接。

ADBC自带日志，用于记录数据库的连接情况与查询指令的记录情况。