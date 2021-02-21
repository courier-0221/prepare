# prepare
使用git命令 如何将本地项目上传到git仓库中
1.打开github网址，新建一个仓库用来存放项目
2.复制仓库链接（https://github.com/courier-0221/prepare.git）
3.找到要上传的项目文件，比如prepare就是我要上传到仓库上的文件
4.在项目根目录上右击，选择git命令窗口输入以下命令
1).添加用户名和邮箱
	git config --global user.name"courier-0221"
	git config --global user.email"courier_0221@163.com"
2).在文件夹下初始化仓库
	git init 初始化仓库，将这个目录变成git可以管理的仓库
3).然后使用git add . 将文件添加到暂存区里面去注意后面你的.
4).然后执行git commit -m '描述内容’ 命令将文件提交到仓库
5).然后关联git仓库，因为此时git还不知道要将我们的项目添加到哪里去。
	接下来执行命令：
	git remote add origin 远程仓库的地址
6).【可以不执行】执行git pull --rebase origin main 命令将文件与远程仓库进行合并 
	（执行下一条命令push失败的情况下执行该命令，原因就是github网站上存在和本地不匹配的文件比如本地没有的文件）
	也就是说的上传前更新到最新。
7).然后将本地文件推送到github仓库中
	使用命令：git push -u origin main 命令
	这里会提示你的github用户名和密码然后输入登录就可以了

简便步骤
1.github网站上创建一个resources，记录下仓库连接
2.本地使用git工具clone下该仓库到本地
    git clone https://github.com/courier-0221/prepare.git
3.增加/修改/删除文件操作  【从工作区添加到暂存区】
    git add/rm xxxfile/dir
4.提交到git仓库 【从暂存区提交到git仓库】
    git  commit -m '提交描述信息'
5.push到远端github网站个人账户
    git push -u origin main
【更新】
    提交前先更新
    github网址仓库内容更新到本地命令
    git pull --rebase origin main
