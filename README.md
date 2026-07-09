# 海洋学院学习小窝

这是海洋学院的学习小窝，收集了一些海院的课程资料。

你可以在 https://zjuocer.github.io/zjuoc-courses/ 看到对应的页面。

## 如何参与编写：

### 如果你愿意提供资料

可以通过以下几种方式联系我们：

- 发邮件至
- 通过钉钉联系
- 在本仓库提交 issue

### 如果你是仓库的维护者

1. 在电脑上安装 Git 和 Python （其中 Python 建议使用版本管理工具，比如 uv）。
2. 将本仓库 `clone` 到本地。
3. 根据对应的版本管理工具安装 Zensical，可参见 [Zensical 官网](https://zensical.org/docs/get-started/)。

    pip：
    ```shell
    python -m venv .venv  
    .venv\Scripts\activate
    pip install zensical
    ```

    uv:
    ```shell
    uv init
    uv add --dev zensical
    uv run zensical
    ```

4. 输入
    ```shell
    zensical serve
    ```

    或者

    ```shell
    uv run zensical serve
    ```

    等到出现提示 `Serving ... on http://localhost:8000` 时，即可在对应的网址打开本地预览。

5. 新建页面或者修改页面，新建页面后记得修改[zensical.toml](./zensical.toml)

6. 编辑完成后，执行

    ```shell
    git add .
    git commit -m "一句话描述本此次改动的内容"
    git push
    ```

7. 如果你有仓库的写入权限，这样应该就已经上传完成了。