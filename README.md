# 分镜桥 StoryboardBridge

批量将 GPT 分镜准备到即梦新版画布与小云雀自由画布，支持原生素材引用、视频参数、命名与排列。

## 在线更新与网络修复

保留现有本地插件，每台电脑首次接入一次。维护者发布新版后，插件在空闲时自动检查、校验和安装。使用者不需要 GitHub 账号或商店版。

**[下载最新 Windows／Mac 更新助手与修复包](https://github.com/hxyywd/StoryboardBridge/releases/tag/updater-v0.2.0)**

- 已配置过助手，但更新报 read tcp／连接被关闭：完整解压，Windows 运行 `Repair-Windows.cmd`，Mac 运行 `Repair-Mac.command`。程序自动找到原配置，输入 YES 确认，不需要重填插件路径和扩展 ID。若提示占用，退出浏览器后重试。修复保留插件、项目、素材、绑定与全部原配置。
- 首次接入：同一安装包内运行 `Install-Windows.cmd` 或 `Install-Mac.command`，按提示填写原 extension 路径和扩展 ID。之后重新加载原扩展并刷新画布／GPT 页面。首次接入的插件为 0.14.2，更新助手为 0.2.0。
- 插件“在线更新”显示“已连接更新源”后，该电脑才完成接入。推送、引用、排列与编辑过程中会推迟更新。每台电脑都需首次配置一次。

助手 0.2.0 增加 Windows／Mac 系统手动代理读取、同仓库官方 API 备用入口和 HTTP/1.1 兼容重试；HTTPS 证书与签名校验保持开启。不修改系统代理设置，不读取浏览器或代理凭据，不上传项目、素材、图片或音频。当前不执行 PAC 自动代理脚本；认证代理、浏览器内部代理仍可能需要单独适配。

## 验证与源码

插件 0.14.2 的 509 项逻辑／DOM 检查通过。更新助手原生回归与竞争检查、实际 HTTPS CONNECT 代理测试、配置保留与签名验证通过，两个公开更新入口均验证成功。Windows／Mac 实机及用户实际代理环境仍待验收；Mac 助手没有 Apple 开发者签名／公证，因此安装包标记为预发布测试版。

插件源码是 v0.14.2 发布页中的 `StoryboardBridge_Source_v0.14.2.zip`；最新助手源码是助手 0.2.0 发布页中的 `StoryboardBridge_Updater_0.2.0_Source.zip`。页面自动生成的 Source code 仅对应仓库快照。公开文件不含发布私钥、用户项目或素材。

已接入的电脑读取 update/stable.json。这里的代码修改需要正式发布到更新源后才会同步；不会仅凭聊天自动发布。
