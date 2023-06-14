# MySQL数据库成图


## 需求说明
链接到MySQL数据库选择指定的表进行成图。


## 带有空间数据成图

带有空间数据是指表中存在`geometry`类型的数据字段。

>   前置操作：创建数据库，
>
>   创建数据表：
>
>   ```
>   CREATE TABLE `a_copy1` (
>     `id` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci DEFAULT NULL,
>     `geometry` geometry DEFAULT NULL
>   ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
>   ```
>
>   在上述数据中`geometry`是空间数据
>
>   插入数据：
>
>   ```
>   INSERT INTO `a`.`a_copy1` (`id`, `geometry`) VALUES ('1', ST_GeomFromText('MULTILINESTRING((119.456968320495 29.2185869231014, 119.457030454832 29.2181936331143))'));
>   INSERT INTO `a`.`a_copy1` (`id`, `geometry`) VALUES ('2', ST_GeomFromText('MULTILINESTRING((119.456968320495 29.2185869231014, 119.457030454832 29.2181936331143))'));
>   INSERT INTO `a`.`a_copy1` (`id`, `geometry`) VALUES ('3', ST_GeomFromText('MULTILINESTRING((119.457030454832 29.2181936331143, 119.456968320495 29.2185869231014))'));
>   ```
>
>   



入口: 依次点击本软件菜单 文件 -> 成图 -> 导入 MySQL。入口界面如图所示

![image-20230614170407455](images/image-20230614170407455.png)

点击导入 MySQL菜单后界面如图所示

![image-20230614170355618](images/image-20230614170355618.png)

点击获取数据按钮进行后续操作。

1.   选择数据库

![image-20230614170445462](images/image-20230614170445462.png)

2.   选择表

![image-20230614170457880](images/image-20230614170457880.png)

3.   选择空间字段

![image-20230614170515087](images/image-20230614170515087.png)

最终点击确定按钮完成成图，最终成图效果如图所示

![image-20230614170545323](images/image-20230614170545323.png)