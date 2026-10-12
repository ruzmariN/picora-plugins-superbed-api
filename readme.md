# 聚合图床Superbed (API版)
为 Picora 添加 [聚合图床](https://www.superbed.cn/) 图片上传支持。插件使用兼容接口 `POST /upload`，上传单张图片并读取响应中的直链 `url`。

聚合图床的API Key获取需要订阅会员，如果不满足此条件可使用账号登录版。

## 使用

1. 在聚合图床用户中心获取具有上传权限的 API Key。
2. 在Picora中安装此插件。
3. 新建「聚合图床 (Superbed)」配置，填写 API Key 后选择图片上传。

## 说明
- 请求发往 `https://api.superbed.cn/upload`，以 `X-API-Key` 请求头传递密钥，以 multipart/form-data 的 `file` 字段发送图片。只有 HTTP 200 且响应 `err` 为数字 `0` 时才视为成功；错误说明从 `msg` 读取。上传请求不会跟随重定向或自动重传。
- 该插件只支持上传，图床管理/删除请前往[聚合图床](https://www.superbed.cn)账号后台。

## 许可

[MIT](LICENSE)。

> 这是第三方适配插件，不代表聚合图床官方。