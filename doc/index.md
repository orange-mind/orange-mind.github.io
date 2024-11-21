# 10分钟掌握OrangeMind，给web加点魔法

为了高效使用Web页面，减少上下文切换和等待，我花了3年时间，开发了一款Chrome扩展：OrangeMind。

OrangeMind包含快捷指令、Web编辑器、页面脚本和代码片段共四大功能。

### 一、快捷指令

OrangeMind以快捷指令驱动网页，内置 25 种常用指令，每种快捷指令支持以普通按键或快捷键触发，快捷指令又可以根据需要自行定义。以下是一些常用的快捷指令：

#### 打开链接

OrangeMind支持打开任意网页或Chrome原生页面，如下所示：

<img src="https://orange-mind.github.io/doc/1.gif" style="zoom:80%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/1.png" style="zoom: 40%;" />

除了打开普通网页外，OrangeMind还支持打开带有前缀的网页，`[fixed]`前缀表示固定标签页，`[single]`前缀表示当前链接仅打开一个，`[fixed:single]`前缀表示双重效果，如下所示：

<img src="https://orange-mind.github.io/doc/2.gif" style="zoom:80%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/2.png" style="zoom:40%;" />

#### 复制文本

同样，复制文本也是非常基础的功能，如下所示：

<img src="https://orange-mind.github.io/doc/3.gif" style="zoom:80%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/3.png" style="zoom:40%;" />

#### 加载iframe页面

浏览网页时如果需要即刻查看另一个网页的内容，可以通过iframe来加载其他网页，从而避免思路跳出当前上下文，如下所示：

<img src="https://orange-mind.github.io/doc/5.gif" style="zoom:80%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/5.png" style="zoom:40%;" />

以上配置上，`80%x80%` 表示iframe弹框的宽高分别占当前页面宽高的 `80%`。

#### 打开Web编辑器

除了常规操作，浏览网页时还可以随时记录想法或执行一段代码，如下所示：

<img src="https://orange-mind.github.io/doc/6.gif" style="zoom:68%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/6.png" style="zoom:40%;" />

OrangeMind Web编辑器功能比较强大，有很多内置功能，后面会一一介绍。

#### 编辑页面样式或页面脚本

OrangeMind默认提供了页面样式的编辑功能，可以添加一段`CSS`，用来移除网页广告，搭配OrangeMindHelper扩展后，还可以进一步加载页面脚本，从而定制网页，如下所示：

<img src="https://orange-mind.github.io/doc/7.gif" style="zoom:67%;" />

如上所示，除`CSS`外，OrangeMind还能注入`html`结构、执行`js`脚本、以及运行`vue`代码。

该指令的配置如下所示：

<img src="https://orange-mind.github.io/doc/7.png" style="zoom:40%;" />

页面脚本是OrangeMind核心功能之一，后面会继续介绍。

#### 自定义二维码

二维码是浏览网页的刚需，快速生成二维码或解析二维码文本必不可少，如下所示：

<img src="https://orange-mind.github.io/doc/8.gif" style="zoom:67%;" />

如上所示，OrangeMind支持为生成的二维码动态添加logo和提示文本，将二维码图片粘贴至输入框时还会解析二维码图片为文本内容，解析失败后输入框中会有提示。

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/8.png" style="width:500px" />

二维码指令自身配置较多，支持宽高、前景色、背景色、内容、logo（可以添加多个自定义logo）、logo透明度、logo宽高、提示文本、提示字体大小、行高、行数和字体颜色等，同时还支持快速导出为jpg、png、base64、svg共4种格式，实际配置如下所示：

<img src="https://orange-mind.github.io/doc/8-1.png" style="width:500px" />

除此之外，二维码指令为方便操作，还支持了快捷复制（`Ctrl+C`）、快捷保存(`Ctrl+S`)、放大缩小(`Ctrl+=`、`Ctrl+-`)功能（Mac下对应按键前缀为`⌘`），为了进一步提升二维码配置的效率，上述配置弹框还支持取色器，取色器中支持拾取透明颜色，如下所示：

<img src="https://orange-mind.github.io/doc/8-2.png" style="zoom:40%;" />

#### 显示页面源代码

浏览器默认的`显示网页源代码`功能，仅支持展示页面源码，不支持代码格式和进一步操作，为了更好的浏览页面源码，OrangeMind提供了快速查看页面源码的指令，如下所示：

<img src="https://orange-mind.github.io/doc/9.gif" style="zoom:67%;" />

格式化的源码还可以进一步编辑，或执行编辑器的各种快捷操作。

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/9.png" style="zoom:40%;" />

#### 页面取色

浏览到精美的页面，可以一键取色，获取色值并复制到剪贴板，如下所示：

<img src="https://orange-mind.github.io/doc/10.gif" style="zoom:67%;" />

不仅如此，取色功能还可以脱离浏览器，支持在屏幕任意位置取色，启用取色指令后，浏览器将秒变取色器。

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/10.png" style="zoom:40%;" />

#### 编辑页面

浏览网页时，如果需要修改网页内容进行截图，或绕过网页的禁止复制限制，开启网页的编辑模式即可，如下所示：

<img src="https://orange-mind.github.io/doc/11.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/11.png" style="zoom:40%;" />

#### 页面截图

系统截图想必大家都比较熟悉，但如何快速截取屏幕可视区域内的所有网页内容，就稍显麻烦，需要多次拖动并调整选区才能截取到合适的页面截图，那么有没有更为快速的方式，一键截图呢，如下所示：

<img src="https://orange-mind.github.io/doc/12.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/12.png" style="zoom:40%;" />

如上所示，按下 `⌘+P` 键（windows下为`Ctrl+P`键），即可获取当前页面截图，此时拖动选区并按下回车键，指定区域截图将保存至剪切板。

如果不拖动选区立即按下回车键，当前页面截图将保存至剪切板，如下所示：

<img src="https://orange-mind.github.io/doc/12-1.gif" style="zoom:67%;" />

如果截图时，需要保持输入框高亮，或者鼠标悬停的各种临时状态，也可以配置截图的延迟秒数，如配置延迟`2`s，则意味着2s后页面将自动截图，如下所示：

<img src="https://orange-mind.github.io/doc/12-2.gif" style="zoom:67%;" />

#### 完整页面截图

有些网页可能内容较多，一页展示不下，这样截图时就不能截取完整页面，OrangeMind考虑到这种场景，支持了完整页面截图，如下所示：

<img src="https://orange-mind.github.io/doc/14.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/14.png" style="zoom:40%;" />

#### 下载页面截屏

小于2M的页面截图，默认会复制到剪切板，1分钟内执行指令可以保存截图到本地，如下所示：

<img src="https://orange-mind.github.io/doc/13.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/13.png" style="zoom:40%;" />

#### 获取标签页详情

执行如下指令，可以快速获取当前标签页信息，如下所示：

<img src="https://orange-mind.github.io/doc/15.gif" style="zoom:67%;" />

该指令配置如下：

<img src="https://orange-mind.github.io/doc/15.png" style="zoom:40%;" />

#### 调整浏览器窗口大小

无论是截图还是响应式开发测试需要，调整浏览器窗口都是常规操作，如下所示：

<img src="https://orange-mind.github.io/doc/16.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/16.png" style="zoom:40%;" />

如上所示，浏览器窗口大小的配置为`宽度x高度`。

#### 窗口平铺和合并

除了调整浏览器窗口大小，浏览器的各个标签页也支持快速平铺展示和合并，如下所示：

<img src="https://orange-mind.github.io/doc/17.gif" style="zoom: 50%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/17.png" style="zoom:40%;" />

#### 获取页面加载性能

对于前端开发而言，关注并查看网页的加载性能，几乎是下意识行为，OrangeMind也提供了对应的指令，如下所示：

<img src="https://orange-mind.github.io/doc/19.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/19.png" style="zoom:40%;" />

#### PDF操作

除了页面截图外，OrangeMind还支持将多张图片合成为PDF，PDF操作涉及到三个快捷指令，操作流程如下所示：

<img src="https://orange-mind.github.io/doc/20.gif" style="zoom:67%;" />

保存的pdf如下所示：

<img src="https://orange-mind.github.io/doc/20.png" style="zoom: 40%;" />

以上操作涉及3个指令，配置如下所示：

<img src="https://orange-mind.github.io/doc/20-1.png" style="zoom:40%;" />

- `指令1`表示开始录制pdf，该指令为前置指令（意味着后续有指令依赖它）

- `指令2`表示添加pdf页面，该指令依赖前置`指令1`，且该指令不刷新指令记录

- `指令3`表示保存pdf到本地，该指令同样依赖前置`指令1`，由于`指令2`不刷新指令记录，所以当`指令3`执行时，前一个指令依然是`指令1`

上述PDF操作中，只是简单应用了前置指令，实际上，通过配置前置指令的方式，可以批量启用多个快捷键（比如说，按下 `vim` 快捷指令，可以一键启动页面的vim模式，当然这种需要一些编码，后续版本可能会支持）。

#### 加载内容弹框

工作中经常会遇到碎片化的信息需要记录，如果通过笔记软件录入，再次查看时一般需要经过这样几步：“唤起笔记软件—等待笔记软件加载完成—切换到对应笔记—关闭笔记软件”，现在只需要通过几次按键就行，能有效减少等待和上下文切换，工作思路更聚焦，如下所示：

<img src="https://orange-mind.github.io/doc/23.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/23.png" style="zoom:40%;" />

以上是`Markdown`格式的文档，OrangeMind还支持通过`HTML` 来配置文档内容，如下所示：

<img src="https://orange-mind.github.io/doc/24.gif" style="zoom:67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/24.png" style="zoom:40%;" />

#### 添加右键菜单

在OrangeMind的其他配置中，可以动态添加浏览器右键菜单，如下所示：

<img src="https://orange-mind.github.io/doc/25.png" style="zoom: 40%;" />

除此之外，快捷指令也支持快速添加右键菜单，如下所示：

<img src="https://orange-mind.github.io/doc/25.gif" style="zoom: 67%;" />

该指令配置如下所示：

<img src="https://orange-mind.github.io/doc/25-1.png" style="zoom: 40%;" />

### 二、Web编辑器

为了方便随时编写和修改代码，OrangeMind提供了功能强大的Web编辑器，编辑器主要包含以下功能：

1. 提供类似于VSCode的编辑体验，支持minimap
2. 支持81种代码语言，提供53种主题皮肤
3. 支持多标签页
4. 支持vim模式
5. js代码支持立即执行
6. 丰富的快捷功能：代码预览、格式化、编译AST、加密混淆，压缩编译、获取Hash、大小写切换等等

Web编辑器实际体验如下所示：

<img src="https://orange-mind.github.io/doc/editor.gif" style="zoom: 67%;" />

#### 多标签页

Web编辑器支持新增任意个标签页，可以同时编写多个代码文件，常见的一些代码语言也支持了icon高亮，为了方便操作，编辑器支持以下快捷键：

- 新建标签页（`Alt+N`）
- 标签页名称获取焦点后，`双击` 鼠标或按 `Enter` 键支持修改当前标签页名称，按`Esc`键可以取消编辑中的标签名

#### Vim模式

打开Web编辑器的设置面板，可以启用Vim模式，如下所示：

<img src="https://orange-mind.github.io/doc/vim.gif" style="zoom:67%;" />

#### js代码立即执行

> 由于V3版本Chrome扩展审核的原因，执行动态JS代码需要安装`OrangeMindHelper`辅助扩展。

安装辅助扩展后，Web编辑器就支持在当前页面动态执行JS代码，这样可以就在编辑器中进行页面局部功能的开发调试，如下所示：

<img src="https://orange-mind.github.io/doc/run.gif" style="zoom:60%;" />

#### 编译AST

为了更好的关注代码的语法结构，Web编辑器提供了编译AST功能，如下所示：

<img src="https://orange-mind.github.io/doc/ast.gif" style="zoom: 67%;" />

#### 加密混淆

代码混淆可以在一定程度上隐藏页面代码逻辑，提升业务安全性，具体效果如下所示：

<img src="https://orange-mind.github.io/doc/hunxiao.gif" style="zoom:67%;" />

#### 代码压缩编译

一般前端项目都会编译上线，那么对于单个文件，有没有办法快速压缩呢，如下所示：

<img src="https://orange-mind.github.io/doc/compress.gif" style="zoom: 67%;" />

#### 获取hash

前后端联调时，有时需要hash一段文本，然后上传到后台进行匹配，那么如何获取hash呢，如下所示：

<img src="https://orange-mind.github.io/doc/hash.gif" style="zoom:67%;" />

#### 快速大小写

快速大小写如下所示：

<img src="https://orange-mind.github.io/doc/upCase.gif" style="zoom:67%;" />

### 三、页面脚本

页面脚本是OrangeMind的核心功能之一，它可以去广告、去水印，聚合展示页面数据，增强页面功能等等，只要能通过JS实现的功能，它都可以做到。（由于V3版本的Chrome扩展不支持动态执行脚本，该功能需要搭配OrangeMindHelper使用，请先安装[OrangeMindHelper]()扩展）

页面脚本配置面板如下所示：

<img src="https://orange-mind.github.io/doc/code.png" style="zoom: 33%;" />

<img src="https://orange-mind.github.io/doc/code-1.png" style="zoom: 33%;" />

单个页面脚本支持配置以下属性：

|     key     |      类型      |                          说明                           |
| :---------: | :------------: | :-----------------------------------------------------: |
|    name     |     String     |                      页面脚本名称                       |
|   version   |     String     |                         版本号                          |
| description |     String     |                   页面脚本描述或说明                    |
|   author    |     String     |                          作者                           |
|    match    | Array\<String> | 页面脚本在哪些页面生效，可以配置多个url，url支持*通配符 |
|    icon     |     String     |                      页面脚本icon                       |

除config面板外，其他几个配置面板分别是html、js、css、vue，这意味着可以同时注入html结构、js代码、css样式和vue代码（未安装OrangeMindHelper扩展时仅支持注入css）。

注入html如下所示：

<img src="https://orange-mind.github.io/doc/code-html.png" style="zoom: 33%;" />

效果如下所示：

<img src="https://orange-mind.github.io/doc/code-html-1.png" style="zoom: 33%;" />

注入js过程及效果如下所示：

<img src="https://orange-mind.github.io/doc/code-js.gif" style="zoom: 67%;" />

为了更加方便的编写页面脚本，OrangeMind内置了`runtimeId`、`actionId`和`orangeMind`对象，点击js面板右上角的第二个按钮（`问号？`按钮），可以查看帮助文档：

<img src="https://orange-mind.github.io/doc/code-js-1.png" style="zoom: 33%;" />

`orangeMind`对象支持以下方法：

|  #   |    方法名     |                            参数                            |                             描述                             |
| :--: | :-----------: | :--------------------------------------------------------: | :----------------------------------------------------------: |
|  1   |     ready     |                          callback                          |                       页面ready后执行                        |
|  2   |    request    | { url, method, data, headers, onload, onerror, ontimeout } |                    请求方法，支持跨域请求                    |
|  3   |  formatTime   |                         timestamp                          |           格式化时间戳为“yyyy-MM-dd HH:mm:ss”格式            |
|  4   |  formatDate   |                         timestamp                          |                  格式化时间戳为“yyyy-MM-dd”                  |
|  5   |   getQrCode   |                          options                           |                          获取二维码                          |
|  6   |   getCache    |                          actionId                          |         获取指定页面脚本的缓存，actionId也会自动注入         |
|  7   |   setCache    |                      actionId, value                       |                    设置指定页面脚本的缓存                    |
|  8   |  clearCache   |                          actionId                          |                    清除指定页面脚本的缓存                    |
|  9   |   showToast   |                          options                           |                          显示toast                           |
|  10  |  loadScript   |                            url                             |                     加载js，返回promise                      |
|  11  |    loadCss    |                            url                             |                       加载css样式资源                        |
|  12  |   loadStyle   |                        styleContent                        |                         加载css样式                          |
|  13  |   loadFrame   |                      runtimeId, links                      | 同时加载4个iframe页面，支持拖拽调整各个页面的大小，links数组的每项为[src, title] |
|  14  |      get      |                            key                             | 获取window指定key的value，若key不存在，则监听该key的绑定，可用于获取不确定赋值时机的全局变量 |
|  15  |   addButton   |                       name, onClick                        |                           添加按钮                           |
|  16  |     copy      |                            text                            |                           复制文本                           |
|  17  |     open      |                            url                             |                          打开H5链接                          |
|  18  |     sleep     |                             ms                             |                  休息一定时间，单位（毫秒）                  |
|  19  |    console    |                             -                              |          输出日志，可以在页面禁用console后打印日志           |
|  20  | setInputValue |                           value                            |                        设置输入框的值                        |
|  21  |   keepScope   |                             -                              | 若页面脚本绑定的点击事件不生效，或异步逻辑不执行，可执行该方法保留作用域 |

基于以上`orangeMind`对象提供的各种API，我们可以很容易实现打开链接、发送跨域请求、获取二维码、复制内容、设置输入值、添加按钮、设置和读取页面脚本缓存数据、加载各种资源等常见功能需求。

注入css如下所示：

<img src="https://orange-mind.github.io/doc/code-css.png" style="zoom: 33%;" />

效果如下所示：

<img src="https://orange-mind.github.io/doc/code-css-1.png" style="zoom: 33%;" />

除了基础的html、js、css代码外，为了快速注入功能模块，OrangeMind还特别支持了vue代码注入，如下所示：

<img src="https://orange-mind.github.io/doc/code-vue.gif" style="zoom: 67%;" />

如上所示，vue面板中键入 `template-vue` 可以快速创建vue模版。

### 四、代码片段

一直以来，如何低成本的管理和唤起代码片段是个难题，为此OrangeMind提供了便捷的代码片段功能，该配置面板所示：

<img src="https://orange-mind.github.io/doc/fragment.png" style="zoom:33%;" />

点击编辑按钮，打开代码片段编辑弹框如下所示：

<img src="https://orange-mind.github.io/doc/fragment-1.png" style="zoom:33%;" />

- 语言：表示在当前代码语言下会出现输入提示
- 关键词：表示输入触发提示的词语
- 输入说明：表示输入提示的说明
- 代码片段：表示选中该条代码片段提示时，实际插入的代码

代码片段如何唤起，如下所示：

<img src="https://orange-mind.github.io/doc/fragment.gif" style="zoom: 67%;" />

为了方便随时添加代码片段，Web编辑器中支持将选中文本快速添加为代码片段，如下所示：

<img src="https://orange-mind.github.io/doc/fragment-1.gif" style="zoom:67%;" />

为了进一步简化代码片段唤起路径，后续快捷指令将会支持代码片段的一键查询。

#### 规划

除了上述这些功能外，OrangeMind还有更多强大功能正在快速开发调试中，敬请期待~。同时使用过程中有啥问题和建议，欢迎在评论区或 [github](https://github.com/orange-mind/orange-mind.github.io/issues) 留言，好的想法或需求也会加入后续迭代计划。











