# 移动端问题总结

## 通用

### 移动端 input输入密码的时候调用纯数字键

- 在 input 的style 标签中加入 ”-webkit-text-security:disc“ 属性
- <input type="tel" style="-webkit-text-security:disc">

## android

## ios

### Date 属性的兼容性

- 在 safari 和 ios 应用中对js的 Date对象的兼容性较差，不可以写成 Date 中的格式不可以写成 ”xxxx-xx-xx“， ios 只接受  ”xxxx/xx/xx“ 格式
- 解决方案

	- 在遇到这问题的时候，需要把 ”xxxx-xx-xx“ 转换成 ”xxxx/xx/xx“ 格式
	- ”xxxx-xx-xx“.replace(/\-/g,"/")

