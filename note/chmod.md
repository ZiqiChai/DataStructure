 权限范围的表示法如下：

- u User，即文件或目录的拥有者；
- g Group，即文件或目录的所属群组；
- o Other，除了文件或目录拥有者或所属群组之外，其他用户皆属于这个范围；
- a All，即全部的用户，包含拥有者，所属群组以及其他用户；
- r 读取权限，数字代号为“4”;
- w 写入权限，数字代号为“2”；
- x 执行或切换权限，数字代号为“1”；
- 不具任何权限，数字代号为“0”；
- s 特殊功能说明：变更文件或目录的权限。 

## 语法
```
chmod(选项)(参数)
```
## 选项
```
-c或——changes：效果类似“-v”参数，但仅回报更改的部分；
-f或--quiet或——silent：不显示错误信息；
-R或——recursive：递归处理，将指令目录下的所有文件及子目录一并处理；
-v或——verbose：显示指令执行过程；
--reference=<参考文件或目录>：把指定文件或目录的所属群组全部设成和参考文件或目录的所属群组相同；
<权限范围>+<权限设置>：开启权限范围的文件或目录的该选项权限设置；
<权限范围>-<权限设置>：关闭权限范围的文件或目录的该选项权限设置；
<权限范围>=<权限设置>：指定权限范围的文件或目录的该选项权限设置；
```

## 参数

#### 权限模式：指定文件的权限模式；
#### 文件：要改变权限的文件。 

r=读取属性　　//值＝4

w=写入属性　　//值＝2

x=执行属性　　//值＝1 

## 示例
```
chmod u+x,g+w f01　　//为文件f01设置自己可以执行，组员可以写入的权限
chmod u=rwx,g=rw,o=r f01
chmod 764 f01
chmod a+x f01　　//对文件f01的u,g,o都设置可执行属性
```
