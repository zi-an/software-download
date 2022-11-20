# 使用说明

eclipse因文件太大无法上传到gitee，故采用split切割(一般在linux或者MobaXterm或git里的命令)，后合并解压使用

## 切割

* windows 暂时只能使用busybox(MobaXterm或git)执行

```shell
# split -b 99m europa.zip europa. 
# ls -ahl # 生成文件如下
-rw-r--r-- 1 root 197121  99M Jun 25 11:37 europa.aa
-rw-r--r-- 1 root 197121  99M Jun 25 11:37 europa.ab
-rw-r--r-- 1 root 197121  17M Jun 25 11:37 europa.ac
-rw-r--r-- 1 root 197121 215M May 30 08:08 europa.zip 

```



## 合并

* copy(windows)

```powershell
copy /B europa.a* europa.zip
```

  

  

* cat(linux,MobaXterm,git)

```shell
cat europa.a* >> europa.zip 
```

  

* 其他方式