- 1. 这里先说明通过ssh的链接，上传本地的文件到github上的仓库.
- 2. 先是执行: ssh-keygen -t rsa -C "youremail@example.com" 命令，该命令可以生成ssh key,youremail是github注册的邮箱,路径和密码默认就行，直接回车。
- 3.命令执行成功之后会在当下目录下生成一个 .ssh文件（文件默认不可见）。打开，选取其中的 id_rsa.pub ,复制其中的key到github上的ssh key中。
- 4.可以使用 ssh -T git@github.com 这个命令来验证是否成功。
- 5. 配置当前仓库文件上传对象的信息 或者是整个全局仓库文件上传对象的信息。如果命令为 git config --global user.name "xxx" 、 git config --global user.email xxx@xx.com。 如果去掉 --global参数，那么该配置只对当前的仓库有效。
- 6.更新目录。提交本地仓库的目录到暂存区。 git add . 
- 7.把暂存区的数据上传到版本库。 git commit -m "注释信息(说明信息)“
- 8.把放到版本库中的数据上传到远程仓库中。 git remote add origin (后面跟的是远程仓库的ssh 或是 https)
- 9.更新提交。 git push -f origin master

