# 自定义Git

## 配置Git



## 属性

可以针对特定的路径配置某些设置项, 这些基于路径的设置项被称为 Git 属性

目录下的 .gitattributes 内设置属性

.git/info/attributes 可以设置属性文件是否提交


### 属性作用

- 可以对项目中的文件或目录单独定义不同的合并策略
- 让 Git 知道怎样比较非文本文件
- 让 Git 在提交或检出前过滤内容

### 二进制文件

.gitattributes 文件添加如下 `*.pbxproj binary`

Git 把所有 pbxproj 文件当成二进制文件：Git 不会尝试转换或修正回车换行

### 比较二进制文件

在比较时 对二进制文件运用一个过滤器转化为文本格式，从而能够使用普通的 diff 方式进行对比

.gitattributes 文件中添加 `*.docx diff=word`

所有.docx文件在进行比较是会使用 docx2txt 将文档转为可读文本文件

### 关键字展开



## 挂钩



## Example


