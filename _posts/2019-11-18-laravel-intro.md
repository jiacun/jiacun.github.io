---
layout: laravel
title: 一份简明的 laravel 笔记与教程
categories: laravel
description: 一份简明的 laravel 笔记与教程
keywords: laravel git
---
*** 
# laravel

---

1.git安装

2.git的使用
	自报家门:
		git config --global user.name "Your Name"
		git config --global user.email "1045514670@qq.com"


	1)指定一个目录座位git工作区的仓库
	git init    git 初始化
		master
	
	2) 把工作区里面的文件 存放到暂存区 
		git add .
			. 代表 修改的文件和新创建的文件
	
	3)把暂存区里面的文件 提交到本地git仓库中
	git commit -m '注释的信息'
	
	4)建立本地和远程的链接
	// origin 这个是可以自定义的  这个只是一个别名
	//是谁的别名? 是远程地址的别名
	git remote add origin  https://github.com/kl412825/214.git
	
	5)把本地的仓库信息推到远程仓库上去
	git push origin master

3.分支
	//查看分支
	git branch

	//创建分支
	git branch 分支名
	//切换分支
	git checkout 分支名
	或者
	//创建分支并且进行切换分支
	git checkout -b 分支名
	
	//删除分支
	git branch -d www
	
	//在分支里面进行命令推送代码
	git add .
	git commit -m 'zjc'
	
	//(1)第一个wjs 是本地的分支
	//(2)第二个wjs 要远程仓库里面创建一个新的分支
	git push origin zjc:zjc
	
	//就会看见在远程仓库里面有一个新的分支出现
	
	//我怎么把自己分支上开发的新的代码合并到主分支上去
	
	//注意:
	
		在合并的时候不要在你的分支上进行合并
		要切换到主分支上去
		git checkout master
		
		切换完成之后再进行合并
		git merge 分支名
	
		//把合并完的代码推动到主分支上
		git push origin master

4.别人是怎么开发的
	//首先克隆
	1) 把代码下载下来
	2) xkh已经和远程地址建立了连接
	git clone https://github.com/kl412825/214.git

	//我现在就有wjs开发的代码
	
	//创建并且切换分支
	git checkout -b zjc
	
	//新建文件
	git add .
	git commit -m '注释'
	
	git push origin xjh:xjh
	
	//合并
	切换分支
		git checkout master
	
		git merge zjc
	
		git push origin master
	
	
	
	别人想要xjh开发的代码
	//pull 拉取
	git pull origin master

//解决不用输入用户名和密码


//添加合作者

# laravel
### 创建控制器

//注意点:
	你们在创建目录的名字的时候 注意大小写

	举例:
		php artisan make:controller Admin/UserController
	
		php artisan make:cintroller admin/LinksController
	

总结
总结
	1)报家门
	2)建立分支
	3)在自己的分支上开发
	4)master合并分支的代码

	5)别人想要主分支上的代码
---