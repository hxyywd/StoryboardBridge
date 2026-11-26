# 分镜桥 StoryboardBridge

将 GPT 分镜批量准备到小云雀自由画布与即梦新版画布：正文、原生素材引用、时长与模型参数、视频命名及排列。

## 本地插件自动更新

保留当前本地插件，不需要换成商店版。每台电脑首次接入一次；此后维护者发布新版，插件在空闲时自动下载、验证和更新。使用者不需要 GitHub 账号。

**[下载 v0.14.0 首次接入包](https://github.com/hxyywd/StoryboardBridge/releases/tag/v0.14.0)**

- Windows 下载 `StoryboardBridge_AutoUpdate_Windows_v0.14.0.zip`，运行 `Install-Windows.cmd`。
- Intel Mac 与 Apple 芯片 Mac 下载 `StoryboardBridge_AutoUpdate_Mac_v0.14.0.zip`，运行 `Install-Mac.command`。
- 暂停推送、关闭侧栏，按提示填写原 `extension` 文件夹路径和扩展 ID；不要删除或重装当前扩展。接入后重新加载扩展、刷新画布与 GPT 页面。具体步骤见包内 README.md。
- 插件“在线更新”显示“已连接更新源”才表示该电脑完成接入。首次接入之后，后续不需要再手动下载安装包。

保留原插件目录与扩展 ID，不清空项目、素材、风格库或视频关联。推送、引用、排列过程中推迟更新；最近 30 秒编辑过侧栏时也等待。签名和校验失败、版本倒退或权限扩张不会自动安装。网页不强制刷新，更新后继续推送前刷新旧标签页。只拉取公开更新文件，不上传项目、素材或登录信息。

## 验证与源代码

508 项插件逻辑／DOM 回归通过，更新助手的协议、签名、坏包拒绝、替换与回退测试通过。Windows x64／ARM64、macOS Intel／Apple Silicon 已交叉编译；Windows／Mac 安装及浏览器联调尚待实机验收，Mac 程序目前没有 Apple 开发者签名／公证。因此首次接入包标记为预发布测试版。

完整源代码是发布页中的 `StoryboardBridge_Source_v0.14.0.zip`，含插件、更新助手、测试与发布说明。页面自动生成的“Source code”只对应仓库快照，请选择上述完整源码包。消费者包不含发布私钥、用户项目备份、素材或诊断。

已接入的电脑读取 `update/stable.json`。聊天中的修改必须发布到更新源后才会同步，不能仅凭聊天自动推送。
