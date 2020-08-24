```
参考文档:https://www.cnblogs.com/dukuan/p/9983899.html
1. 配置文件在`./environment/my-env.startup.yaml`，如有更改需要用`sh file-to-base64.sh my-env.startup.yaml`重新生成后替换`./ldap-secret.yaml`里对应值
2. 持久化已挂载到`./openldap-data`，确实需要删除，请备份整个目录数据，`openldap-pv-pvc.yml`在持久化数据被删除之后才需要重新创建
3. `phpldapadmin.yaml`为管理页面，在需要的时候创建以连接`ldap`，不需要的时候为了安全，应该将其删除`kubectl delete -f phpldapadmin.yaml`
```
