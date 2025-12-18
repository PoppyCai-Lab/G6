# 图可视化工具 - Graph Visualization

一个基于 Next.js 和 AntV G6 的现代图数据可视化工具，用于展示和分析复杂的关系网络。

## ✨ 特性

- 🎨 **现代简约设计** - 扁平化的 UI，柔和的配色，专业的视觉效果
- 🔍 **高级交互** - 拖拽节点、缩放画布、搜索、筛选、高亮路径
- 📊 **数据上传** - 支持 JSON 和 CSV 格式的自定义数据导入
- ⚡ **高性能渲染** - 基于 AntV G6 图可视化引擎
- 📱 **响应式布局** - 完美适配桌面和移动设备
- 🎯 **状态管理** - 使用 Zustand 进行高效的状态管理

## 🚀 快速开始

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

打开浏览器访问 [http://localhost:3000](http://localhost:3000)

### 构建生产版本

```bash
npm run build
npm start
```

## 📁 项目结构

```
graph-viz/
├── app/                    # Next.js App Router
│   ├── page.tsx           # 主页面
│   ├── layout.tsx         # 布局
│   └── globals.css        # 全局样式
├── components/            # React 组件
│   ├── GraphCanvas.tsx    # G6 图渲染组件
│   ├── ControlPanel.tsx   # 控制面板
│   ├── NodeDetails.tsx    # 节点详情
│   └── DataUploader.tsx   # 数据上传
├── lib/                   # 核心逻辑
│   ├── types.ts          # TypeScript 类型定义
│   ├── graph/            # G6 配置
│   └── store/            # Zustand 状态管理
└── data/                  # 数据相关
    └── mockData.ts       # 假数据生成器
```

## 🎯 功能说明

### 1. 图可视化

- **力导向布局** - 自动计算最优节点位置
- **节点拖拽** - 可以自由移动节点
- **画布缩放** - 滚轮缩放，支持平移
- **节点点击** - 点击查看详细信息

### 2. 控制面板

- **搜索** - 按产品名称或品牌搜索
- **品牌筛选** - 多选品牌过滤
- **价格区间** - 自定义价格范围
- **颜色筛选** - 按颜色分类筛选
- **重置过滤** - 一键恢复默认状态

### 3. 节点详情

- **基本信息** - 显示产品的品牌、价格、颜色
- **关联产品** - 展示所有相关联的节点
- **高亮路径** - 可视化节点之间的关系
- **快速跳转** - 点击关联产品快速查看

### 4. 数据上传

支持两种数据格式：

**JSON 格式：**
```json
{
  "nodes": [
    {
      "id": "p1",
      "label": "iPhone 15",
      "brand": "Apple",
      "price": 5999,
      "color": "Black"
    }
  ],
  "edges": [
    {
      "source": "p1",
      "target": "p2"
    }
  ]
}
```

**CSV 格式：**
```csv
id,label,brand,price,color,relatedTo
p1,iPhone 15,Apple,5999,Black,p2;p3
p2,Galaxy S24,Samsung,5499,White,p1
```

## 🛠 技术栈

- **框架**: Next.js 15
- **可视化**: AntV G6 5.0
- **状态管理**: Zustand
- **样式**: Tailwind CSS
- **语言**: TypeScript
- **文件上传**: react-dropzone

## 📝 开发计划

- [ ] 更多布局算法（树形、圆形、网格）
- [ ] 图编辑模式（添加/删除节点）
- [ ] 导出图片功能
- [ ] 连接数据库
- [ ] 实时协作

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！
