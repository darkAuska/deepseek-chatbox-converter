# DeepSeek 转 Chatbox

把 DeepSeek 导出的聊天记录转换成可导入 Chatbox 的备份。工具是一个独立的 HTML 文件，手机和电脑都可以用浏览器打开。文件在本机处理，无需登录转换器或上传聊天记录。

## 在线使用

**[打开 DeepSeek 转 Chatbox 转换器](https://darkauska.github.io/deepseek-chatbox-converter/)**

iPhone / iPad 请在 Safari 中打开链接。用原始 DeepSeek ZIP 转换后，在 Safari 的下载列表或「文件 → 下载」找到生成的 ZIP。如果页面有「分享 ZIP」，也可以点它后选「存储到文件」。在 Chatbox 导入时选择保存的 ZIP。

## 下载离线版

打开 [deepseek-chatbox-converter.html](./deepseek-chatbox-converter.html) 的文件页面，点 **Download raw file**（下载图标）。也可以在仓库首页点 **Code → Download ZIP**，解压后找到同名的 HTML 文件。

手机用户可以直接使用上面的在线版。iPhone / iPad 的「文件」预览可能只显示 HTML 页面，转换请用 Safari 打开在线版。

## 使用

1. 从 DeepSeek 导出聊天记录，保存原始 ZIP。新版导出直接选 ZIP。
2. 在浏览器打开在线转换器。电脑也可以用 Chrome、Edge 或 Safari 打开下载的 **deepseek-chatbox-converter.html**。
3. 点 **选择 DeepSeek 导出文件 → 开始转换**。分包大小可以先用默认的 **约 64 MB**。
4. 点 **下载 ZIP** 或 **分享 ZIP**。若显示 **下载并继续**，按提示把各包分别保存。
5. 打开 Chatbox，进入 **设置 → 数据与备份 → 导入备份**，逐个选择生成的 ZIP。生成的备份直接导入即可。

## 转换范围

| DeepSeek 输入格式 | 可保留的内容 |
| --- | --- |
| 新版官方 ZIP | 会话标题、问答、思考过程、图片、可读取的文件附件和回复分支 |
| 旧版 `conversations.json` | 当前分支的文字和思考过程 |

DeepSeek 的账号信息、搜索工具记录和站内提示不随备份迁移。单个会话的原始 JSON 上限为 **32 MB**。转换大文件时会优先使用浏览器的本地临时空间，空间受限时会逐包下载。单个会话会放在同一包里，因此实际包大小可能超过目标值。

## 验证

用新版导出的 ZIP 验证了 **135 个会话、1,164 条消息和 76 张图片**。桌面 Chrome 已完成解压后 **120 MB** 测试数据的分包转换与下载。安卓和 iPhone 真机尚未逐项验证。
