# alex-base
    向 maven 中央仓库提交
        1、注册账号，之后在 maven/settings.xml 里面增加配置段落
```html
	<server> 
		<id>sonatype</id> 
		<username>alexgaoyh</username> 
		<password>alexgaoyh</password> 
	</server>
```
        2、如果出现 gpg.ext 找不到的错误，同样在 maven/settings.xml 里面增加配置段落
```html
	<profile>
		<id>sonatype</id>
		<activation>
			<activeByDefault>true</activeByDefault>
		</activation>
		<properties>
			<gpg.executable>D:\GnuPG\bin\gpg</gpg.executable>
			<gpg.passphrase>alexgaoyh</gpg.passphrase>
		</properties>
	</profile>
```

        3、其他部分详见 pom.xml 
            3.1、https://issues.sonatype.org/ 上的评论部分，会提示到  s01.oss.sonatype.org ， pom.xml 上需要按情况调整；
            3.2、执行 deploy 命令即可；
