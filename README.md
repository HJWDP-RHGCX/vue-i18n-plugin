<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=kleinwu.front-i18n-auto">
    <img width="200" src="./assets/i18n.png">
  </a>
</p>

<h1 align="center">Vue 国际化自动翻译助手</h1>

本插件用于 Vue 项目添加国际化支援辅助开发之用。可以快速为项目添加国际化支援，同时提供了国际化的翻译功能。

## ✨ 功能

1. 识别 Vue 文件中的中文文本；
2. 自动生成 key；
3. 生成翻译文件；
4. 导出翻译结果；

## 💻 使用

1. 打开 Vue 文件，点击右上角的自动识别中文：
![](./assets/others/20241230-180051.jpeg)
2. 稍等片刻，待其识别完成后，会打开编辑界面：
   ![](./assets/others/20241230-174247.jpeg)
3. 确认 Vue 文件是否还有遗漏的需翻译的中文字符串。如果有，则选中后点击浮窗的`添加到国际化`：
   ![](assets/others/1710671072271.jpeg)
4. 对于不需要翻译的位置，鼠标移动到翻译项位置，点击出现的 `移除翻译位置` 即可：
   ![图 6](assets/others/1710672125889.jpeg)
5. 点击操作的删除按钮可以删除国际化项目，跳转按钮可以跳转到国际化的行。
   ![图 4](assets/others/1710671890941.jpeg)
6. 最后，点击`导出`按钮，同时会将国际化 Key 使用 `$t('key')` 插入到代码中，只要再在代码中加入实现或导入 `$t` 函数即可。
   ![图 4](assets/others/20241230-191931.jpeg)
   ![图 4](assets/others/20241230-191841.jpeg)

## 📦 配置

插件的配置项如下：

- `front-i18n.appId`: 百度翻译接口 appId，若不设置则无法自动生成 Key 与自动翻译导出结果。申请方法见[百度翻译文档](http://api.fanyi.baidu.com/product/113)
- `front-i18n.appKey`: 百度翻译接口 API Key，若不设置则无法自动生成 Key 与自动翻译导出结果。申请方法见[百度翻译文档](http://api.fanyi.baidu.com/product/113)
- `front-i18n.i18nFunctionName`: 插入到代码的 i18n 函数名，默认为 `$t`。
- `front-i18n.autoTranslateResult`: 是否自动翻译导出结果，默认为 `false`。
- `front-i18n.exportLanguageExcel`：是否导出翻译结果 Excel，默认为 `false`。
- `front-i18n.languages`: 导出的语言列表，支援的语言列表见[百度翻译文档](http://api.fanyi.baidu.com/product/113)。默认为 `['en']`。

## ⚙️ 调试

若有更新维护，需要调试代码，可以按照以下步骤进行：

1. 安装依赖：`npm install`
2. 终端执行 `npm run dev`
3. 按下 `F5` 即可调试。

extension 的代码可以直接下断点调试。

Webview 代码则在启动的 `扩展开发宿主` 按下 `Ctrl + Shift + I` 启动开发者工具调试。

启动开发者工具后，可按下 `Ctrl + Shift + C` 选择要调试的 Webview。然后切换到 `Console` 选项卡，查看 Webview 的 id：
![1709711786527](assets/others/1709711786527.jpg)

然后切换到 `Source` 选项卡。在左侧的文件列表中该 id 目录，展开找到 `localhost:5173` 即可对 Webview 代码下断点调试。
![1709711923903](assets/others/1709711923903.jpg)
![](assets/others/20241230-190745.jpeg)
![](assets/others/20241230-190751.jpeg)
## 📄 Release Notes

### 0.0.1

- 初版发布。
