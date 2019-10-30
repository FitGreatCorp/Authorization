**认证服务器接口地址**
<table>
    <tr>
        <td>地址</td>
        <td>说明</td>
    </tr>
    <tr>
        <td>https://login.fitgreat.cn/oauth/v2/revoke</td>
        <td>Revoke接口地址</td>
    </tr>
</table>

这个协议的API是用于Client撤销access_token或者refresh_token：

    POST /revoke HTTP/1.1
    Host: server.example.com
    Content-Type: application/x-www-form-urlencoded
    Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW

    token=45ghiukldjahdnhzdauz&token_type_hint=refresh_token

其中各项含义如下：

    /revoke：是Authorization Server需要提供的API地址，Client使用Post方式请求这个地址。
    Content-Type: application/x-www-form-urlencoded：固定此格式。
    Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW：访问受保护资源的授权凭证。
    token：必选，可以是access_token或者refresh_token的内容。
    token_type_hint：可选，表示token的类型，值为”access_token“或者"refresh_token"。

如果撤销成功，则返回一个HTTP status code为200的响应。

