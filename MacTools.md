### 工具类

命令行工具

* `iterm2`

  > 主题: `Tango Dark`
  
  > [Powerline](https://zhuanlan.zhihu.com/p/26373052)
  
  > [Profile，直接导入iterm2即可](https://github.com/404-alan/CommontoolsForMac/blob/master/iterm2_profile.json)
 
* `oh-my-zsh`:本地默认路径`/usr/local/bin/zsh`
* `git`
* [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
  > shell语法高亮
* [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
* [z](https://www.smashingmagazine.com/2015/07/become-command-line-power-user-oh-my-zsh-z/)`(展示最近浏览路径进行快速跳转)`
  
  > 1.Copy[z.sh可执行文件]到根目录`~`下。
  
  > 2.添加`. ~/z.sh`到`~/.zshrc`文件。
  
 * [Dict-cli](https://pypi.org/project/dict-cli/)
 

文字编辑工具

* `Typora`

  > Markdown编辑工具

* `SublimeText`

  > xml等文件等查看工具
  
Android Studio

* `Shell`

  > 修改路径:Preference -> Tools -> Terminal

### Workflow

* `Alfred`
* `homebrew`
* `PlantUml`(集成在SublimeText中使用)
  * 安装`graphviz`
  * 安装[**sublime_diagram_plugin**](https://github.com/jvantuyl/sublime_diagram_plugin)
* `Git`

  |操作名|具体指令|
  |:--------:|:--------:|
  |拉取远端分支|**第一种:git checkout -b local_branch origin/remote_branch** **第二种:git branch -u origin/remote_branch local_branch** **第三种:git fetch origin remotebranch:local**|
  |绑定远程分支(**先切换本地分支哦!!**)| **git branch -u origin/remote_branch**|
  |推送本地分支到特定分支|**git push origin local:destination**|
  |推送某个Commit到特定分支|**git push origin local^:remote_branch**|
  |拉取远端分支生成新分支并把当前分支和新分支做合并|**git pull origin master:far**|
* `Gradle`

  [Gradle in shell](https://blog.csdn.net/u013634213/article/details/51120783)


### Anti GFW

* `ShadowSocks NG`
* `多态`

### 代理设置
* `Shell代理`:shell代理分两种，根据Shell类型分两种:Mac自带Bash和Zsh，都需要将一下内容拷贝到相应的设置文件中。
    ```
    function proxyoff(){
        unset http_proxy
        unset https_proxy
        echo -e "已关闭代理"
    }

    # 代理地址和端口号需要与Shadowsocks里的设置一致
    function proxyon() {
        export no_proxy="localhost,127.0.0.1,localaddress,.localdomain.com"
        export http_proxy="http://127.0.0.1:1080"
        export https_proxy=$http_proxy
        echo -e "已开启代理"
    }
    ```
   
  |Shell|Setting File|
  |:------:|:-------:|
  |`Bash`|`~/.bash_profile`|
  |[Zsh](https://ohmyz.sh/)|`~/.zshrc`|

  

* [Git代理](https://gist.github.com/laispace/666dd7b27e9116faece6)

### 特别有用的tips

  * [指令1](https://xiaozhou.net/learn-the-command-line-iterm-and-zsh-2017-06-23.html)
  * [指令2](https://linux.cn/article-10047-1.html)
  * [指令3](https://sibevin.github.io/posts/2014-09-28-094856-oh-my-zsh-tips)
  * [指令4](https://xiaozhou.net/learn-the-command-line-iterm-and-zsh-2017-06-23.html)
