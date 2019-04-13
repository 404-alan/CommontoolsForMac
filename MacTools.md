### 工具类

命令行工具

* iterm2 
* oh-my-zsh
* git
* [z](https://www.smashingmagazine.com/2015/07/become-command-line-power-user-oh-my-zsh-z/)`(展示最近浏览路径进行快速跳转)`
  
  > 1.Copy[z.sh可执行文件]到根目录`~`下。
  
  > 2.添加`. ~/z.sh`到`~/.zshrc`文件。

文字编辑工具

* Typora

  > Markdown编辑工具

* SublimeText

  > xml等文件等查看工具

### Workflow

* Alfred
* homebrew
  * 1.开启`socks`代理
  * 2.在`.zshrc`文件加上`export https_proxy="[http://127.0.0.1:1087]`（端口号根据代理端口确定）
* PlantUml(集成在SublimeText中使用)
  * 安装`graphviz`
  * 安装[**sublime_diagram_plugin**](https://github.com/jvantuyl/sublime_diagram_plugin)

### Anti GFW

* ShadowSocks NG
* 多态

### 代理设置
* Shell代理:shell代理分两种，根据Shell类型分两种:Mac自带Bash和Zsh，都需要将一下内容拷贝到相应的设置文件中。
    
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
  |Bash|`~/.bash_profile`|
  |[Zsh](https://ohmyz.sh/)|`~/.zshrc`|

  

* [Git代理](https://gist.github.com/laispace/666dd7b27e9116faece6)
