## 第一次上传项目（只做一次）

```bash
git init                          # 初始化仓库
git remote add origin 仓库地址    # 关联GitHub仓库
git branch -M main                # 设置主分支名
git add .                         # 添加所有文件
git commit -m "第一次提交"         # 保存版本
git push -u origin main           # 上传到GitHub
```


## 日常更新代码（每次改完代码后）

```bash
git add .                         # 添加所有修改
git commit -m "描述改了什么"       # 保存版本
git push                          # 上传到GitHub
```

## 查看状态
```bash
git status                        # 查看哪些文件被修改了
git log                           # 查看历史提交记录
```

## 撤销操作
```bash
git checkout -- 文件名             # 撤销某个文件的修改
git reset --hard HEAD             # 撤销所有未提交的修改（危险！）
```
## 从GitHub下载项目
```bash
git clone 仓库地址                 # 把别人的项目下载到本地
git pull                          # 更新本地代码（同步GitHub上的最新版本）
```



## ⚠️ 常见问题

### 网络连接失败
报错：`fatal: unable to access: Connection was reset`

原因：国内访问 GitHub 网络不稳定

解决方法：设置代理后重试
```bash
git config --global http.proxy http://127.0.0.1:7890
git push -u origin main
```
> 注意：端口号 7890 需要换成你代理软件实际的端口