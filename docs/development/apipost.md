**Resource API接口地址**
<table>
    <tr>
        <td>地址</td>
        <td>说明</td>
    </tr>
    <tr>
        <td>https://login.fitgreat.cn/oauth/v2/api/me</td>
        <td>获取个人信息接口</td>
    </tr>
     <tr>
        <td>https://login.fitgreat.cn/oauth/v2/agora/token</td>
        <td>获取声网token接口</td>
    </tr>
</table>

如需访问资源服务器api，需校验用户token，请求头传入Bearer Token参数进行调用：  

下面是一个例子。

     POST /api/me HTTP/1.1
     Host: server.example.com
     Accept: application/json
     Content-Type: application/x-www-form-urlencoded
     Authorization: Bearer czZCaGRSa3F0MzpnWDFmQmF0M2JW

