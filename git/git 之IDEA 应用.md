##  git 之IDEA 应用
找到
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-3828f649b9e132a0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

选择本地仓库
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-450703c0649446c3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-11ed9cb74e3d6c37.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-36a0fa8450fc1f19.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-d1df40af9e418057.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

 ###IDEA中 如何将本地项目提交到本地仓库和远程仓库(github),下面是想详细的操作步骤：
*  1.要使用GitHub,首先你需要下载一个Github  (地址:[http://windows.github.com/](http://windows.github.com/)) 这里使用的是for Windows (我的系统是win 10) 然后安装完成会得到如下的一个目录：

![](http://upload-images.jianshu.io/upload_images/3946479-1e47306c6ff8ef06.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 2. 在Idea 里面做相关配置： 打开设置面板(Ctrl+Alt+S),点击左边功能面板列表中的**Version Control**(版本控制)如下图：

![](http://upload-images.jianshu.io/upload_images/3946479-57a13f35c9b42a1a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在这里有许多进行版本控制的配置,我们要用的是**Git** ** ** 
* 3. 然后我们点击第六项 **GitHub**(本文默认你已经拥有了一个github账号,如果没有请先注册) 然后Host一栏填写github 的地址: github.com 在 Login 一栏填写你的github 账号，Password 一栏填写密码 填写完成后点击 Test按钮，此时 IDEA 会根据你填写的内容远程访问github社区,如果账号和密码输入正确会提示你链接成功

![](http://upload-images.jianshu.io/upload_images/3946479-ce0344ad09ec2e1c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 4. 接下来，点击左边面板的功能列表中的Git 进行配置 这里面有许多配置，其实基本按照默认的就行了,无需做其他更多的操作。 在Path to Git executable一栏,选择刚才安装的git路径下bin\git.exe 然后点击后面的Test按钮,如果配置成功会看到如下界面：

![](http://upload-images.jianshu.io/upload_images/3946479-7b51d4ec5de02921.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后点击, Apply，OK 按钮 完成配置。 IDEA对Git的相关配置到此就结束了。 

### 关于项目的本地提交(Commit)** ** ** **

** 1.创建本地仓库** 在IDEA中创建任意一个项目，在IDEA的菜单栏中选择 VCS (倒数第三项)，选择Import into Version Control (引入到版本控制) --> Create Git Repository... -->选择一个存放的路径(本文为:I:\workspace\NCPlatform)--> OK 这样就创建了一个本地仓库， 以后代码的本地提交(Commit)的内容都会更新到这个选择的路径中   

**2.将项目提交到本地的Git**  选中项目(或者文件) 右键选择Git--->Add (此时没任何反应)---->commit(提交)  注意:一定要先add 再提交 此时项目文件就添加到本地仓库了

![](http://upload-images.jianshu.io/upload_images/3946479-e2f8522818b080c1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### **关于远程仓库的配置**

** 1.在github上创建一个仓库** : 登陆你的github -->点击你的用户名 -->选择Repositories--> 点击绿色-->输入你的仓库名称 (此时远程仓库创建完成) 
**2.通过Git shell 配置远程仓库**：  
①进入到项目目录：

![](http://upload-images.jianshu.io/upload_images/3946479-6ea9bcc84b7b8dcb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后复制刚才创建的远程仓库的HTTPS/SSH KEY (此处使用的SSH),在Git shell 中键入如下脚本 git remote add origin [git@github.com](mailto:git@github.com):teamaxxiaohu/NCPlatform.git(此处为你自己远程仓库的key)git push -u origin master (解释:该脚本将本地的master 推到刚才设置的github远程仓库中)   如果执行完成2条脚本,没有任何提示,也没任何错误,恭喜你成功了!    
**3. 回到IDEA**，选择项目 -->Git -->Repository --Push  即可将本地的文件推送到远程仓库中，然后刷新你的github仓库你就会看到 你提交的本地内容了,同时你在idea中也能看到你的操作信息。

![](http://upload-images.jianshu.io/upload_images/3946479-7b15268a498bbf08.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/3946479-12673290b4dc88bb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

注意：在执行 通过Gitshell配置远程仓库的时候可能会出现一些意外: 

* 1.  提示这个仓库已经存在(fatal: remote origin already exists) ，如果是这样 就不需要使用add + 地址的形式了 ,请修改为: git remote rm origin  
* 2.提示不能移除配置信息错误(.error: Could not remove config section 'remote.origin') 

解决方案: 在window/用户下面找到.gitconfig文件 (本文路径为:C:\Users\Vincent_2\.gitconfig)打开它把里面的[remote "origin"]那一行删掉   重启gitshell   再重新配置。
 
