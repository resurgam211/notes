#

<h1 align="center" >奇技淫巧</h1>

## 目录

* [SSM学习](#SSM学习)
  * [标签](标签#)
    * [@Param](#@Param)

* [MD文件转换](#MD文件转换)
  * [md2docx](#pandoc)
  * [md2PDF](#md2PDF)

### SSM学习

#### 标签

##### @Param

    这个标签用于给mybatis的mapper一个标识，让值正确的传入

``` java
#dao层

User getUserByName(@Param("dog") String name);
```

``` xml
>Maaper配置文件

<select resultType="com.xxx.User" parameterType="java.lang.String">
select * from users where name=#{dog} <!-- 让这里正确获得参数name -->
</select>
```

### MD文件转换

#### pandoc/md2docx

    转换md文件：CD文件目录
    pandoc file.md -s -o file.docx

#### md2PDF

    vscode F1
    输入 `export`
    输入 markdown to PDF
