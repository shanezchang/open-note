# Git



# Git Note

## Git 面密码push

```sh
git config --global user.name "shane"
git config --global user.email "shane.z.chang@gmail.com"

# 3600*24*30*12 = 31,104,000 
# Linux 下只能设置过期时间 此处设置为1年
git config --global credential.helper 'cache --timeout=31104000'


git config --global credential.helper manager

```



重置账号密码

```bash
git config --global credential.helper manager

git config --system --unset credential.helper

// 如果需要更大的范围
git config --global --unset credential.helper

# 清空当前项目
git config --local --unset credential.helper

git config

git config --local user.name "Garvin"
git config --local user.email "garvinzhang@foxmail.com"

git config --local user.name "shane"
git config --local user.email "shane.z.chang@gmail.com"

git config --global user.name "shane"
git config --global user.email "shane.z.chang@gmail.com"

git config --global user.name "Garvin"
git config --global user.email "garvinzhang@foxmail.com"

git config user.name shane
git config user.email shane.z.chang@gmail.com

git config --list
```

commit Angular 提交规范

1. `build`：对构建系统或者外部依赖项进行了修改
2. `ci`：对 CI 配置文件或脚本进行了修改
3. `docs`：对文档进行了修改
4. `feat`：增加新的特征
5. `fix`：修复`bug`
6. `pref`：提高性能的代码更改
7. `refactor`：既不是修复`bug`也不是添加特征的代码重构
8. `style`：不影响代码含义的修改，比如空格、格式化、缺失的分号等
9. `test`：增加确实的测试或者矫正已存在的测试

clone

设置 depth

```bash
git clone --depth 1 https://github.com/labuladong/fucking-algorithm.git

```

# Git Linux



## Git 免密码push

```sh
git config --global user.name "shane"
git config --global user.email "shane.z.chang@gmail.com"

# 3600*24*30*12 = 31,104,000 
# Linux 下只能设置过期时间 此处设置为1年
git config --global credential.helper 'cache --timeout=31104000'


git config --global credential.helper manager

```



重置账号密码

```bash
git config --global credential.helper manager

git config --system --unset credential.helper

// 如果需要更大的范围
git config --global --unset credential.helper

# 清空当前项目
git config --local --unset credential.helper

git config

git config --local user.name "Garvin"
git config --local user.email "garvinzhang@foxmail.com"

git config --local user.name "shane"
git config --local user.email "shane.z.chang@gmail.com"

git config --global user.name "shane"
git config --global user.email "shane.z.chang@gmail.com"

git config --global user.name "Garvin"
git config --global user.email "garvinzhang@foxmail.com"

git config user.name shane
git config user.email shane.z.chang@gmail.com

git config --list
```

commit Angular 提交规范

1. `build`：对构建系统或者外部依赖项进行了修改
2. `ci`：对 CI 配置文件或脚本进行了修改
3. `docs`：对文档进行了修改
4. `feat`：增加新的特征
5. `fix`：修复`bug`
6. `pref`：提高性能的代码更改
7. `refactor`：既不是修复`bug`也不是添加特征的代码重构
8. `style`：不影响代码含义的修改，比如空格、格式化、缺失的分号等
9. `test`：增加确实的测试或者矫正已存在的测试

clone

设置 depth

```bash
git clone --depth 1 https://github.com/labuladong/fucking-algorithm.git

```

## Git LFS

https://git-lfs.com/

执行命令`./install.sh`，然后通过命令`git lfs install`检验是否安装成功。

