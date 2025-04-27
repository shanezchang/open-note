# Git

## Git 免密码配置

初次配置 git 的 name 和 email，例如：

```sh
git config --global user.name "user"
git config --global user.email "user@email.com"
```

配置密码记录

```bash
# 如果是 Mac 或 Windows 系统，可以通过执行这行命令配置密码记录
git config --global credential.helper manager

# 如果是 Linux 系统，无法设置永久记录，可以设置过期时间自定义为一年
# 3600*24*30*12 = 31,104,000
git config --global credential.helper 'cache --timeout=31104000'
```

## 如果某一个代码工程需要另一个git账户

可以执行如下命令

```bash
# 清空当前项目
git config --local --unset credential.helper

# 查看配置是否清空
git config --list

# 配置新的属于此工程的git代码账户
git config --local user.name "user"
git config --local user.email "user@email.com"

# 查看配置是否成功
git config --list
```



## commit Angular 提交规范

1. `build`：对构建系统或者外部依赖项进行了修改
2. `ci`：对 CI 配置文件或脚本进行了修改
3. `docs`：对文档进行了修改
4. `feat`：增加新的特征
5. `fix`：修复`bug`
6. `pref`：提高性能的代码更改
7. `refactor`：既不是修复`bug`也不是添加特征的代码重构
8. `style`：不影响代码含义的修改，比如空格、格式化、缺失的分号等
9. `test`：增加确实的测试或者矫正已存在的测试



## Clone 设置 depth

工程比较大，只克隆最新的一个commit的代码工程，可以节省空间、并提高clone速度。

```bash
git clone --depth 1 https://github.com/labuladong/fucking-algorithm.git
```

## Git LFS

Git 大型文件扩展功能支持

https://git-lfs.com/

执行命令`./install.sh`，然后通过命令`git lfs install`检验是否安装成功。

## Git Commit 配置

本地已经执行 git add，git commit 之后，想要重新改变commit的内容，回退或者取消评论，并重新执行git add、git commit，可以使用下面的命令

```bash
# 先使用 git log 查看本地有几个是需要回退的commit
# 例如有两个commit要回退，则把最后的数字为2
git reset --mixed HEAD~2

# 然后就可以重新执行 git add，git commit 了。
```

