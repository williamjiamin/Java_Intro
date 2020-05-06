我们先来看看一个完整的Java程序的基本结构是什么：

```java
/**
 * 乐学偶得（lexueoude.com）原创笔记,公众号：乐学Fintech
 */
public class Hello {
    public static void main(String[] args) {
        // 向屏幕输出文本:
        System.out.println("Hello, Welcome to lexueoude.com");
        /* 多行注释开始
        注释内容
        注释结束 */
    }
} // class定义结束
```

因为Java是面向对象的语言，一个程序的基本单位就是`class`，也就是我们经常说的“类”，所谓“物以类聚”，类代表一系列能实现特定功能的代码，（目前这样理解即可，后续讲解面向对象的时候会进行进一步探讨）`class`是关键字，也就是说在语言中有特定的字是不能被占用的，因为这种语言的设计者对这些关键字进行了特殊的定义。这里定义的`class`名字就是`Hello`：

```java
public class Hello { // 类名是Hello
    // ...
} // class定义结束
```

同样，我们虽然可以将类名进行各种自定义命名，你可以叫Hello，也可以叫Lexueoude，但是，按照广大程序员的统一约定俗成的规矩，一般遵循以下要求：

- 类名必须以英文字母开头，后接字母，数字和下划线的组合
- 习惯以大写字母开头

要注意遵守命名习惯，好的命名非常重要，要不然轻则被同行BS，重则。。。。。自己也看不懂

好的类命名：

- Hello
- MyCon
- VideoPlayer

不好的类命名：

- hello
- Goodgoooooood123123
- _WTFWTF



public`的本意是公共，我们在编程中把它叫做访问修饰符，表示该class是公开的（类比公共厕所，大家都能访问）



当然，不是每一个程序都一定要写`public`，假设我们不写，程序也能正确编译，但是这个类将无法从命令行执行（也就是说不能通过cmd或者终端运行，因为非public，不能访问）。



在`class`内部，可以定义若干方法（method）：

```java
public class Hello {
    public static void main(String[] args) { // 方法名是main
        // 方法代码...
    } // 方法定义结束
}
```



method方法这个名字大家第一次见到一定会觉得有点无厘头，但是我们如果这样想：编程就是要去做一个事情，做一个事情会有相应的“方法”。

我们在这里的方法就是我们定义了一组可以让计算机执行执行语句，这些语句会按照顺序执行。



我们栗子中的方法名是`main`，返回值是`void`，表示没有任何返回值。

我们注意到`public`除了可以修饰`class`外，也可以修饰方法。而关键字`static`是另一个修饰符，它表示静态方法，（其实方法还有好几个类型，目前，我们只需要知道，Java入口程序规定的方法必须是静态方法，方法名必须为`main`，括号内的参数必须是String数组）



方法的名称也有相应的命名规则，我们不要怕命名规则多，其实规则和`class`一样，我们只需要牢记：class的名称首字母小写即可：

好的方法命名：

- main
- goodPerson
- playGame

不好的方法命名：

- Main
- good123
- good_person
- _playGame



当然，我们刚刚之前的都是为真正执行的代码搭建架子，方法内部的语句才是真正的执行代码。

这里我们需要注意：Java的每一行语句必须以分号结束：

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, Welcom to lexueoude.com!"); // 语句
    }
}
```



如果说程序员最讨厌的事情，莫非是写注释和doc文档了——在Java程序中，注释是一种给人阅读的文本（而不是给机器运行执行的命令）。

注释不是程序的一部分，所以编译器会自动忽略注释。

Java有3种注释，第一种是单行注释，以双斜线开头，直到这一行的结尾结束：

```java
// 这是注释...
```

而多行注释以`/*`星号开头，以`*/`结束，可以有多行：

```java
/*
这是注释
blablabla...
这也是注释
*/
```

还有一种特殊的多行注释，以`/**`开头，以`*/`结束，如果有多行，每行通常以星号开头：

```java
/**
 * 可以在这里设置自动创建所有java文件开头的注释
 * 
 * 比如你可以这里写：乐学偶得出品，lexueoude.com
 * 公众号：乐学Fintech
 */
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

这种特殊的多行注释需要写在类和方法的定义处，可以用于自动创建文档doc。



注意：写文档是程序员的一个非常好的习惯，不仅能够让别人看我们代码的时候，代码可读性更强，也可以避免以后自己看到自己代码的时候看不懂（没错，这种情况真的会经常发生）





Java程序对格式没有明确的要求，多几个空格或者回车不影响程序的正确性，但是我们要养成良好的编程习惯，注意遵守Java社区约定的编码格式。

那约定的编码格式有哪些要求呢？其实如果你去查看各种编码格式要求，一定会崩溃——因为一个正常的程序员根本不会记这么多内容。

还好我们有现代IDE给我们解决了统一格式的问题，如果你是用的Intellij IDEA,可以按下option+command+L进行自动排版操作；Eclipse IDE可以按下快捷键`Ctrl+Shift+F`（macOS是`⌘+⇧+F`）就能快速格式化代码的功能，具体的代码格式要求可以在Eclipse的设置中`Java`-`Code Style`查看。
