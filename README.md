# Personal homepage template

已选模板：Minimal Mistakes 4.28.1，`single` 页面布局，默认白色皮肤，左侧作者资料栏，英文。

## 先看效果

用浏览器打开 `preview/index.html`。这是用于确认版式的静态预览，可离线查看；它不是 Jekyll 的构建输出。预览采用原主题 CSS，已添加本人照片、姓名、邮箱、GitHub、Google Scholar、英文简介、教育背景、WONN 论文和 2025 年国家奖学金。Education 和 Selected Awards 使用交大官方校徽，图片来源见 `assets/images/SOURCES.md`。照片原文件保存在 `assets/images/jiawen-dai.jpg`，圆形显示由 CSS 完成。

## 后续修改入口

- `_config.yml`：姓名、头像、身份、简介和真实联系方式。
- `index.md`：主页正文。
- `_data/navigation.yml`：顶部导航。
- `assets/css/homepage.css`：预览和 Jekyll 共用的字号、布局与个人资料样式。
- `assets/images/`：照片和其他图片。
- `assets/icons/`：离线可用的资料图标与许可说明。
- `_sass/`、`_layouts/`、`_includes/`：保留自桌面原始主题压缩包的样式与组件。

静态预览是本次选版的快照，不会随 Markdown 自动更新。后续编辑应以 Jekyll 源文件为准，再重新构建预览。

## 构建 Jekyll 网站

需要兼容 Jekyll 4.4 的 Ruby 和 Bundler 环境。本机当前为系统 Ruby 2.6，未安装 Jekyll；本次没有更改系统 Ruby，也没有运行 Jekyll 构建。

在环境准备好后，于本目录运行：

```sh
bundle install
bundle exec jekyll serve
```

正式生成静态文件：

```sh
bundle exec jekyll build
```

构建结果位于 `_site/`。部署前需按最终域名设置 `_config.yml` 的 `url` 和 `baseurl`。

## 来源与许可

原始文件：桌面 `minimal-mistakes-master.zip`，主题版本 4.28.1。原始说明保存在 `THEME-README.md`，MIT 许可保存在 `LICENSE`。

静态预览 CSS 来自主题官方演示：https://mmistakes.github.io/minimal-mistakes/assets/css/main.css 。它只服务于预览，Jekyll 正式构建使用随包保留的 SCSS。

目前为本地模板，未注册或部署线上站点。
