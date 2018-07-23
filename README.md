# normandy
Ansible -> (OpenLDAP + saslauth + google_authenticator + portal)

# 简介
一个由Ansible部署的简便的 CentOS7.2 server CLI 用户登录认证小系统

# 步骤
执行playbooks或scripts，完成此系统的安装配置;
根据ldap中的用户，在portal server创建用户账户;
通过portal节点登录到servers of cluster

# 说明
## OpenLDAP + saslauth + google_authenticator 节点：
配置username和email，生成用户密码，验证用户登录

## portal节点:
根据在ldap注册的用户，创建相应user，并把user的公钥push到各个服务器;
登录到其他服务器的入口

## servers of cluster:
目的地: normandy
