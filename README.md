# 前言

##  一、什么是设计模式？

什么样的程序员是一个好的程序员？学会很多门编程语言，就是一个好的程序员了么？事实上，学会一门编程语言不是一件很难的事，而“学会”一门编程语言是非常难的一件事。前一个“会”强调“能”，懂语法，能写简单的程序就算是前者的“会”了；后一个“会”，强调“精”，显然，光能写出“Hello World”并不算是后者的“会”，能熟练应用，并用编程语言解决各种问题，才算是真正的“会”。编程语言就像是世界上任何有意义的东西一样，它在一直变化，一直进化，此刻学会的编程语言，到了下一刻，就可能有新东西出来，跟上它进步的节奏，本身就是一件非常费精力的事，更别说去在这个基础上，去“会”第二门编程语言了。因而，个人认为，使用过很多种的编程语言，并不是成为一个好的程序员的充分条件。一个好的程序员，更多的体现不应该在他会使用多少“工具”，而是他能使用这些“工具”，创造多么大的成绩，解决多么大的问题。掌握解决问题的方法，能用自己精通的编程语言解决各种问题，这才是成为一个优秀程序所必备的。
正因为如此，我们才需要学习设计模式。设计模式是面对各种问题进行提炼和抽象而形成的解决方案。这些设计方案是前人不断试验，考虑了封装性、复用性、效率、可修改、可移植等各种因素的高度总结。它不限于一种特定的语言，它是一种解决问题的思想和方法。

## 二、设计模式的意义

现在社会的发展可谓突飞猛进，过去常常被当作软件行业标杆的“软件工程”设计模型，逐渐让出了它的半壁江山，给了一种叫作“敏捷开发、快速迭代”的软件开发方式。快速迭代的环境下，需求就显得不那么明确，需求常常伴随着整个项目的进行而变化。需求的不确定性，对程序编写的要求就会比较高了。首先要考虑各种可能需求的兼容，但考虑的需求越多，就很容易陷入整个软件架构设计的深渊，不可自拔。设计模式对需求变更与代码重用的考虑，可以被作为软件设计的参考，由于设计模式基本上本着“高内聚、低耦合”的原则，遵循设计模式而设计的代码结构，常常会有着对需求的适应性。
一个大型的软件项目，不可能由一个人完成，此类项目常常需要多个软件开发工程师的协同开发。既然是协同开发，就一定会涉及到模块间的相互影响，一个工程师编写的一行代码，可能会影响到其它工程师代码的诸多因子。如果工程师之间的相互影响过大，那么整个项目无法形成合力，也就无法按时保质完成。最理想的情况下，一个工程师的代码不要影响到别人的模块，但有时，又不得不去借用或者被借到其它模块。这其中的组织，也是需要智慧的。设计模式同样可以作为协同作业的参考，遵循设计模式而设计的代码结构，尽可能地减少模块间的不必要依赖，在协同工作条件下，对项目的有序进行有着非常大的帮助。
公司人事会有变动，程序员也会成长。不管是哪种情况，代码非常有可能会被移交，即代码的编写者和维护者很有可能会是不同的人。那么代码的可读性就显得非常重要了。由于高级语言的出现，让机器读懂你的意图已经不是最主要的“矛盾”，而让人读懂你的意图才是最重要。按照设计模式编写的代码，其可读性也会大大提升，利于团队项目的继承和扩展。

## 三、有哪些设计模式？

设计模式可以分为三个大类：创建类设计模式、结构类设计模式、行为类设计模式。创建类设计模式可以分为单例模式、工厂模式、抽象工厂模式、原型模式、建造者模式；结构类设计模式可以分为装饰器模式、适配器模式、门面模式、组合模式、享元模式、桥梁模式；行为类设计模式可以细分为策略模式、责任链模式、命令模式、中介者模式、模板模式、迭代器模式、访问者模式、观察者模式、解释器模式、备忘录模式、状态模式。本课程主要针对这23种设计模式进行基于Python代码的实例学习。
随着现代社会各类业务规模越来越大，挑战越来越多，开源技术不断发展，设计模式也衍生出了很多的新的种类，不局限于这23种，在介绍这些基本的设计模式时，针对些新的“品种”也会简单进行介绍。

## 四、设计模式与架构、框架的关系

### 1、软件框架与设计模式的关系

软件框架随着软件工程的发展而出现，所谓的软件框架，是提取了特定领域的软件的共性部分所形成的软件体系，它并不是一个成熟的软件，而更像是一个“半成品”，程序员在框架之上，可以很方便地某些特定领域实现又快又可靠的二次开发。
设计模式和软件框架在软件设计中是两个不同的研究领域：A、设计模式如前边的定义所讲，它指的是针对一类问题的解决方法，一个设计模式可应用于不同的框架和被不同的语言所实现；而框架则是一个应用的体系结构，是一种或多种设计模式和代码的混合体；B、设计模式相较于框架更容易移植，并且可以用各种语言实现，而软件框架则受限于领域大环境。虽然设计模式和软件框架有很多不同，但在某些方面他们二者是统一的，即重视软件复用，提高开发效率。

### 2、软件架构与设计模式的关系

软件架构是个比较大的概念，架构要考虑软件的整体结构、层次划分以及不同部分间的协作和交互等，架构的着眼点偏整体。相比之下，框架和设计模式的范围则具体很多，框架着眼于领域内的解决方法，而设计模式则针对一类问题的解决方案和设计思路。
总体来说，软件架构可以由不同的框架和不同的设计模式，再加上特定的构件组合来实现；框架可以根据设计模式结合特定编程语言和环境来实现。设计模式就是解决单一问题的设计思路和解决方法。

## 转载来源

[目标](https://yq.aliyun.com/articles/70448)
