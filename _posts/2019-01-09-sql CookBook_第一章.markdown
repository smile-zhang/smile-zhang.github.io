###### 1.1 在where 子句中引用取别名的列
```
   select * from (select * sal as salary where emp) as x where salary>200;
```
###### 1.2 连接列值(多列的查询结果合并为一列)
```   
    mysql
    SELECT CONCAT(ENAME,' works as a ',JOB) as msg FROM emp where DEPTNO=10;
    
    DB2 Oracle，PostgreSQL
    select ename || ' works as a ' || job as msg from emp ;

    SQL server
    select ename + ' works as a ' + job as msg from emp;
```
###### 1.3 在select 语句中使用条件逻辑（case when...then...else..end as ..）
```
    SELECT	ENAME,	SAL,
    CASE	WHEN sal <= 2000 THEN 'underpaid'
    	    WHEN sal > 4000 THEN 'overpaid'
    	    ELSE 'ok'
    	    END as status 
    	    from emp ;
```
#### 1.4 限制返回的行数
```
    mysql  postgreSQL
    
    
    
```
