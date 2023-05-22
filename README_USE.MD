## IDEA启动以及配置

### 一、数据库

创建以下数据库即可
- /scripts/sql/apolloconfigdb.sql
- /scripts/sql/apolloportaldb.sql

### 启动 apollo-configservice : 8080
```yaml
-Dapollo_profile=github
-Dspring.datasource.url=jdbc:mysql://localhost:3306/ApolloConfigDB?characterEncoding=utf8
-Dspring.datasource.username=root
-Dspring.datasource.password=root
```
### 启动 apollo-adminservice : 8090
```yaml
-Dapollo_profile=github
-Dspring.datasource.url=jdbc:mysql://localhost:3306/ApolloConfigDB?characterEncoding=utf8
-Dspring.datasource.username=root
-Dspring.datasource.password=root
```

### 启动 apollo-portal : 8070

```yaml
-Dapollo_profile=github,auth
-Dspring.datasource.url=jdbc:mysql://localhost:3306/ApolloPortalDB?characterEncoding=utf8
-Dspring.datasource.username=root
-Dspring.datasource.password=root
```