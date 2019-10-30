**认证服务器接口地址**
<table>
    <tr>
        <td>地址</td>
        <td>说明</td>
    </tr>
    <tr>
        <td>https://login.fitgreat.cn/oauth/v2/introspection</td>
        <td>Introspection接口地址</td>
    </tr>
</table>

针对资源服务器，如需校验用户token，则传入以下参数进行调用：

    token：用于校验的token，必选项。
    token_type_hint：用于校验的token类型，必选项。

下面是一个例子。


     POST /introspect HTTP/1.1
     Host: server.example.com
     Accept: application/json
     Content-Type: application/x-www-form-urlencoded
     Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW

     token=mF_9.B5f-4.1JqM&token_type_hint=access_token 

