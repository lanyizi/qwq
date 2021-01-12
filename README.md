# qwq
一个非常简(jǐan)单(lòu)、基于[mirai-ts](https://github.com/YunYouJun/mirai-ts)的跨群转发消息机器人

这样的机器人到底有什么用呢，大概就是，可以把多个群，通过互相转发消息，“合并”成一个群吧 ←_←

它可以支持跨群回复，也就是，假如机器人转发消息过来，你回复机器人，机器人就会在另一个群里替你回复另一个人！
此外它还支持撤回，假如你撤回了自己的消息，那么机器人也将会尝试撤回它转发到其他群的消息。

## 使用方法
首先你需要拥有一个能够通过 HTTP API 访问的 Mirai 机器人
（比如说，一个启用了 [mirai-api-http](https://github.com/project-mirai/mirai-api-http) 插件的 [Mirai Console](https://github.com/mamoe/mirai-console)）
接下来需要编译 index.ts，可以通过 `tsc` 命令来执行（需要先安装 typescript 编译器）
然后执行 `node index.js -c 配置文件.json` 即可。
配置文件的格式可以参考这里：https://github.com/BSG-75/qwq/blob/main/index.ts#L28
- `mahConfig` 指的是与 mirai-api-http 有关的配置，具体内容可以参考[这里](https://github.com/YunYouJun/mirai-ts#javascript)

开始运行之后，它就会自动在各个群里互相转发消息了
