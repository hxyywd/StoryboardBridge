# 分镜桥 StoryboardBridge

将 GPT 分镜批量准备到小云雀自由画布与即梦新版画布：正文、原生素材引用、时长与模型参数、视频命名及排列。

## 本地插件自动更新

保留当前本地插件，每台电脑首次接入一次；维护者发布新版后，插件在空闲时自动检查、下载和安装。无需商店版，使用者无需 GitHub 账号。

**[下载 v0.14.1 首次接入包](https://github.com/hxyywd/StoryboardBridge/releases/tag/v0.14.1)**

- Windows 下载 `StoryboardBridge_AutoUpdate_Windows_v0.14.1.zip`，运行 `Install-Windows.cmd`。
- Intel Mac／Apple 芯片 Mac 下载 `StoryboardBridge_AutoUpdate_Mac_v0.14.1.zip`，运行 `Install-Mac.command`。
- 暂停推送、关闭侧栏，填写原 extension 文件夹路径和原扩展 ID。不要删除或重装扩展。完成后重新加载扩展并刷新画布／GPT 页面，详细步骤见安装包内 README.md。
- 插件“在线更新”显示“已连接更新源”后，该电脑才完成配置。每台电脑都需要首次配置一次，以后不再手动下载安装包。

保留原目录、扩展 ID、项目、素材、风格库与视频关联。推送／引用／排列中等待，最近 30 秒编辑过侧栏也等待；空闲后校验签名与 SHA-256、替换代码并重新加载。损坏包、倒退版本、权限扩张不自动安装。网页不会被强制刷新，更新后继续推送前刷新旧网页。只拉取更新文件，不上传项目或素材。0.14.1 增加持续原生连接，避免慢网络下载中浏览器休眠。

## 验证与源代码

508 项插件逻辑／DOM 回归通过；更新助手协议、签名、坏包拒绝、替换与回退测试通过。公开更新源的下载安装与回退模拟已通过。Windows x64／ARM64、macOS Intel／Apple Silicon 已交叉编译；Windows／Mac 实机安装及浏览器联调尚待验证，Mac 程序目前没有 Apple 开发者签名／公证，因此接入包标记为预发布测试版。

完整源码是发布页中的 `StoryboardBridge_Source_v0.14.1.zip`，包含插件、助手、测试与发布说明。请不要把页面自动生成的 Source code 当作完整源码。使用者安装包不含发布私钥、用户项目备份、素材或诊断。

已接入的电脑读取 update/stable.json。聊天中的代码修改必须发布到更新源后才会同步，不能仅凭聊天自动推送。
