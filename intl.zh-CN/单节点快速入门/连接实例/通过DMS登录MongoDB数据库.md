# 通过DMS登录MongoDB数据库 {#concept_xdd_13v_cgb .concept}

您可以通过[数据管理服务DMS](https://www.alibabacloud.com/help/zh/doc-detail/47550.htm)登录MongoDB数据库。使用DMS您可以更便捷地对MongoDB数据库进行管理。

## 注意事项 {#section_tqx_53v_cgb .section}

通过DMS登录MongoDB实例的数据库时，须使用MongoDB实例的内网连接地址，暂不支持公网连接地址。

## 准备工作 {#section_nlw_mz4_tgb .section}

将下表中的DMS服务器IP地址加入至MongoDB实例的白名单中，操作步骤请参见[设置白名单](intl.zh-CN/单节点快速入门/设置白名单.md#)。

**说明：** 如果您已经将DMS服务器的IP地址加入至MongoDB实例的白名单中，可跳过此步骤。

|MongoDB实例的网络类型|DMS服务器的IP地址|
|:-------------|:----------|
|内网连接 - 专有网络|100.104.0.0/16|

## 操作步骤 {#section_wtq_x3v_cgb .section}

1.  登录[MongoDB管理控制台](https://mongodb.console.aliyun.com/)。
2.  在页面左上角，选择实例所在的地域。
3.  在左侧导航栏，单击**副本集实例列表**。
4.  找到目标实例，单击实例ID。
5.  单击左侧导航栏的**数据库连接**，获取 Primary 节点的内网连接地址。

    ![MongoDB内网连接地址](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23695/156747847334538_zh-CN.png)

6.  单击右上角的**登录数据库**，跳转至数据管理控制台页面。
7.  在数据管理控制台页面，填写如下信息登录MongoDB数据库。

    ![DMS登录MongoDB页面](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23695/156747847313740_zh-CN.png)

    -   网络地址及端口：填入Primary节点的内网连接地址。
    -   数据库用户名：默认为 root 。
    -   数据库：鉴权数据库，默认为 admin 。
    -   密码：数据库登录密码，如忘记密码可[重置密码](intl.zh-CN/单节点快速入门/设置密码.md#)。
8.  单击**登录**。

## 相关问题 {#section_02s_xo9_vmh .section}

-   [排查 Mongo Shell 登录问题](../../../../intl.zh-CN/常见问题/热点问题/排查 Mongo Shell 登录问题.md#)
-   [排查因连接数耗尽导致的数据库连接问题](../../../../intl.zh-CN/常见问题/热点问题/排查因连接数耗尽导致的数据库连接问题.md#)
-   [排查 MongoDB CPU使用率高的问题](../../../../intl.zh-CN/最佳实践/排查MongoDB CPU使用率高的问题.md#)
-   [如何查询及限制连接数](../../../../intl.zh-CN/常见问题/热点问题/如何查询及限制连接数.md#)

## 更多信息 {#section_zsr_lf2_qgb .section}

建议在生产环境中不要直接使用 root 用户登录数据库。您可以根据业务需求，创建用户并分配权限，详情请参见[使用DMS管理MongoDB数据库用户](../../../../intl.zh-CN/用户指南/账号管理/使用DMS管理MongoDB数据库用户.md#)。

