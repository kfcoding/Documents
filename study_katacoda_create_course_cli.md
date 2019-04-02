
## KataCoda 客户端介绍

从命令行创建和管理课程和场景化方案。

## 实际体验步骤

### 下载客户端

`` katacoda ``  命令行是使用 ``Go`` 语言写的二进制可执行文件，直接在官方下载即可，到终端输入:

```
curl -s https://cli.katacoda.com | sudo sh
```

MacOS X  或Linux 做如下操作：

```
$ mv katacoda_darwin_amd64 /usr/local/bin
$ cd /usr/local/bin
$ ln -s katacoda_darwin_amd64 katacoda
$ chmod +x katacoda_darwin_amd64
```

然后，执行 ``katacoda``即可正常使用。不过在这之前还需要做一点工作。

### 创建个人画像

在KataCoda填写自己的个人画像。

### 创建GitHub 仓库

网页上有详细的步骤，按照相应方式执行即可。

1. 首先在自己的GitHub账户里创建一个项目。
2. 在KataCoda的画像里更新这个项目的URL。
3. 返回到GitHub项目，添加对应的WebHook秘钥。

### 使用客户端

```
$ katacoda create scenario
Creating New Katacoda Scenario. Please complete the following details to generate scenario template.

Friendly URL (katacoda.com/username/friendly-url): git-test
Scenario Title: Git
Description: git for test.
Environment ImageID (Available environments at https://katacoda.com/docs/scenarios/environments): (docker)
Scenario Layout (Available layouts at https://katacoda.com/docs/scenarios/layouts): (terminal)
New Scenario Created: git-test
Created index.json, step1.md, step2.md, step3.md, intro.md, finish.md


Complete your content and when ready, push the changes to your configured Git Repository.

```

以上即是 ``katacoda`` 命令行客户端创建情景课程的初始化过程。接下来就是上传相应的步骤文件即可。

### 上传文件到GitHub

执行下列命令:

```
$ mv git-test/ katacoda/
$ cd katacoda/
jae:katacoda lee$ ls
README.md git-test
$ git add .
$ git commit -s
[master b7e29fa] add first katacoda project.
 6 files changed, 32 insertions(+)
 create mode 100644 git-test/finish.md
 create mode 100644 git-test/index.json
 create mode 100644 git-test/intro.md
 create mode 100644 git-test/step1.md
 create mode 100644 git-test/step2.md
 create mode 100644 git-test/step3.md
$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 621 bytes | 621.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To github.com:lijiangsheng1/katacoda.git
   ed7ce67..b7e29fa  master -> master
```

### 返回katacoda

这个时候就可以看到自己刚才所创建的课程了。

如大家可以访问：[李建盛的KataCoda主页](https://www.katacoda.com/lijiansheng)，来看我刚才创建的内容。（暂时为空:-)）
