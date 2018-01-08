# 安装hugo

Hugo的安装十分简单，安装时不需要安装任何依赖软件，其本身只是一个二进制文件，可以使用以下几种方式安装：

## 直接使用二进制文件安装

到[Hugo release](https://github.com/gohugoio/hugo/releases)下载对应系统的安装包，解压后放到`$PATH`目录下即可使用

## 使用go get安装

这种安装方式的前提是您的电脑上已经配置了Go开发环境，为了简单起见，建议直接下载贬义好的发型版安装。

```bash
go get -u -v github.com/gohugoio/hugo
```

详细方式请参考：https://github.com/gohugoio/hugo

## Brew安装

如果您是Mac用户，可以使用`brew`命令来安装。

```bash
brew install hugo
```

**注意**：这种安装方式安装的往往不是最新版本的hugo，如果要使用最新版的hugo，请使用前两种方式安装。