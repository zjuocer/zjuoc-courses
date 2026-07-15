# 海洋学院学习小窝

浙江大学海洋学院课程资料共建平台。

在线访问：<https://zjuocer.github.io/zjuoc-courses/>

## 这里收集什么

- 历年卷 / 回忆卷
- 课程笔记
- 课程评价
- 课程资料
- 飞跃手册与同学主页链接

每份资料都应保留贡献者署名，方便后来者知道资料来源，也记录每一位同学的贡献。

## 目录结构

```text
docs/
  index.md                    # 网站首页
  1-freshman/                 # 大一课程
  2-sophomore/                # 大二课程
  3-junior/                   # 大三课程
  4-senior/                   # 大四课程
  community/                  # 名人堂、个人主页
  flying-handbook/            # 飞跃手册
  stylesheets/extra.css       # 站点样式
zensical.toml                 # 网站导航与主题配置
```

## 课程页面规范

每门课建议设置以下四个分支：

1. 历年卷 / 回忆卷
2. 课程笔记
3. 课程评价
4. 课程资料

新增页面后，请同步修改 [zensical.toml](./zensical.toml)，把页面加入导航。

## 如何参与编写

如果你愿意提供资料，可以通过以下方式参与：

- 在本仓库提交 issue。
- 联系维护者上传资料。
- 直接提交 Pull Request。

## 维护者本地预览

1. 安装 Git 和 Python。Python 推荐配合 `uv` 使用。
2. 将本仓库 clone 到本地。
3. 安装并运行 Zensical：

```shell
uv run zensical serve
```

或：

```shell
zensical serve
```

看到 `Serving ... on http://localhost:8000` 后，即可打开本地预览。

## 上传修改

```shell
git pull
git add .
git commit -m "一句话描述本次改动"
git push
```

如果你有仓库写入权限，推送后 GitHub Pages 会自动更新网站。
