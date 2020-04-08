# 使用方法

# 创建放置文档的仓库

在电脑中创建一个 Gitbook 文件夹，用于放置自己的 Gitbook 文件。

再在 Gitbook 文件夹中创建新的文件夹，以 bookname 命名。

# 初始化

到 bookname 文件夹中打开 powershell 窗口，执行`gitbook init`命令。

> 坑：在此系统禁止运行脚本
>
> 此处若失败并出现提示信息“因为在此系统禁止运行脚本”，需要以管理员身份打开power shell，输入`set-ExecutionPolicy RemoteSigned`，选择“是”。

# 编辑

接下来打开 Typora，文件 - 打开文件夹 - 选择 bookname 文件夹，编辑 SUMMARY.md 文件以修改大纲。

修改后，打开 power shell，输入 `gitbook init`，bookname 文件夹内就会生成对应的 md 文件。

# 预览

执行 `gitbook serve` 来预览这本书籍。

>坑：Error: ENOENT: no such file or directory
>
>用户目录下找到文件 .gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js，将所有的 confirm: true 语句改为 confirm: false

之后打开 [http://localhost:4000](http://localhost:4000/) 预览。

# 生成静态网站

执行 `gitbook build` 命令，默认将生成的静态网站输出到 _book 目录。

