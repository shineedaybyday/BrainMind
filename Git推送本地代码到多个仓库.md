# Git推送本地代码到多个仓库
- 首先如下所示添加第一个仓库：

```git
	git remote add $(lib_mask) $(gitlib_url)
```
*其中\$(lib_mask)表示远程仓库地址的在你本地计算机上的简称，\$(gitlib_url)代表远程仓库地址*

- 使用如下命令添加第二个仓库url

```git
	git remote set-url --add $(lib_mask) $(gitlib_url2)
```
*其中\$(lib_mask)与你初次新建的库代号是一样的*

- 添加第三第四个库同上
- 最后使用如下命令提交

```git
	git push $(lib_mask) --all
```
*其中\$(lib_mask)于初次新建的库代号是一样的*