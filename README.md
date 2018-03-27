# MySQL简明教程/速查
本教程用于:
1. 入门学习
2. 快速查询
- 初稿完成于2018/3/13 by [nightttt7](https://github.com/nightttt7) and [lotus3333](https://github.com/lotus3333)

# todo
1. 完善 游标
2. 触发器
3. 函数
4. 引擎
5. 数据库设置与安全
6. 范式
7. 更多的实战

# 目录
0. [合并教程](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%90%88%E5%B9%B6%E6%95%99%E7%A8%8B.md)

1. [windows下的MySQL安装](https://github.com/nightttt7/MySQL-tutorial/blob/master/windows%E4%B8%8B%E7%9A%84MySQL%E5%AE%89%E8%A3%85.md)

2. [linux下的MySQL安装](https://github.com/nightttt7/MySQL-tutorial/blob/master/linux%E4%B8%8B%E7%9A%84MySQL%E5%AE%89%E8%A3%85.md)

3. [增删查改](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md)
    1. [创建](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E5%88%9B%E5%BB%BA)
    2. [插入](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E6%8F%92%E5%85%A5)
    3. [更新](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E6%9B%B4%E6%96%B0)
    4. [简单检索](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E7%AE%80%E5%8D%95%E6%A3%80%E7%B4%A2)
    5. [删除](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E5%88%A0%E9%99%A4)
    6. [示例代码](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%A2%9E%E5%88%A0%E6%9F%A5%E6%94%B9.md#%E7%A4%BA%E4%BE%8B%E4%BB%A3%E7%A0%81)

4. [过滤](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%BF%87%E6%BB%A4.md)
    1. [WHERE 单一条件过滤](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%BF%87%E6%BB%A4.md#where-%E5%8D%95%E4%B8%80%E6%9D%A1%E4%BB%B6%E8%BF%87%E6%BB%A4)
    2. [WHERE 多子句过滤](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%BF%87%E6%BB%A4.md#where-%E5%A4%9A%E5%AD%90%E5%8F%A5%E8%BF%87%E6%BB%A4)
    3. [通配符过滤](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%BF%87%E6%BB%A4.md#%E9%80%9A%E9%85%8D%E7%AC%A6%E8%BF%87%E6%BB%A4)

5. [数据处理,汇总,分组](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md)
    1. [创建计算字段](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md#%E5%88%9B%E5%BB%BA%E8%AE%A1%E7%AE%97%E5%AD%97%E6%AE%B5)
    2. [函数处理数据](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md#%E5%87%BD%E6%95%B0%E5%A4%84%E7%90%86%E6%95%B0%E6%8D%AE)
    3. [汇总数据](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md#%E6%B1%87%E6%80%BB%E6%95%B0%E6%8D%AE)
    4. [数据分组](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md#%E6%95%B0%E6%8D%AE%E5%88%86%E7%BB%84%E9%80%82%E7%94%A8%E4%BA%8E%E5%A4%9A%E5%88%97%E6%95%B0%E6%8D%AE)
    5. [select子句顺序](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%A4%84%E7%90%86%2C%E6%B1%87%E6%80%BB%2C%E5%88%86%E7%BB%84.md#select%E5%AD%90%E5%8F%A5%E9%A1%BA%E5%BA%8F)

6. [子查询,组合查询,联结](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%AD%90%E6%9F%A5%E8%AF%A2%2C%E7%BB%84%E5%90%88%E6%9F%A5%E8%AF%A2%2C%E8%81%94%E7%BB%93.md)
    1. [子查询](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%AD%90%E6%9F%A5%E8%AF%A2%2C%E7%BB%84%E5%90%88%E6%9F%A5%E8%AF%A2%2C%E8%81%94%E7%BB%93.md#%E5%AD%90%E6%9F%A5%E8%AF%A2)
    2. [联结](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%AD%90%E6%9F%A5%E8%AF%A2%2C%E7%BB%84%E5%90%88%E6%9F%A5%E8%AF%A2%2C%E8%81%94%E7%BB%93.md#%E8%81%94%E7%BB%93)
    3. [组合查询](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%AD%90%E6%9F%A5%E8%AF%A2%2C%E7%BB%84%E5%90%88%E6%9F%A5%E8%AF%A2%2C%E8%81%94%E7%BB%93.md#%E7%BB%84%E5%90%88%E6%9F%A5%E8%AF%A2)

7. [约束,外键,索引](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E7%BA%A6%E6%9D%9F%2C%E5%A4%96%E9%94%AE%2C%E7%B4%A2%E5%BC%95.md)
    1. [约束](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E7%BA%A6%E6%9D%9F%2C%E5%A4%96%E9%94%AE%2C%E7%B4%A2%E5%BC%95.md#%E7%BA%A6%E6%9D%9F-constraint)
    2. [外键](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E7%BA%A6%E6%9D%9F%2C%E5%A4%96%E9%94%AE%2C%E7%B4%A2%E5%BC%95.md#%E5%A4%96%E9%94%AE)
    3. [索引](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E7%BA%A6%E6%9D%9F%2C%E5%A4%96%E9%94%AE%2C%E7%B4%A2%E5%BC%95.md#%E7%B4%A2%E5%BC%95)

8. [视图,存储过程,游标](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%A7%86%E5%9B%BE%2C%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B%2C%E6%B8%B8%E6%A0%87.md)
    1. [视图](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%A7%86%E5%9B%BE%2C%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B%2C%E6%B8%B8%E6%A0%87.md#%E8%A7%86%E5%9B%BE-view)
    2. [存储过程](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%A7%86%E5%9B%BE%2C%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B%2C%E6%B8%B8%E6%A0%87.md#%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B-procedure)
    3. [游标](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%A7%86%E5%9B%BE%2C%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B%2C%E6%B8%B8%E6%A0%87.md#%E6%B8%B8%E6%A0%87-cursor)

9. [事务](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E4%BA%8B%E5%8A%A1.md)

10. [数据类型](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B.md)

11. [文本文档的导入导出](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%96%87%E6%9C%AC%E6%96%87%E6%A1%A3%E7%9A%84%E5%AF%BC%E5%85%A5%E5%AF%BC%E5%87%BA.md)

12. [批处理](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%89%B9%E5%A4%84%E7%90%86.md)

13. [范式 尚未完成](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E8%8C%83%E5%BC%8F.md)

14. [数据库安全与设置 尚未完成](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E6%95%B0%E6%8D%AE%E5%BA%93%E5%AE%89%E5%85%A8%E4%B8%8E%E8%AE%BE%E7%BD%AE.md)

# 实战系列
1. [实战1](https://github.com/nightttt7/MySQL-tutorial/blob/master/%E5%AE%9E%E6%88%981.md)
