readme.txt--update

示例
spring使用druid配置dataSource片段代码
dataSource配置

    <!-- 基于Druid数据库链接池的数据源配置 -->
    <bean id="dataSource" class="com.alibaba.druid.pool.DruidDataSource" init-method="init" destroy-method="close">
        <!-- 基本属性driverClassName、 url、user、password -->
        <property name="driverClassName" value="com.mysql.jdbc.Driver" />
        <property name="url" value="${jdbc.url}" />
        <property name="username" value="${jdbc.username}" />
        <property name="password" value="${jdbc.password}" />
        <!-- 配置初始化大小、最小、最大 -->
        <!-- 通常来说，只需要修改initialSize、minIdle、maxActive -->
        <property name="initialSize" value="2" />
        <property name="minIdle" value="2" />
        <property name="maxActive" value="30" />
        <property name="testWhileIdle" value="false" />

        <!-- 配置获取连接等待超时的时间 -->
        <property name="maxWait" value="5000" />
        <!-- 配置一个连接在池中最小生存的时间，单位是毫秒 -->
        <property name="minEvictableIdleTimeMillis" value="30000" />
        <!-- 配置间隔多久才进行一次检测，检测需要关闭的空闲连接，单位是毫秒 -->
        <property name="timeBetweenEvictionRunsMillis" value="60000" />
        <!-- 解密密码必须要配置的项 -->
        <property name="filters" value="config" />
        <property name="connectionProperties" value="config.decrypt=true" />
    </bean>
jdbc.properties

## JDBC set
jdbc.url=jdbc\:mysql\://localhost\:3306/edu_demo?useUnicode\=true&characterEncoding\=utf-8
jdbc.username=root
jdbc.password=Obsbr4gd1oVyYr+k4KQdUMNYgKMWdDibsNJTabnph+yPmxjc6tUrT1GNsPDqa9ZvTF9QvaRD86H+Zn/H+yz2jA\=\=



如何生成密文密码?
前提:已经配置了jdk环境
生成密文密码需要准备druid的jar包.然后通过命令行生成,如下步骤:
1.准备jar包(示例使用 druid-0.2.23.jar),放到某目录下,且打开命令窗口(win用户可以在目录中 shift+鼠标右键 打开命令窗口);

2.输入命令:

java -cp druid-0.2.23.jar com.alibaba.druid.filter.config.ConfigTools you_password
我要加密的密码是:123456pwd

java -cp druid-0.2.23.jar com.alibaba.druid.filter.config.ConfigTools 123456pwd   
回车后,就会看到生成后的密文密码了,复制出来就大功告成,测试....!