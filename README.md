<!DOCTYPE html>
<html lang="zh-cn">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1" />
</head>
<body>
<a name="top"></a>
<div id="header">
<div id="HeaderTitle">
<div id="Title">
<h1><a id="Header1_HeaderTitle" class="headermaintitle" href="http://www.cnblogs.com/albertrui/">AlbertRui</a><h1>
</div>
<div id="subTitle"></div>
</div>
</div>
<div id="main">
<div id="post_detail">
	<div class="post">
		<h2>
			<a id="cb_post_title_url" href="http://www.cnblogs.com/albertrui/p/8275678.html">Spring框架学习记录</a>
		</h2>
<h2><span style="font-size: 14pt">一、Spring简介（由Rod Johnson创建的一个开源框架）</span></h2>
<div class="lemma-summary">
<div class="para"><span style="font-size: 18px">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Spring是一个开放源代码的设计层面框架，他解决的是业务逻辑层和其他各层的松耦合问题，因此它将面向接口的编程思想贯穿整个系统应用。Spring是于2003 年兴起的一个轻量级的Java 开发框架，由Rod Johnson创建。简单来说，Spring是一个分层的JavaSE/EE<strong>full-stack(</strong><strong>一站式)</strong> 轻量级开源框架。</span></div>
<h2 class="para"><span style="font-size: 14pt">二、Spring起源</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px">　　你可能正在想“Spring不过是另外一个的framework”。当已经有许多开放源代码（和专有）J2EEframework时，我们为什么还需要Spring Framework？</span></div>
<div class="para"><span style="font-size: 18px">　　Spring是独特的，因为若干个原因：</span></div>
<div class="para">
<ul>
<li><span style="font-size: 18px">它定位的领域是许多其他流行的framework没有的。Spring致力于提供一种方法管理你的业务对象。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring是全面的和模块化的。Spring有分层的体系结构，这意味着你能选择使用它孤立的任何部分，它的架构仍然是内在稳定的。因此从你的学习中，你可得到最大的价值。例如，你可能选择仅仅使用Spring来简单化JDBC的使用，或用来管理所有的业务对象。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">它的设计从底部帮助你编写易于测试的代码。Spring是用于测试驱动工程的理想的framework。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring对你的工程来说，它不需要一个以上的framework。Spring是潜在地一站式解决方案，定位于与典型应用相关的大部分基础结构。它也涉及到其他framework没有考虑到的内容。</span></li>
</ul>
</div>
<h2 class="para"><span style="font-size: 14pt">三、背景</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px">　　Rod Johnson在2002年编著的《Expert one on one J2EE design and development》一书中，对Java EE 系统框架臃肿、低效、脱离现实的种种现状提出了质疑，并积极寻求探索革新之道。以此书为指导思想，他编写了interface21框架，这是一个力图冲破J2EE传统开发的困境，从实际需求出发，着眼于轻便、灵巧，易于开发、测试和部署的轻量级开发框架。Spring框架即以interface21框架为基础，经过重新设计，并不断丰富其内涵，于2004年3月24日，发布了1.0正式版。同年他又推出了一部堪称经典的力作《Expert one-on-one J2EE Development without EJB》，该书在Java世界掀起了轩然大波，不断改变着Java开发者程序设计和开发的思考方式。在该书中，作者根据自己多年丰富的实践经验，对EJB的各种笨重臃肿的结构进行了逐一的分析和否定，并分别以简洁实用的方式替换之。至此一战功成，Rod Johnson成为一个改变Java世界的大师级人物。</span></div>
<div class="para"><span style="font-size: 18px">　　传统J2EE应用的开发效率低，应用服务器厂商对各种技术的支持并没有真正统一，导致J2EE的应用没有真正实现Write Once及Run Anywhere的承诺。Spring作为开源的中间件，独立于各种应用服务器，甚至无须应用服务器的支持，也能提供应用服务器的功能，如声明式事务、事务处理等。</span></div>
<div class="para"><span style="font-size: 18px">　　Spring致力于J2EE应用的各层的解决方案，而不是仅仅专注于某一层的方案。可以说Spring是企业应用开发的“一站式”选择，并贯穿表现层、业务层及持久层。然而，Spring并不想取代那些已有的框架，而是与它们无缝地整合。</span></div>
<h2 class="para"><span style="font-size: 14pt">四、框架特征</span></h2>
<div class="para">
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>轻量</strong>——从大小与开销两方面而言Spring都是轻量的。完整的Spring框架可以在一个大小只有1MB多的JAR文件里发布。并且Spring所需的处理开销也是微不足道的。此外，Spring是非侵入式的：典型地，Spring应用中的对象不依赖于Spring的特定类。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>控制反转</strong>——Spring通过一种称作控制反转（IoC）的技术促进了低耦合。当应用了IoC，一个对象依赖的其它对象会通过被动的方式传递进来，而不是这个对象自己创建或者查找依赖对象。你可以认为IoC与JNDI相反——不是对象从容器中查找依赖，而是容器在对象初始化时不等对象请求就主动将依赖传递给它。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>面向切面</strong>——Spring提供了面向切面编程的丰富支持，允许通过分离应用的业务逻辑与系统级服务（例如审计（auditing）和事务（transaction）管理）进行内聚性的开发。应用对象只实现它们应该做的——完成业务逻辑——仅此而已。它们并不负责（甚至是意识）其它的系统级关注点，例如日志或事务支持。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>容器</strong>——Spring包含并管理应用对象的配置和生命周期，在这个意义上它是一种容器，你可以配置你的每个bean如何被创建——基于一个可配置原型（prototype），你的bean可以创建一个单独的实例或者每次需要时都生成一个新的实例——以及它们是如何相互关联的。然而，Spring不应该被混同于传统的重量级的EJB容器，它们经常是庞大与笨重的，难以使用。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>框架</strong>——Spring可以将简单的组件配置、组合成为复杂的应用。在Spring中，应用对象被声明式地组合，典型地是在一个XML文件里。Spring也提供了很多基础功能（事务管理、持久化框架集成等等），将应用逻辑的开发留给了你。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px"><strong>MVC</strong>——Spring的作用是整合，但不仅仅限于整合，Spring 框架可以被看做是一个企业解决方案级别的框架。客户端发送请求，服务器控制器（由DispatcherServlet实现的)完成请求的转发，控制器调用一个用于映射的类HandlerMapping，该类用于将请求映射到对应的处理器来处理请求。HandlerMapping 将请求映射到对应的处理器Controller（相当于Action）在Spring 当中如果写一些处理器组件，一般实现Controller 接口，在Controller 中就可以调用一些Service 或DAO 来进行数据操作 ModelAndView 用于存放从DAO 中取出的数据，还可以存放响应视图的一些数据。 如果想将处理结果返回给用户，那么在Spring 框架中还提供一个视图组件ViewResolver，该组件根据Controller 返回的标示，找到对应的视图，将响应response 返回给用户。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">所有Spring的这些特征使你能够编写更干净、更可管理、并且更易于测试的代码。它们也为Spring中的各种模块提供了基础支持。</span></li>
</ul>
</div>
<h2 class="para"><span style="font-size: 14pt">五、特性</span></h2>
<div class="para">
<div class="para">
<ul>
<li><span style="font-size: 18px">强大的基于 JavaBeans的采用控制反转（Inversion of Control，IoC）原则的配置管理，使得应用程序的组件更加快捷简易。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">一个可用于从 applet 到 Java EE 等不同运行环境的核心 Bean 工厂。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">数据库事务的一般化抽象层，允许宣告式(Declarative)事务管理器，简化事务的划分使之与底层无关。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">内建的针对 JTA 和 单个 JDBC 数据源的一般化策略，使 Spring 的事务支持不要求 Java EE 环境，这与一般的 JTA 或者 EJB CMT 相反。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">JDBC 抽象层提供了有针对性的异常等级(不再从SQL异常中提取原始代码), 简化了错误处理, 大大减少了程序员的编码量. 再次利用JDBC时，你无需再写出另一个 '终止' (finally) 模块. 并且面向JDBC的异常与Spring 通用数据访问对象(Data Access Object) 异常等级相一致.</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">以资源容器，DAO 实现和事务策略等形式与 Hibernate，JDO 和 iBATIS SQL Maps 集成。利用众多的反转控制方便特性来全面支持, 解决了许多典型的Hibernate集成问题. 所有这些全部遵从Spring通用事务处理和通用数据访问对象异常等级规范.</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">灵活的基于核心 Spring 功能的 MVC 网页应用程序框架。开发者通过策略接口将拥有对该框架的高度控制，因而该框架将适应于多种呈现(View)技术，例如 JSP，FreeMarker，Velocity，Tiles，iText 以及 POI。值得注意的是，Spring 中间层可以轻易地结合于任何基于 MVC 框架的网页层，例如 Struts，WebWork，或 Tapestry。</span></li>
<li><span style="font-size: 18px">提供诸如事务管理等服务的面向切面编程(AOP)框架。</span></li>
</ul>
</div>
</div>
<h2 class="para"><span style="font-size: 14pt">六、特点</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px"><strong>　　1.方便解耦，简化开发</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　通过Spring提供的IoC容器，我们可以将对象之间的依赖关系交由Spring进行控制，避免硬编码所造成的过度程序耦合。有了Spring，用户不必再为单实例模式类、属性文件解析等这些很底层的需求编写代码，可以更专注于上层的应用。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　2.AOP</strong><strong>编程</strong><strong>的支持</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　通过Spring提供的AOP功能，方便进行面向切面的编程，许多不容易用传统OOP实现的功能可以通过AOP轻松应付。</span></div>
<div class="para"><span style="font-size: 18px">　　3.<strong>声明式事务</strong><strong>的支持</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　在Spring中，我们可以从单调烦闷的事务管理代码中解脱出来，通过声明式方式灵活地进行事务的管理，提高开发效率和质量。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　4.方便程序的测试</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　可以用非容器依赖的编程方式进行几乎所有的测试工作，在Spring里，测试不再是昂贵的操作，而是随手可做的事情。例如：Spring对Junit4支持，可以通过注解方便的测试Spring程序。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　5.方便集成各种优秀框架</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　Spring不排斥各种优秀的开源框架，相反，Spring可以降低各种框架的使用难度，Spring提供了对各种优秀框架（如Struts,Hibernate、Hessian、Quartz）等的直接支持。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　6.降低Java EE API的使用难度</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　Spring对很多难用的Java EE API（如JDBC，JavaMail，远程调用等）提供了一个薄薄的封装层，通过Spring的简易封装，这些Java EE API的使用难度大为降低。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　7.Java 源码是经典学习范例</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　Spring的源码设计精妙、结构清晰、匠心独运，处处体现着大师对Java设计模式灵活运用以及对Java技术的高深造诣。Spring框架源码无疑是Java技术的最佳实践范例。如果想在短时间内迅速提高自己的Java技术水平和应用开发水平，学习和研究Spring源码将会使你收到意想不到的效果。</span></div>
<h2 class="para"><span style="font-size: 14pt">七、为什么要使用Spring</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px">　　在我们进入细节以前，让我们看一下Spring可以给一个工程带来的一些好处：</span></div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring能有效地组织你的中间层对象，无论你是否选择使用了EJB。如果你仅仅使用了Struts或其他的包含了J2EE特有API，framework，你会发现Spring关注了遗留下的问题。Spring能消除在许多工程上对Singleton的过多使用。这是一个主要的问题，它减少了系统的可测试性和面向对象特性。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring能消除使用各种各样格式的属性定制文件的需要，在整个应用和工程中，可通过一种一致的方法来进行配置。曾经感到迷惑，一个特定类要查找迷幻般的属性关键字或系统属性，为此不得不读Javadoc乃至源编码吗？有了Spring，你可很简单地看到类的JavaBean属性。倒置控制的使用（在下面讨论）帮助完成这种简化。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring能通过接口而不是类促进好的编程习惯，减少编程代价到几乎为零。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring被设计为让使用它创建的应用尽可能少的依赖于他的APIs。在Spring应用中的大多数业务对象没有依赖于Spring。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">使用Spring构建的应用程序易于单元测试。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring能使EJB的使用成为一个实现选择，而不是应用架构的必然选择。你能选择用POJOs或local EJBs来实现业务接口，却不会影响调用代码。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring帮助你解决许多问题而无需使用EJB。Spring能提供一种EJB的替换物，它们适于许多web应用。例如，Spring能使用AOP提供声明性事务而不通过使用EJB容器，如果你仅仅需要与单个的数据库打交道，甚至不需要JTA实现。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring为数据存取提供了一致的框架，不论是使用JDBC或O/R mapping产品（如Hibernate）。</span></li>
</ul>
</div>
<div class="para">
<ul>
<li><span style="font-size: 18px">Spring确实使你能通过最简单可行的解决办法解决你的问题。这些特性是有很大价值的。</span></li>
</ul>
</div>
<div class="para"><span style="font-size: 18px"><strong>　　总结起来，Spring有如下优点：</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　1.低侵入式设计，代码污染极低</span></div>
<div class="para"><span style="font-size: 18px">　　　　2.独立于各种应用服务器，基于Spring框架的应用，可以真正实现Write Once,Run Anywhere的承诺</span></div>
<div class="para"><span style="font-size: 18px">　　　　3.Spring的DI机制降低了业务对象替换的复杂性，提高了组件之间的解耦</span></div>
<div class="para"><span style="font-size: 18px">　　　　4.Spring的AOP支持允许将一些通用任务如安全、事务、日志等进行集中式管理，从而提供了更好的复用</span></div>
<div class="para"><span style="font-size: 18px">　　　　5.Spring的ORM和DAO提供了与第三方持久层框架的良好整合，并简化了底层的数据库访问</span></div>
<div class="para"><span style="font-size: 18px">　　　　6.Spring并不强制应用完全依赖于Spring，开发者可自由选用Spring框架的部分或全部</span></div>
<h2 class="para"><span style="font-size: 14pt">八、作用</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px">　　Spring提供许多功能，在此我将快速地依次展示其各个主要方面（图片来自Spring官网）<span class="description"> <br></span></span></div>
<div class="para"><span style="font-size: 18px"><span class="description"><span class="description">&nbsp; <img src="https://images2017.cnblogs.com/blog/1268854/201801/1268854-20180114140921426-853446737.png" alt=""></span></span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></div>
<div class="para"><span style="font-size: 18px">　　首先，让我们明确Spring范围。尽管Spring覆盖了许多方面，但我们已经有清楚的概念，它什么应该涉及和什么不应该涉及。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　Spring的主要目的是使JavaEE易用和促进好编程习惯。</strong></span></div>
<div class="para"><span style="font-size: 18px">　　Spring不重新开发已有的东西。因此，在Spring中你将发现没有日志记录的包，没有连接池，没有分布事务调度。这些均有开源项目提供（例如Commons Logging 用来做所有的日志输出，或Commons DBCP用来作数据连接池），或由你的应用程序服务器提供。因为同样的的原因，我们没有提供O/R mapping层，对此，已有友好的解决办法如Hibernate和JDO。</span></div>
<div class="para"><span style="font-size: 18px">　　<strong>Spring的目标是使已存在的技术更加易用</strong>。</span></div>
<div class="para"><span style="font-size: 18px">　　例如，尽管我们没有底层事务协调处理，但我们提供了一个抽象层覆盖了JTA或任何其他的事务策略。Spring没有直接和其他的开源项目竞争，除非我们感到我们能提供新的一些东西。例如，像许多开发人员，我们从来没有为Struts高兴过，并且感到在MVC web framework中还有改进的余地。在某些领域，例如轻量级的IoC容器和AOP框架，Spring有直接的竞争，但是在这些领域还没有已经较为流行的解决方案。（Spring在这些区域是开路先锋。）</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　Spring也得益于内在的一致性。</strong></span></div>
<div class="para"><span style="font-size: 18px">　　所有的开发者都在唱同样的的赞歌，基础想法依然是Expert One-on-One J2EE设计与开发的那些。</span></div>
<div class="para"><span style="font-size: 18px">　　并且我们已经能够使用一些主要的概念，例如倒置控制，来处理多个领域。</span></div>
<div class="para"><span style="font-size: 18px"><strong>　　Spring在应用服务器之间是可移植的</strong>。</span></div>
<div class="para"><span style="font-size: 18px">　　当然保证可移植性总是一次挑战，但是我们避免任何特定平台或非标准化，并且支持在WebLogic，Tomcat，Resin，JBoss，WebSphere和其他的应用服务器上的用户。</span></div>
<h2 class="para"><span style="font-size: 14pt">九、作为Java平台最基本的框架</span></h2>
<div class="para">
<div class="para"><span style="font-size: 18px">　　Spring 框架是一个分层架构，由 7 个定义良好的模块组成。Spring模块构建在核心容器之上，核心容器定义了创建、配置和管理 bean 的方式，如图所示：</span></div>
<div class="para"><span class="image-link" style="width: 220px; height: 114px; font-size: 18px"><span class="image-link" style="width: 220px; height: 114px"> <img src="https://images2017.cnblogs.com/blog/1268854/201801/1268854-20180112142720160-122795874.png" alt=""></span></span></div>
<div class="para"><span style="font-size: 18px"><strong>　　组成Spring框架的每个模块（或组件）都可以单独存在，或者与其他一个或多个模块联合实现。每个模块的功能如下：</strong></span></div>
<div class="para"><span style="font-size: 18px">　　　　1、核心容器：核心容器提供 Spring 框架的基本功能(Spring Core)。核心容器的主要组件是 BeanFactory，它是工厂模式的实现。BeanFactory 使用控制反转（IOC） 模式将应用程序的配置和依赖性规范与实际的应用程序代码分开。</span></div>
<div class="para"><span style="font-size: 18px">　　　　2、Spring 上下文：Spring 上下文是一个配置文件，向 Spring框架提供上下文信息。Spring 上下文包括企业服务，例如JNDI、EJB、电子邮件、国际化、校验和调度功能。</span></div>
<div class="para"><span style="font-size: 18px">　　　　3、Spring AOP：通过配置管理特性，Spring AOP 模块直接将面向切面的编程功能集成到了 Spring 框架中。所以，可以很容易地使 Spring 框架管理的任何对象支持AOP。Spring AOP 模块为基于 Spring 的应用程序中的对象提供了事务管理服务。通过使用 Spring AOP，不用依赖 EJB 组件，就可以将声明性事务管理集成到应用程序中。</span></div>
<div class="para"><span style="font-size: 18px">　　　　4、Spring DAO：JDBCDAO抽象层提供了有意义的异常层次结构，可用该结构来管理异常处理和不同数据库供应商抛出的错误消息。异常层次结构简化了错误处理，并且极大地降低了需要编写的异常代码数量（例如打开和关闭连接）。Spring DAO 的面向 JDBC 的异常遵从通用的 DAO 异常层次结构。</span></div>
<div class="para"><span style="font-size: 18px">　　　　5、Spring ORM：Spring 框架插入了若干个ORM框架，从而提供了 ORM 的对象关系工具，其中包括JDO、Hibernate和iBatisSQL Map。所有这些都遵从 Spring 的通用事务和 DAO 异常层次结构。</span></div>
<div class="para"><span style="font-size: 18px">　　　　6、Spring Web 模块：Web 上下文模块建立在应用程序上下文模块之上，为基于 Web 的应用程序提供了上下文。所以，Spring框架支持与 Jakarta Struts 的集成。Web 模块还简化了处理多部分请求以及将请求参数绑定到域对象的工作。</span></div>
<div class="para"><span style="font-size: 18px">　　　　7、Spring MVC 框架：MVC框架是一个全功能的构建 Web应用程序的 MVC 实现。通过策略接口，MVC框架变成为高度可配置的，MVC 容纳了大量视图技术，其中包括 JSP、Velocity、Tiles、iText 和 POI。模型由javabean构成，存放于Map；视图是一个接口，负责显示模型；控制器表示逻辑代码，是Controller的实现。Spring框架的功能可以用在任何J2EE服务器中，大多数功能也适用于不受管理的环境。Spring 的核心要点是：支持不绑定到特定 J2EE服务的可重用业务和数据访问对象。毫无疑问，这样的对象可以在不同J2EE 环境（Web 或EJB）、独立应用程序、测试环境之间重用。</span></div>
<div class="para"><span style="font-size: 18px">&nbsp;</span></div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>	
</div>	
</div>
</body>
</html>
