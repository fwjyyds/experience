# experience
experience about solving some problems in applivation

tds 2024.12.4 in chendu

Fallen in love with sb,i deto be powerful...

tds 2024.12.4 in chendu

Fallen in love with sb,i deto be powerful...

前提知识;
配置ssh令牌
1. 使用个人访问令牌（Personal Access Token）
步骤 1: 生成个人访问令牌
登录到你的 GitHub 账户。
点击右上角的头像，选择 Settings。
在左侧菜单中选择 Developer settings。
选择 Personal access tokens，然后点击 Generate new token。
选择你需要的权限（至少选择 repo 权限），然后生成令牌。
复制生成的令牌，因为一旦离开页面，你将无法再次查看它。
步骤 2: 使用令牌进行身份验证
当你在命令行中进行 git push 或 git pull 时，系统会提示你输入用户名和密码。此时：

用户名：输入你的 GitHub 用户名。
密码：输入你刚刚生成的个人访问令牌（而不是你的 GitHub 密码）。
2. 使用 SSH 密钥
步骤 1: 生成 SSH 密钥
如果你还没有 SSH 密钥，可以使用以下命令生成一个新的 SSH 密钥：

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
DiffCopyInsert
按照提示完成密钥生成过程。

步骤 2: 添加 SSH 密钥到 GitHub
将生成的公钥添加到 GitHub：
cat ~/.ssh/id_rsa.pub

切记代码复制查看，而不是直接复制

DiffCopyInsert
复制输出内容。
登录到你的 GitHub 账户。
点击右上角的头像，选择 Settings。
在左侧菜单中选择 SSH and GPG keys。
点击 New SSH key，粘贴你复制的公钥，并保存。
步骤 3: 使用 SSH URL
将你的远程仓库 URL 从 HTTPS 改为 SSH：

git remote set-url origin git@github.com:fwjyyds/experience.git
DiffCopyInsert
3. 验证身份验证
完成上述步骤后，尝试再次进行 git push 或 git pull，应该不会再出现身份验证失败的错误。

参考文档
GitHub 关于远程仓库的文档
GitHub 关于个人访问令牌的文档
通过以上方法，你应该能够成功解决身份验证失败的问题。


git项目开发和管理
1.点击个人主页选择仓库点击new
2.填写名字和描述创建仓库
3.进入仓库点击main分支搜索q创建q分支
4.git clone (code里的http路径)    
5.创建和远程一样的分支q,git checkout q
6.开发的时候切换为q,git checkout q
7.上传本地分支先q后master,git add .,git commit -m "name",git pull origin q,git push origin q
8.如果不行，修改git remote set-url origin 仓库ssh路径
9.git checkout master
10.git merge q
11.git pull origin master
12.git push origin master
13.如果遇到不同分支无法pull,master git reset --hard 合并版本，在实现

 

