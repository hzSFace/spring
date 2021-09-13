AOP：AspectJ Oriented Program，面向切面编程，在Spring IOC的基础上进行扩展
扩展了OOP面向对象变成的功能，OOP的核心是对象，AOP的核心是关注点/连接点Joint Point

动态代理：JDK动态代理和CGLIB动态代理
指在程序运行时，动态的将某段代码切入到指定方法指定位置进行运行的编程方式；
JDK动态代理：实现了接口，利用了反射
CGLIB动态代理：未实现接口，类不能被final修饰，利用asm的特性

AOP的应用：事务、日志、权限、安全、交易

AOP的两种实现方式：
AspectJ
XML


主配置类中添加@EnableAspectJAutoProxy注解，开启aop支持



