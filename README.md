# OpenAI/ChatGPT 免翻墙代理

据很多网友反应，**OpenAI 检测到中国的 API
访问时，会直接封号**。所以可以在国外的服务器上搭建了一个代理，用于访问
OpenAI/ChatGPT 的 API。

## 方式一：使用 Deno

```bash
deno run --allow-net --allow-read --allow-env --watch main.ts
```

### 部署

点击[这个链接][1]，可以快速一键部署到 Deno Deploy 上。

然后在 Settings 选项卡里可以设置自定义二级域名，或者绑定自己的域名。

## 方式二：使用 Cloudflare Workers
1. 新建一个 Cloudflare 账号。
2. 注册一个域名、可以使用阿里云等。
3. 将新注册域名的 DNS 解析转到 Cloudflare。如果在 Cloudflare 购买的域名可以忽略这一步。
4. 打开 Cloudflare 管理后台 Workers 标签，创建新的服务，将 cloudflare/index.js 里面的代码复制到 Cloudflare
5. 在把域名绑定一下。

[1]: https://dash.deno.com/new?url=https://raw.githubusercontent.com/QuincySx/proxy-openai/master/main.ts
