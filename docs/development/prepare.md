##确定授权类型

OAuth 2.0的运行流程如下图
![摘自RFC 6749](img/bg2014051203.png)

     (A) 用户打开客户端以后，客户端要求用户给予授权。  
     (B) 用户同意给予客户端授权。  
     (C) 客户端使用上一步获得的授权，向认证服务器申请令牌。  
     (D) 认证服务器对客户端进行认证以后，确认无误，同意发放令牌。  
     (E) 客户端使用令牌，向资源服务器申请获取资源。  
     (F) 资源服务器确认令牌无误，同意向客户端开放资源。  

OAuth 2.0定义了四种授权方式，FitGreat统一认证平台实现了以下几种：

    授权码模式（authorization code）
    密码模式（resource owner password credentials）
    客户端模式（client credentials）


根据客户端实际需要选择授权模式，并申请客户端密钥。  

* * * 

##申请客户端密钥
当前客户端创建和管理由平台管理员完成，如有需要，请联系 [管理员邮箱](mailto:ryanren@fitgreat.cn)。  
需要提供的信息包括：
<table>
    <thead>
        <td>名称</td>
        <td>类型</td>
        <td>描述</td>
    </thead>
    <tbody>
        <tr>
            <td>客户端名称</td>
            <td>文本</td>
            <td>描述客户端</td>
        </tr>
         <tr>
            <td>客户端地址</td>
            <td>文本</td>
            <td>客户端web访问地址，没有可以不填</td>
        </tr>
         <tr>
            <td>访问范围</td>
            <td>选项</td>
            <td>当前可以访问的内容有基本信息，声网Token接口</td>
        </tr>
        <tr>
            <td>授权类型</td>
            <td>文本</td>
            <td>填写授权类型</td>
        </tr>
        <tr>
            <td>回调地址</td>
            <td>多行文本</td>
            <td>如果是授权码模式，请填写合法的回调地址</td>
        </tr>
    </tbody>
</table>