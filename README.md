# three-plane-overlap · 三图平行堆叠 3D 对照查看器

三张图片平行堆叠在 3D 场景中（默认等距视角），自由旋转视角查看三张图的重叠关系。
每个面由两层组成：「衬底面」与「图片内容」，二者透明度独立可调——把「面」调到 0 可只看图片内容本身。

## 在线体验

GitHub Pages：<https://dreamrain314.github.io/three-plane-overlap/>

## 功能

- 拖动旋转 / 滚轮缩放 / 右键平移；触屏单指旋转、双指缩放
- 层间距可调，「重置视角」一键回到等距默认位
- 每层可单独换图、调「面 / 图」透明度、显示或隐藏

## 本地运行

three.js（MIT）已内置于 `vendor/`，无需外网 CDN。内置图片放在 `images/` 下，命名为 `a`、`b`、`c`（png / jpg / webp 均可，程序自动尝试扩展名）。
当前图层对应：最上层 = `images/a`（图1 石峰），中间层 = `images/b`（图2 纸片碎片），最底层 = `images/c`（图3 雾山底景）。
用任意静态服务器打开即可，例如：

```bash
python -m http.server 8090
# 浏览器访问 http://localhost:8090
```

> 直接双击 index.html（file:// 协议）时浏览器会阻止内置图片载入 WebGL，此时显示程序内置的占位示例图；通过 HTTP 访问或 GitHub Pages 则正常。
