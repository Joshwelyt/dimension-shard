# 代码结构

- `jsconfig.json`: 给 `VSCode` 用的，方便生成 `require` 和跳转
- `main.js`: 主入口，只做 `require` ，决定了内容顺序
- `abomb4/`: 自己封装的通用库，理论上给别的 mod 也能用
  - `abilities.js`: 单位能力，比如单位力场这种
  - `block-types.js`: 方块定义，定义一些常用方块
  - `hud.js`: 一个扩展右下角内容框的 UI ，暂未使用
  - `lib.js`: Utilities 工具方法
  - `multi-crafter.js`: 多合成表工厂库，暂未使用
  - `skill-framework.js`: 单位技能框架，如果有别的 mod 复制了，那么与本 mod 同时运行时肯定出问题
- `ds-common/`: 次元碎片 Mod 中的通用内容，包括非指定科技线的建筑、原版增强、物品定义、战役等
  - `bullet-types/`: 弹药类型，说不定会合并到 `abomb4/`
  - `ds-global.js`: 次元碎片 Mod 的公用方法，目前只有可建造判断
  - `items.js`: 物品与液体
  - `overrides.js`: 覆写原版内容的 js
  - `planets.js`: 星球
  - `research-tree.js`: 科技树，必须在 `main.js` 最后面引入，否则会打乱内容顺序
- `tech-ds/`: Dimension Shard, 次元碎片科技线内容，由 `main.js` 编排顺序
- `tech-solid/`: Solid Industry, 坚实工业科技线内容，由 `main.js` 编排顺序
- `tech-spore/`: Spore Erosion, 孢子侵蚀科技线内容，由 `main.js` 编排顺序