## 2.1.6（2023-04-16）
* 修复 组件使用 v-show 指令会导致选择图片后初始位置严重偏位的问题

## 2.1.5（2023-04-16）
* 新增 兼容APP平台

## 2.1.4（2023-03-13）
* 新增 fileType 属性，用于指定生成文件的类型，只支持 'jpg' 或 'png'，默认为 'png'
* 新增 delay 属性，微信小程序平台使用 `Canvas 2D` 绘制时控制图片从绘制到生成所需时间
* 优化 当生成图片的尺寸宽/高超过 Canvas 2D 最大限制（1365*1365）则将画布尺寸缩放在限制范围内绘制完成后输出目标尺寸
* 优化 旋转图标指示方向与实际旋转方向不符

## 2.1.3（2023-02-06）
* 优化 vue3支持

## 2.1.2（2023-02-03）
* 新增 navigation 属性，H5平台当 showAngle 为 true 时，使用插件的页面在 `page.json` 中配置了 "navigationStyle": "custom" 时，必须将此值设为 false ，否则四个可拉伸角的触发位置会有偏差
* 修复 H5平台部分设备（已知iPhone11以下机型）拍照的图片缩放时会闪动的问题

## 2.1.1（2022-12-06）
* 修复 横屏适配问题

## 2.1.0（2022-12-06）
* 新增 兼容H5平台，使用 renderjs 响应手势事件

## 2.0.0（2022-12-05）
* 重构 插件，使用 WXS 响应手势事件
* 新增 图片翻转
* 新增 拉伸裁剪框放大图片
* 新增 监听PC鼠标滚轮触发缩放
* 新增 圆形、圆角矩形的图片裁剪
* 优化 图片缩放，移动端以双指触摸中心点为缩放中心点，PC端以鼠标所在点为缩放中心点
* 优化 裁剪框样式
* 优化 图片位置拖动 支持边界回弹效果（滑动时可滑出边界，释放时回弹到边界）
* 优化 生成图片使用新版 Canvas 2D 接口
