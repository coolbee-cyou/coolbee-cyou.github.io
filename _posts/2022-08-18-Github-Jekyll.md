# Github+Jekyll 搭建个人网站详细教程

## 第一步 网站托管

1. 首先你要到[GitHub](https://github.com/)上注册一个账号

2. 点击New repository–>输入仓库名称格式为：**<用户名>.github.io**->点击Create repository
   到这里，一个免费且无限流量的github代码托管仓库就创建完成了。

## 第二步 Jekyll安装

首先解释下什么是jekyll，jekyll相当于一个编译工具，安装好jekyll后，你可以通过jekyll创建一个网站模板，创建好之后，我们就可以通过http://127.0.0.1:4000/访问刚刚创建的网站了（具体jekyll用法后面再介绍），我们可以实时修改刚刚创建的模板里面的内容，并可以实时通过本地url预览改动后的效果。我们把这个博客推送到上一步创建的代码仓库里，再通过https://leach-chen.github.io/就可以访问到博客里面的内容了。有了Jekyll，我们不用每次改动一点点就把代码推送到仓库中进行预览，而是本地就可以预览。GitHub支持jekyll，hexo等语法解析。

### windows版本

#### 安装Ruby

首先点击下载[Ruby installer](https://rubyinstaller.org/)，执行安装程序，默认下一步下一步地安装；

#### 安装Gem

点击下载[RubyGems](https://rubygems.org/pages/download),下载完成后解压至你想放的位置，例如我放到E:\rubygems-2.7.4。 打开命令行执行：

```shell
e:
cd E:\rubygems-2.7.4 //进入到解压包的位置
ruby setup.rb
```

#### 安装jekyll

在命令行通过gem安装jekyll

```shell
gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
gem sources -l
gem install jekyll
```

#### 创建博客模板

```shell
cd d:
d:
jekyll new testblog
cd testblog
jekyll server
```

   在浏览器输入http://127.0.0.1:4000/即可浏览刚刚创建的blog
   到此jekyll 就安装完成了。

### Debian(Ubuntu)版本

#### 安装Ruby

```shell
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev
```

#### 安装Gem

```shell
sudo apt update
sudo apt install rubygems
```

#### 安装jekyll

在命令行通过gem安装jekyll

```shell
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
gem sources -l
gem install jekyll bundler
```

#### 创建博客模板

```shell
jekyll new testblog
cd testblog
jekyll server
```

   在浏览器输入http://127.0.0.1:4000/即可浏览刚刚创建的blog
   到此jekyll 就安装完成了。
