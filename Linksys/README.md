# Linksys路由器固件解密

## 解密流程

```
寻找过渡版本

对过渡版本解包 -- `binwalk`

寻找key  -- `grep -arl "BEGIN PGP"`

将key导入本地gpg环境  -- `gpg --import  key_filename`

固件解密  --  `gpg --decrypt   filename.gpg.bin  > newname
```

## 测试

```
下载链接：
    https://www.linksys.com/sg/support-article/?articleNum=148460
具体固件：
    FW_RE6500_v1.0.013.001_20210924.gpg.bin
    FW_RE6500_v1.0.05.003_20160305.bin
固件加密：
    gpg加密，过渡版本为1.0.05.003
    
下载链接：
    https://www.linksys.com/sg/support-article/?articleNum=148444
具体固件：
    FW_EA6100_1.1.6.181939_prod.gpg.img
    FW_EA6100_1.1.5.172244_prod.img
固件加密：
    gpg加密，过渡版本为1.1.5.172244
```

## 参考链接

https://www.anquanke.com/post/id/246659