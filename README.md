根目录下还有cluster.ini文件，请从群中获取。

根目录下的cluster_token.txt请自行产生。



如果git使用SSH的方式，需在`用户目录/.ssh/`目录下添加一个名为`config`的文件，前提是已经为git配置过公钥私钥，`config`文件内容如下：

```
Host github.com *.github.com
    ProxyCommand connect -H 127.0.0.1:1080 %h %p   
    IdentityFile ~/.ssh/id_rsa      
    User git
```

127.0.0.1:1080替换成你的代理地址和端口。

`~/.ssh/id_rsa`替换成你的私钥地址