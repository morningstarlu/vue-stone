# MEMO

## Notice

- Dayspicker 中请用 v-model 代替 days。 days 属性将在下个正式版本中不可用。

- Range 组件中采用下划线式命名的属性将在下个大版本中不支持。

- Button 新增 syncHold 属性，值为 true 时会忽略 hold 属性，作用和 hold 属性类似，但不具备 hold 属性改变一次状态前只会触发一次 change 事件的特性。

## Todo

* [ ] To finish those docs of components, refer the format of [format-of-docs](https://github.com/JD-Smart-FE/vue-stone/blob/master/wiki/format-of-docs.md)

* [x] The option v-model will be unnecessary
  * [x] In Action-box

* [ ] 有些组件依赖与个别icon，如 checkboard 选中状态下的小对勾。应当把这些组件必须的 icon 和 非必需 icon 分别对待。
  * [x] checkborad
  * [ ] Loading

* [ ] Vue 2.2 以上要求 for 循环需要添加 key 属性，因此需要为组件库里用到 for 循环的组件添加 key.

* [ ] 进一步完善 README，添加按需引入组件的说明。

* [ ] 所有组件暴露出的接口应风格一致。为符合 HTML5 书写习惯，组件中的 props 请用驼峰式命名，vue 会将其在组件外暴露为端横连接的方式。以下几个组件的 props 采取了下划线作为链接符，需在下个大版本中统一为驼峰式（为兼容现有项目，组件属性请采取无痛的过渡方案，暨不删除现有下划线式的属性，另外在支持驼峰式的属性）
  * [ ] Range

* [ ] 事件及方法名称尽可能的统一，比如说组件状态发生改变尽可能的统一使用 `change` 作为事件名。

## Thinking

* [ ] 字体图标的引用。 默认状态下所有的字体图标会被打包进组件库的样式文件，这会导致样式文件大小成倍的增加，因此很有必要分离出字体图标样式文件。分离出来后目前能想到两种引用的方式。
  1. 像按需引用组件一样，将字体图标作为一个单独的组件对待。
  2. 单独让用户 require 样式文件，如 `require(vue-stone/dist/iconfonts.css)`。
  3. 或者是均支持。