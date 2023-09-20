# 冥冥meichan的 vup 歌单页

## 部署使用

### 制作歌单内容

**进行此步骤之前请先确保拥有 python 环境并安装依赖**

1. 按照模板 `scrips/example.xlsx` 填写，制作歌单内容
2. 运行 `python3 scripts/converter.py` 生成歌单文件

### 修改配置文件

1. 重命名 `config/constants.example.js` 为 `config/constants.js`
2. 修改其中内容 (以下为示例)

```js
let config = {
  Name: "", // 主页名字

  BiliLiveRoomID: "", // 直播间id

  NetEaseMusicId: "", // 网易云音乐id
  QQMusicId: "", // QQ音乐id
  Footer: "", //Copyright内容

  Cursor: true, // 使用自定义光标图片

  LanguageCategories: ["", "", ""], // 语言分类
  RemarkCategories: ["", ""], // 标签分类

  BannerTitle: "", // banner 标题

  BannerContent: [
    ``, // banner 内容
  ],

  // 自定义按钮 （可以复制生成更多）
  CustomButtons: [
    {
      link: "https:<any link you like>",
      name: "提问箱",
      image: ".png",
    },
    {
      link: "https://space.bilibili.com/<uid>",
      name: "录播组",
      image: "",
    },
  ],
};
```

### 启动开发环境

```bash
npm install
npm run dev
```

### 导出静态网站

```bash
npm run build
npm run export
# or
npm run buildssg
```

Next.JS 自动生成的"out"文件夹可直接用于部署静态网页

## 配置相关

### 鼠标指针

如果需要更改鼠标指针，可以在 config 中更改，默认为 `false`，如果需要请更改为 `true`，并且更改 styles 中的相关样式
并且将鼠标指针图片放入 `./assets/cursor/` 目录下

### Follow the MIT License