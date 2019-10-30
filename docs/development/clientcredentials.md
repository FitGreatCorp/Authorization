##授权流程
Client Credentials 授权流程如下图：
![Client Credentials](img/bg2014051207.png)


    （A）客户端向认证服务器进行身份认证，并要求一个访问令牌。  
    （B）认证服务器确认无误后，向客户端提供访问令牌。



* * * 

##调用接口描述
**认证服务器接口地址**
<table>
    <tr>
        <td>地址</td>
        <td>说明</td>
    </tr>
    <tr>
        <td>https://login.fitgreat.cn/oauth/common/authorize</td>
        <td>认证服务器认证地址</td>
    </tr>
    <tr>
        <td>https://login.fitgreat.cn/oauth/v2/token</td>
        <td>token获取接口地址</td>
    </tr>
</table>

**A步骤中**，客户端发出的HTTP请求，包含以下参数：

granttype：表示授权类型，此处的值固定为"clientcredentials"，必选项。  
scope：表示权限范围，可选项。  


         POST /token HTTP/1.1
         Host: server.example.com
         Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW
         Content-Type: application/x-www-form-urlencoded

         grant_type=client_credentials

认证服务器必须以某种方式，验证客户端身份。

---

**B步骤中**，认证服务器向客户端发送访问令牌，下面是一个例子。


         HTTP/1.1 200 OK
         Content-Type: application/json;charset=UTF-8
         Cache-Control: no-store
         Pragma: no-cache

         {
           "access_token":"2YotnFZFEjr1zCsicMWpAA",
           "token_type":"example",
           "expires_in":3600,
           "example_parameter":"example_value"
         }

