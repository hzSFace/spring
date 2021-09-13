refresh->finishBeanFactoryInitialization->preInstantiateSingletons
->getBean->doGetBean->createBean->doCreateBean

AbstractAutowireCapableBeanFactory.doCreateBean 创建Bean实例
1.createBeanInstance：实例化Bean
2.populateBean：设置Bean的属性，依赖注入
3.initializeBean：初始化Bean
    （1）、invokeAwareMethods：调用Aware接口的方法设置值
    （2）、applyBeanPostProcessorsBeforeInitialization：调用BeanPostProcessors的初始化之前的方法
    （3）、invokeInitMethods：调用初始化方法
        a）如果实现了InitializingBean接口，调用afterPropertiesSet方法
        b）如果自定义了init方法，则调用自定义的init方法
    （4）、applyBeanPostProcessorsAfterInitialization：调用BeanPostProcessors的初始化之后的方法
4.registerDisposableBeanIfNecessary：注册Bean的销毁方法 