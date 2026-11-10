# ViTalk 金句插件

收藏历史记录里值得重读的表达。插件 ID 是 `vitalk.quotes`。

金句页面由 ViTalk 宿主渲染，不在这个仓库里实现界面。宿主识别到已启用的 `vitalk.quotes` 后，打开内置的金句页。安装包里的 HTML 只是占位，避免把它当成另一套页面。

已收藏的句子写在本机 `localStorage` 键 `vitalk.saved-quotes.v1`。卸载插件只移除安装记录，不删除这些句子。

## 仓库里有什么

- `manifest.json`：名称、版本、权限和页面标题。当前权限为空。
- `vitalk.quotes.vitalk-plugin.json`：可安装的 `vitalk-plugin/v1` 包，版本 `1.0.0`。

当前 ViTalk 客户端在商店里直接安装同一份内置包，不从本仓库下载。公共目录 `orulink-ai/vitalk-plugins` 仍负责已上架插件的审核清单；金句尚未列入该目录。

## 和宿主的分工

改金句的收藏、空状态或「回到历史」时，改 ViTalk 里的金句页面。改插件名称、说明、版本或权限时，改本仓库，并让宿主内置包与这里保持一致。
