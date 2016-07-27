1. download the jdk-*-linux-x64.tar.gz from http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
2.tar the .tar.gz 
3.mv jdk  folder to the /usr/lib/jvm
4. vim /etc/profile  tip:设置JDK环境变量（也有在~/.bashrc修改的，区别是：
	/etc/profile的设置方法对所有登陆用户都有效
	~/.bashrc只对当前用户有效）
5. add content
	export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_102
	export JRE_HOME=$JAVA_HOME/jre
	export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib
	export PATH=$JAVA_HOME/bin:$PATH
6.:wq
7.source /etc/profile
8.question:
	bash: /usr/lib/jvm/jdk1.8.0_102/bin/java: Permission denied
  solution:
	1.cd /usr/lib/jvm/jdk1.*/bin
	2.chmod 755 ./*

9.test java -version
	result:
	Ike@ubuntu:~$ java -version
	java version "1.8.0_102"
	Java(TM) SE Runtime Environment (build 1.8.0_102-b14)
	Java HotSpot(TM) 64-Bit Server VM (build 25.102-b14, mixed mode)

