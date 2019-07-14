## vue-ace-edit

### 基于ace edit的在线代码编辑器，内置 xcode,one_dark主题，beautifier格式化插件

### 使用

暂时没有上传npm，可以下载js到项目中

```node
import { VueAceEdit } from './vue-ace-edit.umd.min.js'
Vue.component('v-ace-edit', VueAceEdit)
```
也可以浏览器中直接加载使用

```html
<script src="../dist/vue-ace-edit.umd.min.js"></script>

 <v-code-edit v-model="code"> </v-code-edit>

```
[在线demo ](https://websky219.github.io/vue-ace-edit/demo/ "demo")


### props

| 属性 | 类型   | 默认值 | 描述 |
| ----- | --------- | ----------- | ------- |
| value | String |  | 编辑器默认值 绑定 v-model|
| meun | Boolean | true | 是否显示顶上菜单 |
| setting  | Boolean |true| 是否显示主题设置 |
| format-btn | Boolean | true| 是否显示格式化按钮 |
| base-path  | String     | https://cdn.jsdelivr.net/npm/ace-builds@1.4.5/src-min-noconflict|ace资源位置，内置了js的资源，如果选择了其他语言需要从cdn库加载
| theme | String | one_dark | 主题风格，内置one_dark,xcode |
| mode  | String | javascript| 语言模式 |
| max-lines | [String,Number] | 80 | 最大行数，超过会自动出现滚动条 |
| min-lines  | [String,Number]     | 30 | 最小行数，还未到最大行数时，编辑器会自动伸缩大小|
| font-size | [String,Number] | 18  | 字体大小 |
| wrap  | String | free  | 自动换行 |
| indent-size | String| 2 | 格式化缩进2空格 |
| show-print-margin  | showPrintMargin | true | 是否显示代码标尺(中间竖线) |
| use-worker  | Boolean | true | 使用worker,语法检查使用的 |

### 事件

| 事件名 | 参数 | 说明|
| ----- | --------- | ----------- |
| init | edit对象 | 初始化事件 |
