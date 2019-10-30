##授权流程
Resource Owner Password Credentials 授权流程如下图：
![Resource Owner Password Credentials](img/bg2014051206.png)

    （A）用户向客户端提供用户名和密码。  
    （B）客户端将用户名和密码发给认证服务器，向后者请求令牌。  
    （C）认证服务器确认无误后，向客户端提供访问令牌。  


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

**B步骤中**，客户端发出的HTTP请求，包含以下参数：

    grant_type：表示授权类型，此处的值固定为"password"，必选项。
    username：表示用户名，必选项。
    password：表示用户的密码，必选项。
    scope：表示权限范围，可选项。

下面是一个例子。


         POST /token HTTP/1.1
         Host: server.example.com
         Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW
         Content-Type: application/x-www-form-urlencoded

         grant_type=password&username=johndoe&password=A3ddj3w

---

**C步骤中**，认证服务器向客户端发送访问令牌，下面是一个例子。


         HTTP/1.1 200 OK
         Content-Type: application/json;charset=UTF-8
         Cache-Control: no-store
         Pragma: no-cache

         {
           "access_token":"2YotnFZFEjr1zCsicMWpAA",
           "token_type":"example",
           "expires_in":3600,
           "refresh_token":"tGzv3JOkF0XG5Qx2TlKWIA",
           "example_parameter":"example_value"
         }

