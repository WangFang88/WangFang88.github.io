# 情侣邀请落地页（GitHub Pages）

Universal Link 的 `apple-app-site-association` **必须挂在域名根**  
`https://WangFang88.github.io/.well-known/apple-app-site-association`，  
因此本目录内容需要发布到 **用户站仓库** `WangFang88.github.io`（不是 `JiaClock` 项目站的 `/JiaClock/` 路径）。

## 一次性部署

1. 在 GitHub 新建公开仓库：**`WangFang88.github.io`**
2. 将本目录 `invite-web/` 下的全部文件推到该仓库的 **默认分支根目录**（保留 `.well-known/`、`couple/`、`apple-app-site-association`）
3. 仓库 Settings → Pages → Source：Deploy from branch → `main` / root
4. 等待约 1–2 分钟后验证：
   - https://WangFang88.github.io/.well-known/apple-app-site-association
   - https://WangFang88.github.io/couple/join?code=TESTCODE

## App 侧已配置

- Associated Domains：`applinks:WangFang88.github.io`
- 邀请 HTTPS：`https://WangFang88.github.io/couple/join?code=XXXXXXXX`
- Team / Bundle：`CR7GXH4RAJ.jdarray.JiaClock`
- App Store：`id6776895229`

## Apple Developer

App ID `jdarray.JiaClock` 需勾选 **Associated Domains**，并用含该 capability 的描述文件重新签名。
