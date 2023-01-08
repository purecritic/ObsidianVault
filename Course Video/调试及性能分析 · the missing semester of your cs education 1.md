
Topic: the missing semester lecture7
Date: 1月 2, 2023
Course:the missing semester lecture7
Class:

---

### Body
## Lecture 7: Debugging and Profiling (2020)

Time

Subtitle

Machine Translation

>👇[0s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=0)

So welcome back. Today we are gonna cover debugging and profiling.

欢迎回来。 今天我们将 介绍调试和分析。

>👇[4s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=4)

Before I get into it we're gonna make another reminder to fill in the survey.

在开始之前，我们将再次 提醒您填写调查问卷。

>👇[9s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=9)

Just one of the main things we want to get from you is questions, because the last day

我们想从你们那里得到的主要事情之一 就是问题，因为最后一天

>👇[14s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=14)

is gonna be questions from you guys: about things that

将是你们的问题 ：关于

>👇[18s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=18)

we haven't covered, or like you want us to kind of talk more in depth.

我们没有涉及的事情，或者你们希望 我们更深入地讨论。

>👇[23s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=23)

The more questions we get, the more interesting we can make that section,

我们收到的问题越多，该部分就越有趣 ，

>👇[26s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=26)

so please go on and fill in the survey.

所以请继续填写调查。

>👇[28s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=28)

So today's lecture is gonna be a lot of topics. All the topics revolve around the concept of

所以今天的讲座会涉及很多话题。 所有的主题都围绕着

>👇[35s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=35)

what do you do when you have a program that has some bugs.

当你 的程序有一些错误时你会怎么做的概念。

>👇[39s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=39)

Which is most of the time, like when you are programming, you're kind of thinking

大多数时候，就像当你 在编程时，你正在

>👇[42s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=42)

about how you implement something and there's like a half life of fixing all the issues that

考虑如何实现某些东西，并且 解决该程序存在的所有问题就像是半衰期

>👇[47s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=47)

that program has. And even if your program behaves like you want, it might be that it's

。 即使你的程序表现得 如你所愿，也可能是

>👇[52s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=52)

really slow, or it's taking a lot of resources in the process.

它真的很慢，或者 在这个过程中占用了大量资源。

>👇[55s](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=55)

So today we're gonna see a lot of different approaches of dealing with these problems.

所以今天我们将看到许多 处理这些问题的不同方法。

>👇[1:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=61)

So first, the first section is on debugging.

所以首先，第一部分是调试。

>👇[1:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=66)

Debugging can be done in many different ways,

调试可以通过许多不同的方式完成，

>👇[1:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=68)

there are all kinds of...

有各种各样的

>👇[1:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=70)

The most simple approach that, pretty much, all

...最简单的方法，几乎​​所有

>👇[1:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=73)

CS students will go through, will be just: you have some code, and it's not behaving

CS 学生都会经历，只是： 你有一些代码，但它的行为

>👇[1:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=77)

like you want, so you probe the code by adding

不像你想要的那样， 所以你通过添加

>👇[1:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=80)

print statements. This is called "printf debugging" and

打印语句来探测代码。 这称为 “printf 调试”

>👇[1:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=83)

it works pretty well.

，效果很好。

>👇[1:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=84)

Like, I have to be honest,

就像，老实说，我经常

>👇[1:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=86)

I use it a lot of the time because of how simple to set up and how quick the feedback can be.

使用它，因为它 设置起来很简单，反馈也很快。

>👇[1:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=94)

One of the issues with printf debugging is that you can get a lot of output

printf 调试的问题之一 是您可以获得大量输出，

>👇[1:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=99)

and maybe you don't want

并且您可能不

>👇[1:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=100)

to get as much output as you're getting.

希望获得尽可能多的输出。

>👇[1:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=103)

There has... people have thought of slightly more complex ways of doing printf debugging and

有...人们想到了稍微 复杂的 printf 调试方法，

>👇[1:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=113)

one of these ways is what is usually referred to as "logging".

其中一种方法通常 被称为“日志记录”。

>👇[1:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=118)

So the advantage of doing logging versus doing printf debugging is that, when you're creating logs,

因此，与 printf 调试相比，进行日志记录的优势 在于，当您创建日志时，

>👇[2:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=125)

you're not necessarily creating the logs because there's a specific issue you want to fix;

您不一定会创建日志，因为 有一个特定的问题需要修复；

>👇[2:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=129)

it's mostly because you have built a

这主要是因为您构建了一个

>👇[2:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=132)

more complex software system and you want to log when some events happen.

更复杂的软件系统，并且您 想在某些事件发生时进行记录。

>👇[2:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=137)

One of the core advantages of using a logging library is that

使用日志库的核心优势之一是

>👇[2:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=142)

you can can define severity levels, and you can filter based on those.

您可以定义严重级别， 并且可以基于这些级别进行过滤。

>👇[2:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=147)

Let's see an example of how we can do something like that.

让我们看一个例子，说明我们 如何做这样的事情。

>👇[2:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=152)

Yeah, everything fits here. This is a really silly example:

是的，一切都适合这里。 这 是一个非常愚蠢的例子：

>👇[2:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=156)

We're just gonna

我们只是要对

>👇[2:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=157)

sample random numbers and, depending on the value of the number,

随机数进行采样，并且根据数字 的值

>👇[2:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=161)

that we can interpret as a kind of "how wrong things are going".

，我们可以将其解释为 一种“事情进展得如何”。

>👇[2:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=164)

We're going to log the value of the number and then

我们将记录数字的 值，然后

>👇[2:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=169)

we can see what is going on.

我们可以看到发生了什么。

>👇[2:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=172)

I need to disable these formatters...

我需要禁用这些格式化程序

>👇[2:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=179)

And if we were just to execute the code as it is,

……如果我们只是按原样执行代码，

>👇[3:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=184)

we just get the output and we just keep getting more and more output.

我们只会得到输出，而且我们只会 不断得到越来越多的输出。

>👇[3:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=187)

But you have to kind of stare at it and make sense of what is going on, and we don't know

但是你必须盯着它看，才能 理解发生了什么，我们不知道

>👇[3:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=193)

what is the relative timing between printfs, we don't really know whether this is just an information message

printfs 之间的相对时间是什么，我们真的不 知道这只是一条信息消息

>👇[3:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=199)

or a message of whether something went wrong.

还是一条消息 出了些问题。

>👇[3:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=203)

If we just go in,

如果我们只是进入

>👇[3:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=207)

and undo, not that one...

并撤消，而不是那个……

>👇[3:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=214)

That one, we can set that formatter.

那个，我们可以设置那个格式化程序。

>👇[3:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=218)

Now the output looks something more like this

现在输出看起来更像

>👇[3:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=221)

So for example, if you have several different modules that you are programming with,

这样 例如，如果您有几个不同的 模块用于编程，

>👇[3:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=224)

you can identify them with like different levels.

您可以用不同的级别来识别它们。

>👇[3:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=226)

Here, we have, we have debug levels,

在这里，我们有，我们有调试级别，

>👇[3:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=230)

we have critical

我们有关键

>👇[3:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=231)

info, different levels. And it might be handy because here we might only care about the error messages.

信息，不同级别。 它可能很方便，因为 在这里我们可能只关心错误消息。

>👇[3:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=237)

Like those are like, the... We have been

就像那些一样，......我们一直

>👇[4:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=240)

working on our code, so far so good, and suddenly we get some error.

在研究我们的代码，到目前为止 一切顺利，突然我们遇到了一些错误。

>👇[4:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=243)

We can log that to identify where it's happening.

我们可以记录它以确定发生的位置。

>👇[4:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=246)

But maybe there's a lot of information messages, but we can deal with that

但也许有很多信息 消息，但我们可以

>👇[4:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=252)

by just changing the level to error level.

通过将级别更改为错误级别来处理。

>👇[4:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=257)

And

-

>👇[4:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=258)

now if we were to run this again, we are only going to get those

现在，如果我们再次运行它， 我们只会

>👇[4:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=263)

errors in the output, and we can just look through those to make sense of what is going on.

在输出中得到这些错误，我们可以通过查看 这些错误来了解发生了什么。

>👇[4:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=268)

Another really useful tool when you're dealing with logs is

当你处理日志时，另一个非常有用的工具 是

>👇[4:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=274)

As you kind of look at this,

当你看这个时，

>👇[4:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=276)

it has become easier because now we have this critical and error levels that we can quickly identify.

它变得更容易了，因为现在我们有了 可以快速识别的关键和错误级别。

>👇[4:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=283)

But since humans are fairly visual creatures,

但是由于人类是相当视觉化的生物，

>👇[4:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=288)

one thing that you can do is use colors from your terminal to

您可以做的一件事就是使用 终端中的颜色来

>👇[4:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=293)

identify these things. So now, changing the formatter,

识别这些东西。 所以现在， 更改格式化程序，

>👇[4:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=297)

what I've done is slightly change how the output is formatted.

我所做的只是稍微 更改输出的格式化方式。

>👇[5:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=303)

When I do that, now whenever I get a warning message, it's color coded by yellow;

当我这样做时，现在每当我收到一条警告 消息时，它的颜色编码为黄色；

>👇[5:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=309)

whenever I get like an error,

每当我遇到错误时，就会

>👇[5:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=310)

faded red; and when it's critical, I have a bold red indicating something went wrong.

变红； 当它很关键时，我有一个 粗体红色表示出了问题。

>👇[5:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=316)

And here it's a really short output, but when you start having thousands and thousands of lines of log,

这是一个非常短的输出，但是当您开始 拥有成千上万行日志时，

>👇[5:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=322)

which is not unrealistic and happens every single day in a lot of apps,

这并非不切实际并且 每天都在很多应用程序中发生，

>👇[5:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=327)

quickly browsing through them and identifying where the error or the red patches are

快速浏览它们并 确定错误或红色补丁的位置

>👇[5:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=332)

can be really useful.

真的很有用。

>👇[5:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=335)

A quick aside is, you might be curious about how the terminal is displaying these colors.

顺便说一句，您可能 对终端如何显示这些颜色感到好奇。

>👇[5:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=341)

At the end of the day, the terminal is only outputting characters.

在一天结束时， 终端只输出字符。

>👇[5:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=347)

Like, how is this program or how are other programs, like LS,

比如，这个程序怎么样，或者 其他程序怎么样，比如 LS

>👇[5:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=350)

that has all these fancy colors. How are they telling the terminal that it should use these different colors?

，有所有这些花哨的颜色。 他们如何告诉 终端它应该使用这些不同的颜色？

>👇[5:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=356)

This is nothing extremely fancy,

这没什么特别的

>👇[5:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=359)

what these tools are doing, is something along these lines.

，这些工具正在做的 就是这些。

>👇[6:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=363)

Here we have...

这里我们有...

>👇[6:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=365)

I can clear the rest of the output, so we can focus on this.

我可以清除其余的输出， 所以我们可以专注于此。

>👇[6:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=368)

There's some special characters, some escape characters here,

这里有一些特殊字符， 一些转义字符，

>👇[6:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=374)

then we have some text and then we have some other special characters. And if we execute this line

然后我们有一些文本，然后我们有一些其他 特殊字符。 如果我们执行这一行，

>👇[6:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=379)

we get a red "This is red".

我们会得到一个红色的“This is red”。

>👇[6:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=382)

And you might have picked up on the fact that we have a "255;0;0" here,

你可能已经 注意到我们这里有一个“255;0;0”，

>👇[6:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=386)

this is just telling the RGB values of the color we want in the terminal.

这只是告诉 终端我们想要的颜色的 RGB 值。

>👇[6:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=391)

And you pretty much can do this in any piece of code that you have, and like that you can color code the output.

你几乎可以在任何你拥有的代码中做到这一点 ，并且你可以像这样对输出进行颜色编码。

>👇[6:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=398)

Your terminal is fairly fancy and supports a lot of different colors in the output.

您的终端相当花哨，并且 在输出中支持许多不同的颜色。

>👇[6:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=402)

This is not even all of them, this is like a sixteenth of them.

这还不是他们的全部， 这像是他们的十六分之一。

>👇[6:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=406)

I think it can be fairly useful to know about that.

我认为了解这一点非常 有用。

>👇[6:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=412)

Another thing is maybe you don't enjoy or you don't think

另一件事是您可能不 喜欢或者您认为

>👇[6:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=416)

logs are really fit for you.

原木真的不适合您。

>👇[6:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=418)

The thing is a lot of other systems that you might start using will use logs.

问题是 您可能开始使用的许多其他系统都将使用日志。

>👇[7:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=422)

As you start building larger and larger systems,

当您开始构建越来越大的系统时，

>👇[7:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=425)

you might rely on other dependencies. Common dependencies might be web servers or

您可能会依赖其他依赖项。 常见的 依赖项可能是 Web 服务器或

>👇[7:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=430)

databases, it's a really common one.

数据库，这是一个非常常见的依赖项。

>👇[7:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=432)

And those will be logging their errors or exceptions in their own logs.

那些将 在他们自己的日志中记录他们的错误或异常。

>👇[7:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=437)

Of course, you will get some client-side error,

当然，您会收到一些客户端错误，

>👇[7:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=440)

but those sometimes are not informative enough for you to figure out what is going on.

但有时这些错误信息不足以 让您弄清楚发生了什么。

>👇[7:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=445)

In most UNIX systems, the logs are usually placed under a folder called "/var/log"

在大多数 UNIX 系统中，日志通常 放在一个名为“/var/log”的文件夹下

>👇[7:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=453)

and if we list it, we can see there's a bunch of logs in here.

，如果我们列出它，我们可以看到 这里有一堆日志。

>👇[7:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=462)

So we have like the shutdown monitor log, or some weekly logs.

所以我们有关闭监控 日志，或一些每周日志。

>👇[7:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=469)

Things related to the Wi-Fi, for example. And if we output the

例如，与 Wi-Fi 相关的事情 。 而如果我们输出

>👇[7:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=477)

System log, which contains a lot of information about the system,

系统日志，里面包含了 很多关于系统的信息，

>👇[8:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=480)

we can get information about what's going on.

我们就可以得到关于发生了什么的信息。

>👇[8:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=484)

Similarly, there are tools that will let you

同样，有一些工具可以让您

>👇[8:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=487)

more sanely go through this output. But here, looking at the system log,

更理智地查看此输出。 但是在这里，查看系统日志，

>👇[8:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=493)

I can look at this, and say:

我可以看看这个，然后说：

>👇[8:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=495)

oh there's some service that is exiting with some abnormal code

哦，有一些服务正在 退出，并带有一些异常代码

>👇[8:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=500)

and based on that information, I can go and try to figure out what's going on,

，根据这些信息，我可以 去尝试弄清楚发生了什么，

>👇[8:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=505)

like what's going wrong.

比如发生了什么 错误的。

>👇[8:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=509)

One thing to know when you're working with logs is that

当您使用日志时要知道的一件事 是，

>👇[8:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=512)

more traditionally, every software had their own

更传统地说，每个软件都有自己的

>👇[8:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=515)

log, but it has been increasingly more popular to have a unified system log where everything is placed.

日志，但是拥有 一个统一的系统日志来放置所有内容越来越受欢迎。

>👇[8:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=523)

Pretty much any application can log into the system log, but instead of being in a plain text format,

几乎任何应用程序都可以登录系统 日志，但它不是纯文本格式，

>👇[8:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=529)

it will be compressed in some special format.

而是以某种特殊格式进行压缩。

>👇[8:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=532)

An example of this, it was what we covered in the data wrangling lecture.

这方面的一个例子，就是我们 在数据争论讲座中介绍的内容。

>👇[8:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=536)

In the data wrangling lecture we were using the "journalctl",

在数据争论讲座中， 我们使用了“journalctl”，

>👇[9:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=540)

which is accessing the log and outputting all that output.

它正在访问日志并 输出所有输出。

>👇[9:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=544)

Here in Mac, now the command is "log show",

在 Mac 中，现在的命令是“log show”，

>👇[9:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=547)

which will display a lot of information.

它会显示很多信息。

>👇[9:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=550)

I'm gonna just display the last ten seconds, because logs are really, really verbose and

我只显示最后 10 秒， 因为日志真的非常冗长，

>👇[9:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=557)

just displaying the last 10 seconds is still gonna output a fairly large amount of lines.

只显示最后 10 秒仍然 会输出相当多的行。

>👇[9:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=563)

So if we go back through what's going on,

因此，如果我们回顾发生的事情，

>👇[9:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=568)

we here see that a lot of Apple things are going on, since this is a macbook.

我们会看到很多 Apple 的事情 正在发生，因为这是一台 macbook。

>👇[9:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=573)

Maybe we could find errors about like some system issue here.

也许我们可以 在这里找到一些系统问题的错误。

>👇[9:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=579)

Again they're fairly verbose, so you might want to practice your data wrangling techniques here,

同样，它们相当冗长，所以您可能想 在这里练习您的数据整理技术，

>👇[9:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=586)

like 10 seconds equal to like 500 lines of logs, so you can kind of

比如 10 秒等于 500 行日志，这样您就

>👇[9:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=590)

get an idea of how many lines per second you're getting.

可以大致了解每秒获得多少行 。

>👇[9:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=596)

They're not only useful for figuring out some other programs' output,

它们不仅可用于 计算其他程序的输出

>👇[10:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=601)

they're also useful for you, if you want to log there instead of into your own file.

，如果您想在 那里登录而不是登录到您自己的文件中，它们对您也很有用。

>👇[10:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=605)

So using the "logger" command, in both linux and mac,

所以在 linux 和 mac 中使用“logger”命令，

>👇[10:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=611)

You can say okay

你可以说好吧，

>👇[10:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=613)

I'm gonna log this "Hello Logs" into this system log.

我要把这个“Hello Logs”记录 到这个系统日志中。

>👇[10:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=618)

We execute the command and then

我们执行命令，然后

>👇[10:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=622)

we can check by going through the last minute of logs,

我们可以通过查看 最后一分钟的日志来检查，

>👇[10:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=627)

since it's gonna be fairly recent, and grepping for that "Hello"

因为它是相当新的， 并且通过搜索“Hello”

>👇[10:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=631)

we find our entry. Fairly recent entry, that we just created that said "Hello Logs".

我们找到了我们的条目。 相当新的条目， 我们刚刚创建，上面写着“Hello Logs”。

>👇[10:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=639)

As you become more and more familiar with these tools, you will find yourself using

随着你越来越熟悉 这些工具，你会发现自己

>👇[10:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=648)

the logs more and more often, since

越来越频繁地使用日志，因为

>👇[10:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=651)

even if you have some bug that you haven't detected, and the program has been running for a while,

即使你有一些你没有检测到的错误， 并且程序已经运行了一段时间，

>👇[10:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=656)

maybe the information is already in the log and can tell you enough to figure out what is going on.

也许信息 已经在日志中，可以 告诉您足够的信息来弄清楚发生了什么。

>👇[11:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=662)

However, printf debugging is not everything. So now I'm going to be covering debuggers.

然而，printf 调试并不是一切。 所以现在我将介绍调试器。

>👇[11:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=668)

But first any questions on logs so far?

但首先，到目前为止对日志有什么问题吗？

>👇[11:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=671)

So what kind of things can you figure out from the logs?

那么你能从日志中找出什么样的东西 呢？

>👇[11:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=675)

like this Hello Logs says that you did something with Hello at that time?

像这样 Hello Logs 说你 当时用 Hello 做了什么？

>👇[11:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=678)

Yeah, like say, for example, I can write a bash script that detects...

是的，比如说，例如，我可以 编写一个 bash 脚本来检测……

>👇[11:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=685)

Well, that checks every time what Wi-Fi network I'm connected to.

嗯，每次 我连接到哪个 Wi-Fi 网络时都会检查它。

>👇[11:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=689)

And every time it detects that it has changed, it makes an entry in the logs and says

每次它检测到它发生变化时， 它都会在日志中记录一个条目并说

>👇[11:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=694)

Oh now it looks like we have changed Wi-Fi networks.

哦，现在看起来我们已经 改变了 Wi-Fi 网络。

>👇[11:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=697)

and then you might go back and parse through the logs and take like, okay

然后你可能会返回并 分析日志，然后想，

>👇[11:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=701)

When did my computer change from one Wi-Fi network to another. And this is just kind of a simple example

好吧，我的电脑什么时候从一个 Wi-Fi 网络切换到 另一个。 这只是一个简单的示例，

>👇[11:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=707)

But there are many, many ways,

但是您可以通过多种方式在此处记录

>👇[11:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=710)

many types of information that you could be logging here.

多种类型的信息 。

>👇[11:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=714)

More commonly, you will probably want to check if your computer, for example, is

更常见的是，您可能想要 检查您的计算机是否正在

>👇[11:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=719)

entering sleep, for example, for some unknown reason.

进入睡眠状态，例如， 出于某种未知原因。

>👇[12:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=722)

Like it's on hibernation mode.

就像它处于休眠模式一样。 日志

>👇[12:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=724)

There's probably some information in the logs about who asked that to happen,

中可能有一些 关于谁要求发生这种情况的信息，

>👇[12:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=729)

or why it's that happening.

或者为什么会发生这种情况。

>👇[12:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=731)

Any other questions? Okay.

还有其他问题吗？ 好的。

>👇[12:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=734)

So when printf debugging is not enough,

因此，当 printf 调试不够时

>👇[12:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=738)

the best alternative after that is using...

，最好的替代方法是使用...

>👇[12:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=743)

[Exit that]

[退出]

>👇[12:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=748)

So, it's using a debugger.

所以，它正在使用调试器。

>👇[12:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=750)

So a debugger is a tool that will wrap around your code and will let you run your code,

所以调试器是一种工具，可以环绕 你的代码并让你运行你的代码，

>👇[12:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=758)

but it will kind of keep control over it.

但它会保持对它的控制。

>👇[12:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=760)

So it will let you step

所以它会让你单

>👇[12:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=762)

through the code and execute it and set breakpoints.

步执行代码并执行 它并设置断点。

>👇[12:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=767)

You probably have seen debuggers in some way, if you have

如果您

>👇[12:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=770)

ever used something like an IDE, because IDEs have this kind of fancy: set a breakpoint here, execute, ...

曾经使用过类似 IDE 的东西，您可能已经以某种方式看到过调试器，因为 IDE 有 这种奇特的功能：在此处设置断点，执行，...

>👇[12:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=776)

But at the end of the day what these tools are using is just

但归根结底， 这些工具使用的是 只是

>👇[12:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=779)

these command line debuggers and they're just presenting them in a really fancy format.

这些命令行调试器，它们只是 以一种非常奇特的格式呈现它们。

>👇[13:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=784)

Here we have a completely broken bubble sort, a simple sorting algorithm.

这里我们有一个完全破坏的冒泡 排序，一个简单的排序算法。

>👇[13:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=790)

Don't worry about the details,

不要担心细节，

>👇[13:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=791)

but we just want to sort this array that we have here.

但我们只想对 我们这里的这个数组进行排序。

>👇[13:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=797)

We can try doing that by just doing

我们可以通过执行 Python bubble.py 来尝试做到这

>👇[13:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=801)

Python bubble.py

一点

>👇[13:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=803)

And when we do that... Oh there's some index error, list index out of range.

当我们这样做时......哦有一些 索引错误，列表索引超出范围。

>👇[13:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=808)

We could start adding prints

我们可以开始添加印刷品，

>👇[13:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=811)

but if have a really long string, we can get a lot of information.

但如果有很长的字符串， 我们可以获得很多信息。

>👇[13:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=813)

So how about we go up to the moment that we crashed?

那么我们如何回到 我们坠毁的那一刻？

>👇[13:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=817)

We can go to that moment and examine what the

我们可以回到那一刻，检查

>👇[13:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=821)

current state of the program was.

程序的当前状态。

>👇[13:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=823)

So for doing that I'm gonna run the program using the Python debugger.

为此，我将 使用 Python 调试器运行该程序。

>👇[13:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=829)

Here I'm using technically the ipython debugger, just because it has nice coloring syntax

在这里，我在技术上使用 ipython 调试器， 只是因为它有很好的着色语法，

>👇[13:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=834)

so it's probably easier for both of us to understand

所以我们俩可能更 容易理解

>👇[13:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=839)

what's going on in the output.

输出中发生的事情。

>👇[14:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=841)

But they're pretty much identical anyway.

但无论如何，它们几乎完全相同。

>👇[14:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=845)

So we execute this, and now we are given a prompt

所以我们执行这个，现在我们在程序的第一行得到一个提示

>👇[14:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=849)

where we're being told that we are here, at the very first line of our program.

，告诉我们我们在这里 。

>👇[14:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=853)

And we can...

我们可以...

>👇[14:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=855)

"L" stands for "List", so as with many of these tools

“L”代表“列表”，因此 对于许多这些工具

>👇[14:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=861)

there's kind of like a language of operations that you can do,

，您可以使用一种类似操作的语言，

>👇[14:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=864)

and they are often mnemonic, as it was the case with VIM or TMUX.

并且它们通常是助记符， 就像 VIM 或 TMUX 的情况一样 .

>👇[14:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=868)

So here, "L" is for "Listing" the code, and we can see the entire code.

所以在这里，“L”代表“Listing”代码 ，我们可以看到完整的代码。

>👇[14:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=874)

"S" is for "Step" and will let us kind of one

“S”代表“Step”，让我们

>👇[14:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=878)

line at a time, go through the execution.

一次一行，完成执行。

>👇[14:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=882)

The thing is we're only triggering the error some time later.

问题是我们只是 在一段时间后才触发错误。

>👇[14:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=887)

So

所以

>👇[14:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=888)

we can restart the program and instead of trying to step until we get to the issue,

我们可以重新启动程序，而不是 尝试逐步解决问题，

>👇[14:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=895)

we can just ask for the program to continue which is the "C" command and

我们可以只要求程序继续 ，这是“C”命令，

>👇[15:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=901)

hey, we reached the issue.

嘿，我们解决了问题。

>👇[15:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=904)

We got to this line where everything crashed,

我们到了这一行，一切都崩溃了，

>👇[15:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=908)

we're getting this list index out of range.

我们让这个列表索引超出了范围。

>👇[15:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=911)

And now that we are here we can say, huh?

既然我们在这里，我们可以说，嗯？

>👇[15:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=914)

Okay, first, let's print the value of the array.

好的，首先，让我们打印数组的值。

>👇[15:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=918)

This is the value of the current array

这是当前数组的值

>👇[15:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=923)

So we have six items. Okay. What is the value of "J" here?

所以我们有六个项目。 好的。 这里“J”的值是多少？

>👇[15:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=927)

So we look at the value of "J". "J" is 5 here, which will be the last element, but

所以我们看“J”的值。 “J” 在这里是 5，这将是最后一个元素，但是

>👇[15:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=932)

"J" plus 1 is going to be 6, so that's triggering the out of bounds error.

“J”加 1 将是 6，所以这会 触发越界错误。

>👇[15:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=937)

So what we have to do is

所以我们要做的就是

>👇[15:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=940)

this "N", instead of "N" has to be "N minus one". We have identified that the error lies there.

这个“N”，而不是“N”必须是“N减一”。 我们已经确定错误就在那里。

>👇[15:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=947)

So we can quit, which is "Q".

所以我们可以退出，也就是“Q”。

>👇[15:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=952)

Again, because it's a post-mortem debugger.

同样，因为它是一个事后调试器。

>👇[15:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=956)

We go back to the code and say okay,

我们回到代码并说好的，

>👇[16:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=962)

we need to append this "N minus one".

我们需要附加这个“N减一”。

>👇[16:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=966)

That will prevent the list index out of range and

这将防止列表索引超出范围，

>👇[16:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=971)

if we run this again without the debugger,

如果我们在没有调试器的情况下再次运行它，

>👇[16:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=975)

okay, no errors now. But this is not our sorted list.

好的，现在没有错误。 但这 不是我们的排序列表。

>👇[16:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=978)

This is sorted, but it's not our list.

这是排序的，但它不是我们的列表。

>👇[16:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=981)

We are missing entries from our list,

我们的列表中缺少条目，

>👇[16:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=983)

so there is some behavioral issue that we're reaching here.

因此我们遇到了一些行为问题 。

>👇[16:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=987)

Again, we could start using printf debugging but kind of a hunch now

同样，我们可以开始使用 printf 调试，但现在

>👇[16:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=992)

is that probably the way we're swapping entries in the bubble sort program is wrong.

有一种预感是我们 在冒泡排序程序中交换条目的方式可能是错误的。

>👇[16:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=998)

We can use the debugger for this. We can go through them to the moment we're doing a swap and

我们可以为此使用调试器。 我们可以通过 它们直到我们进行交换的那一刻，并

>👇[16:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1006)

check how the swap is being performed.

检查交换是如何执行的。

>👇[16:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1008)

So a quick overview,

快速概览

>👇[16:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1010)

we have two for loops and in the most nested loop,

一下，我们有两个 for 循环， 在最嵌套的循环中，

>👇[16:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1016)

we are checking if the array is larger than the other array. The thing is if we just try to execute until this line,

我们检查数组是否大于另一个数组。 问题是如果我们只是尝试执行到这一行，

>👇[17:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1023)

it's only going to trigger whenever we make a swap.

它只会 在我们进行交换时触发。

>👇[17:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1026)

So what we can do is we can set a breakpoint in the sixth line.

所以我们能做的就是 在第六行设置一个断点。

>👇[17:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1031)

We can create a breakpoint in this line and then

我们可以在这一行中创建一个断点，

>👇[17:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1035)

the program will execute and the moment we try to swap variables is when the program is going to stop.

然后程序将执行，我们尝试交换 变量的那一刻就是程序将要停止的时候。

>👇[17:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1041)

So we create a breakpoint there

所以我们在那里创建一个断点

>👇[17:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1042)

and then we continue the execution of the program. The program halts

，然后我们继续 执行程序。 程序停止

>👇[17:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1047)

and says hey, I have executed and I have reached this line.

并说嘿，我已经执行 并到达了这一行。

>👇[17:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1050)

Now

现在

>👇[17:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1051)

I can use "locals()", which is a Python function that returns a dictionary with all the values

我可以使用“locals()”，这是一个 Python 函数 ，它返回一个包含所有值的字典

>👇[17:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1059)

to quickly see the entire context.

以快速查看整个上下文。

>👇[17:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1063)

The string, the array is fine and is six, again, just the beginning and

字符串，数组很好，是 六个，再次，只是开始，

>👇[17:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1068)

I step, go to the next line.

我一步，转到下一行。

>👇[17:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1071)

Oh,

哦

>👇[17:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1072)

and I identify the issue: I'm swapping one item at a time, instead of simultaneously,

，我确定了问题所在：我一次交换一个 项目，而不是同时交换，

>👇[17:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1077)

so that's what's triggering the fact that we're losing variables as we go through.

所以这就是触发 我们在经历过程中丢失变量的事实。

>👇[18:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1083)

That's kind of a very simple example, but

这是一个非常简单的例子，但

>👇[18:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1087)

debuggers are really powerful.

调试器真的很强大。

>👇[18:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1089)

Most programming languages will give you some sort of debugger,

大多数编程语言都会 为您提供某种调试器

>👇[18:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1093)

and when you go to more low level debugging you might run into tools like...

，当您进行更底层的调试时， 您可能会遇到诸如...之类的工具。

>👇[18:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1099)

You might want to use something like

您可能想使用

>👇[18:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1105)

GDB.

GDB 之类的东西。

>👇[18:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1111)

And GDB has one nice property:

GDB 有一个很好的特性：

>👇[18:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1114)

GDB works really well with C/C++ and all these C-like languages.

GDB 与 C/C++ 和所有这些类 C 语言一起工作得非常好。

>👇[18:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1117)

But GDB actually lets you work with pretty much any binary that you can execute.

但 GDB 实际上允许您使用 几乎任何您可以执行的二进制文件。

>👇[18:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1122)

So for example here we have sleep, which is just a program that's going to sleep for 20 seconds.

因此，例如这里我们有睡眠，这只是 一个将睡眠 20 秒的程序。

>👇[18:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1128)

It's loaded and then we can do run, and then we can interrupt this sending an interrupt signal.

它被加载，然后我们可以运行，然后我们 可以中断它发送一个中断信号。

>👇[18:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1135)

And GDB is displaying for us, here, very low-level information about what's going on in the program.

GDB 在这里为我们显示了 关于程序中正在发生的事情的非常低级的信息。

>👇[19:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1142)

So we're getting the stack trace, we're seeing we are in this nanosleep function,

所以我们得到了堆栈跟踪，我们看到 我们在这个 nanosleep 函数中，

>👇[19:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1147)

we can see the values of all the hardware registers in your machine. So

我们可以看到你机器中所有硬件 寄存器的值。 因此，

>👇[19:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1152)

you can get a lot of low-level detail using these tools.

您可以 使用这些工具获得很多底层细节。

>👇[19:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1158)

I think that's all I want to cover for debuggers.

我想这就是我想为调试器介绍的全部内容。

>👇[19:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1162)

Any questions related to that?

有什么相关的问题吗？

>👇[19:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1173)

Another interesting tool when you're trying to debug is that sometimes you want to debug as if

当您尝试调试时，另一个有趣的工具 是有时您想要调试，就好像

>👇[19:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1179)

your program is a black box.

您的程序是一个黑盒子一样。

>👇[19:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1182)

So you, maybe, know what the internals of the program but at the same time

因此，您也许知道 程序的内部结构，但同时

>👇[19:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1186)

your computer knows whenever your program is trying to do some operations.

您的计算机知道您的程序 何时尝试执行某些操作。

>👇[19:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1192)

So this is in UNIX systems,

所以这是在 UNIX 系统中，

>👇[19:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1194)

there's this notion of like user level code and kernel level code.

有类似用户 级代码和内核级代码的概念。

>👇[19:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1198)

And when you try to do some operations like reading a file or like reading the network connection

当您尝试执行某些操作（如 读取文件或读取网络连接）时，

>👇[20:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1203)

you will have to do something called system calls.

您将不得不执行 称为系统调用的操作。

>👇[20:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1206)

You can get a program and go through those operations and ask

你可以拿一个程序，把 那些操作过一遍，问问

>👇[20:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1214)

what operations did this software do?

这个软件做了什么操作？

>👇[20:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1218)

So for example, if you have like a Python function

因此，例如，如果您 有一个 Python 函数

>👇[20:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1220)

that is only supposed to do a mathematical operation and you run it through this program,

，它只应该执行数学运算， 并且您通过该程序运行它，

>👇[20:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1226)

and it's actually reading files,

并且它实际上正在读取文件，

>👇[20:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1228)

Why is it reading files? It shouldn't be reading files. So, let's see.

为什么它正在读取文件？ 它不 应该读取文件。 那么，让我们看看。

>👇[20:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1234)

This is "strace".

这是“痕迹”。

>👇[20:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1237)

So for example, we can do it something like this.

因此，例如，我们可以这样做。

>👇[20:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1238)

So here we're gonna run the "LS - L"

所以在这里我们要运行“LS - L

>👇[20:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1242)

And then we're ignoring the output of LS, but we are not ignoring the output of STRACE.

” 然后我们忽略 LS 的输出，但 我们不会忽略 STRACE 的输出。

>👇[20:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1247)

So if we execute that...

所以如果我们执行那个……

>👇[20:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1252)

We're gonna get a lot of output.

我们会得到很多输出。

>👇[20:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1254)

This is all the different system calls

这是这个 LS 执行的所有不同的系统调用

>👇[21:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1260)

That this

-

>👇[21:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1262)

LS has executed. You will see a bunch of OPEN, you will see FSTAT.

。 你会看到 一堆OPEN，你会看到FSTAT。

>👇[21:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1268)

And for example, since it has to list all the properties of the files that are in this folder, we can

例如，由于它必须 列出此文件夹中文件的所有属性，我们可以

>👇[21:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1275)

check for the LSTAT call. So the LSTAT call will check for the properties of the files and

检查 LSTAT 调用。 所以 LSTAT 调用将 检查文件的属性，

>👇[21:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1281)

we can see that, effectively, all the files and folders that are in this directory

我们可以看到，实际上， 该目录中的所有文件和文件夹都已

>👇[21:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1287)

have been accessed through a system call, through LS.

通过系统调用通过 LS 访问过。

>👇[21:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1294)

Interestingly, sometimes you actually don't need to run your code to

有趣的是，有时您实际上 不需要运行您的代码就可以发现您的代码

>👇[21:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1304)

figure out that there is something wrong with your code.

有 问题。

>👇[21:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1307)

So far we have seen enough ways of identifying issues by running the code,

到目前为止，我们已经看到了足够多的 通过运行代码来识别问题的方法，

>👇[21:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1312)

but what if you...

但是如果你......

>👇[21:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1314)

you can look at a piece of code like this, like the one I have shown right now in this screen,

你可以查看一段这样的代码， 就像我现在在这个屏幕上显示的那样，

>👇[21:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1318)

and identify an issue.

并识别问题。

>👇[22:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1320)

So for example here,

因此，例如在这里，

>👇[22:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1322)

we have some really silly piece of code. It defines a function, prints a few variables,

我们有一些非常愚蠢的代码。 它 定义了一个函数，打印了一些变量，

>👇[22:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1327)

multiplies some variables, it sleeps for a while and then we try to print BAZ.

将一些变量相乘，它休眠 了一会儿，然后我们尝试打印 BAZ。

>👇[22:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1332)

And you could try to look at this and say, hey, BAZ has

你可以试着看看 这个，然后说，嘿，BAZ

>👇[22:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1335)

never been defined anywhere. This is a new variable. You probably meant to say BAR

从来没有在任何地方定义过。 这是一个新 变量。 您可能想说 BAR，

>👇[22:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1340)

but you just mistyped it.

但您打错了。

>👇[22:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1342)

Thing is, if we try to run this program,

问题是，如果我们尝试运行这个程序，

>👇[22:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1348)

it's gonna take 60 seconds, because like we have to wait until this time.sleep function finishes. Here, sleep is just for

它将需要 60 秒，因为我们必须等到 这个时间。sleep 函数完成。 在这里，sleep 只是为了

>👇[22:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1357)

motivating the example but in general you may be loading a data set that takes really long

激发示例，但通常您可能 会加载一个需要很长时间的数据集，

>👇[22:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1362)

because you have to copy everything into memory.

因为您必须将所有内容复制到内存中。

>👇[22:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1364)

And the thing is, there are programs that will take source code as input,

问题是，有些 程序会将源代码作为输入，对其

>👇[22:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1369)

will process it and will say, oh probably this is wrong about this piece of code. So in Python,

进行处理，然后说，哦，这段代码可能是 错误的。 所以在 Python 中，

>👇[22:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1375)

or in general, these are called static analysis tools.

或者一般来说，这些被称为 静态分析工具。

>👇[23:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1380)

In Python we have for example pyflakes.

在 Python 中，我们有例如 pyflakes。

>👇[23:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1382)

If we get this piece of code and run it through pyflakes,

如果我们得到这段代码 并通过 pyflakes 运行它，

>👇[23:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1386)

pyflakes is gonna give us a couple of issues.

pyflakes 会给我们一些问题。

>👇[23:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1390)

First one is the one.... The second one is the one we identified: here's an undefined name called BAZ.

第一个是那个……第二个是 我们确定的：这是一个未定义的名称，称为 BAZ。

>👇[23:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1395)

You probably should be doing something about that.

你可能应该为此 做点什么。

>👇[23:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1397)

And the other one is like oh, you're redefining the

另一个就像 哦，你正在重新定义该行中

>👇[23:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1403)

the FOO variable name in that line.

的 FOO 变量名称。

>👇[23:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1407)

So here we have a FOO function and then we are kind of

所以这里我们有一个 FOO 函数 ，然后我们

>👇[23:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1411)

shadowing that function by using a loop variable here.

通过 在此处使用循环变量来隐藏该函数。

>👇[23:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1414)

So now that FOO function that we defined is not accessible anymore

所以现在我们定义的 FOO 函数 不再可访问

>👇[23:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1418)

and then if we try to call it afterwards, we will get into errors.

，如果我们之后尝试调用它， 我们将陷入错误。

>👇[23:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1423)

There are other types of

还有其他类型的

>👇[23:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1426)

Static Analysis tools. MYPY is a different one. MYPY is gonna report the same two errors, but it's also

静态分析工具。 MYPY 是不同的。 MYPY 会报告同样的两个错误，但它

>👇[23:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1433)

going to complain about type checking. So it's gonna say, oh here you're multiplying an int by a float and

也会抱怨类型检查。 所以它会 说，哦，这里你将一个整数乘以一个浮点数，

>👇[24:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1440)

if you care about the type checking of your code, you should not be mixing those up.

如果你关心代码的类型检查 ，你不应该把它们混在一起。

>👇[24:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1447)

it can be kind of inconvenient, having to run this, look at the line, going back to your

这可能有点不方便，必须运行 它，查看行，回到你的

>👇[24:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1452)

VIM or like your editor, and figuring out what the error matches to.

VIM 或像你的编辑器，并 找出错误匹配的内容。

>👇[24:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1458)

There are already solutions for that. One

已经有解决方案了。 一种

>👇[24:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1462)

way is that you can integrate most editors with these tools and here..

方法是，您可以将大多数 编辑器与这些工具集成在一起，并在此处...

>👇[24:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1468)

You can see there is like some red highlighting on the bash, and it will read the last line here.

您可以看到 bash 上有一些红色突出显示 ，它会在此处读取最后一行。

>👇[24:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1474)

So, undefined named 'baz'.

所以，未定义名为'baz'。

>👇[24:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1476)

So as I'm editing this piece of Python code,

因此，当我编辑这段 Python 代码时，

>👇[24:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1479)

my editor is gonna give me feedback about what's going wrong with this.

我的编辑器会给我反馈，告诉我这里出 了什么问题。

>👇[24:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1483)

Or like here have another one saying the redefinition of unused foo.

或者像这里有另一个说 未使用的 foo 的重新定义。

>👇[24:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1489)

And

-

>👇[24:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1493)

even, there are some stylistic complaints.

甚至，还有一些文体上的抱怨。

>👇[24:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1496)

So, oh, I will expect two empty lines.

所以，哦，我会期待两个空行。

>👇[24:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1498)

So like in Python, you should be having two empty lines between a function definition.

所以就像在 Python 中一样，你应该 在函数定义之间有两个空行。

>👇[25:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1505)

There are...

有……

>👇[25:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1507)

there is a resource on the lecture notes

讲义上有一个资源，关于

>👇[25:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1509)

about pretty much static analyzers for a lot of different programming languages.

许多不同编程语言的静态分析器。

>👇[25:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1513)

There are even static analyzers for English.

甚至还有英语的静态分析器。

>👇[25:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1518)

So I have my notes

所以我

>👇[25:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1524)

for the class here, and if I run it through this static analyzer for English, that is "writegood".

在这里有我的课程笔记，如果我通过这个 英语静态分析器运行它，那就是“writegood”。

>👇[25:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1530)

It's going to complain about some stylistic properties.

它会抱怨 一些风格属性。

>👇[25:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1533)

So like, oh,

所以就像，哦，

>👇[25:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1533)

I'm using "very", which is a weasel word and I shouldn't be using it.

我用的是“非常”，这是一个狡猾的 词，我不应该使用它。

>👇[25:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1537)

Or "quickly" can weaken meaning, and you can have this for spell checking, or for a lot of different

或者“快速”可以弱化意思，你可以用 它来进行拼写检查，或者进行许多不同

>👇[25:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1543)

types of stylistic analysis.

类型的文体分析。

>👇[25:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1548)

Any questions so far?

到目前为止有什么问题吗？

>👇[25:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1557)

Oh,

哦，

>👇[25:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1559)

I forgot to mention...

我忘了提...

>👇[26:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1561)

Depending on the task that you're performing, there will be different types of debuggers.

根据您执行的任务， 将有不同类型的调试器。

>👇[26:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1567)

For example, if you're doing web development,

例如，如果您正在进行 Web 开发，那么

>👇[26:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1569)

both Firefox and Chrome

Firefox 和 Chrome

>👇[26:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1573)

have a really really good set of tools for doing debugging for websites.

都有一套非常好的工具 来对网站进行调试。

>👇[26:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1580)

So here we go and say inspect element,

所以在这里我们说检查元素，

>👇[26:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1583)

we can get the... do you know? how to make this larger...

我们可以得到...你知道吗？ 如何使这个更大...

>👇[26:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1587)

We're getting

我们正在

>👇[26:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1589)

the entire source code for the web page for the class.

获取该课程网页的完整源代码 。

>👇[26:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1595)

Oh, yeah, here we go.

哦，是的，我们开始了。

>👇[26:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1598)

Is that better?

那个更好吗？

>👇[26:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1600)

And we can actually go and change properties about the course. So we can say... we can edit the title.

我们实际上可以去更改 课程的属性。 所以我们可以说...我们可以编辑标题。

>👇[26:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1607)

Say, this is not a class on debugging and profiling.

说，这不是关于 调试和分析的课程。

>👇[26:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1611)

And now the code for the website has changed.

现在网站的代码已经更改。

>👇[26:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1614)

This is one of the reasons why you should never trust

这就是 为什么你永远不应该相信

>👇[26:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1616)

any screenshots of websites, because they can be completely modified.

任何网站截图的原因之一，因为 它们可以被完全修改。

>👇[27:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1621)

And you can also modify this style. Like, here I have things

并且您还可以修改此样式。 就像，这里我有

>👇[27:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1626)

using the

-

>👇[27:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1627)

the dark mode preference,

使用黑暗模式偏好的东西，

>👇[27:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1629)

but we can alter that.

但我们可以改变它。

>👇[27:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1631)

Because at the end of the day, the browser is rendering this for us.

因为在一天结束时， 浏览器正在为我们呈现它。

>👇[27:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1637)

We can check the cookies, but there's like a lot of different operations.

我们可以检查 cookie，但是 有很多不同的操作。

>👇[27:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1641)

There's also a built-in debugger for JavaScript, so you can step through JavaScript code.

还有一个内置的 JavaScript 调试器， 因此您可以单步调试 JavaScript 代码。

>👇[27:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1647)

So kind of the takeaway is, depending on what you are doing, you will probably want to search for what tools

因此，要得出的结论是，根据您的 工作，您可能想要搜索

>👇[27:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1654)

programmers have built for them.

程序员为他们构建的工具。

>👇[27:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1664)

Now I'm gonna switch gears and

现在我要换档，

>👇[27:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1668)

stop talking about debugging, which is kind of finding issues with the code, right?

不再谈论调试，这是 一种发现代码问题的方法，对吧？

>👇[27:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1671)

kind of more about the behavior, and then start talking

更多关于行为的信息， 然后开始

>👇[27:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1674)

about like how you can use profiling.

谈论如何使用分析。

>👇[27:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1676)

And profiling is how to optimize the code.

而profiling就是如何优化代码。

>👇[28:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1681)

It might be because you want to optimize the CPU, the memory, the network, ...

可能是因为您想 优化 CPU、内存、网络……

>👇[28:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1686)

There are many different reasons that you want to be optimizing it.

您想要优化它的原因有很多。

>👇[28:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1690)

As it was the case with debugging, the kind of first-order approach

就像调试的情况一样，

>👇[28:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1694)

that a lot of people have experience with already is

很多人 已经体验过的那种一阶方法是

>👇[28:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1696)

oh, let's use just printf profiling, so to say, like we can just take...

哦，让我们只使用 printf 分析 ，可以说，就像我们可以采取......

>👇[28:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1702)

Let me make this larger. We can

让我把它扩大 . 我们可以

>👇[28:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1706)

take the current time here,

在这里获取当前时间，

>👇[28:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1708)

then we can check, we can do some execution and then we can take the time again and

然后我们可以检查，我们可以执行一些操作 ，然后我们可以再次获取时间并

>👇[28:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1715)

subtract it from the original time.

从原始时间中减去它。

>👇[28:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1717)

And by doing this you can kind of narrow down

通过这样做，您可以缩小

>👇[28:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1719)

and fence some different parts of your code and try to figure out what is the time taken between those two parts.

并隔离代码的某些不同部分，并尝试 找出这两个部分之间花费的时间。

>👇[28:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1727)

And that's good. But sometimes it can be interesting, the results. So here, we're sleeping for

那很好。 但有时结果可能很 有趣。 所以在这里，我们休眠了

>👇[28:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1733)

0.5 seconds and the output is saying, oh it's 0.5 plus some extra time,

0.5 秒，输出说， 哦，它是 0.5 加上一些额外的时间，

>👇[28:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1739)

which is kind of interesting. And if we keep running it, we see there's like some small error and the thing is

这很有趣。 如果我们继续运行它， 我们会看到一些小错误，问题就

>👇[29:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1746)

here, what we're actually measuring is what is usually referred to as the "real time".

在这里，我们实际测量的 是通常所说的“实时”。

>👇[29:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1752)

Real time is as if you get

实时就像你得到

>👇[29:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1754)

like a

一个

>👇[29:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1755)

clock, and you start it when your program starts, and you stop it when your program ends.

时钟，当你的程序开始时你启动 它，当你的程序结束时你停止它。

>👇[29:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1759)

But the thing is, in your computer it is not only your program that is running.

但问题是，在您的计算机中， 不仅仅是您的程序在运行。

>👇[29:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1763)

There are many other programs running at the same time and those might

有许多其他程序同时运行 ，而这些程序

>👇[29:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1767)

be the ones that are taking the CPU. So, to try to make sense of that,

可能正在占用 CPU。 所以，为了理解这一点

>👇[29:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1775)

A lot of... you'll see a lot of programs

，很多……你会看到很多

>👇[29:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1780)

using the terminology that is

程序使用

>👇[29:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1784)

real time, user time and system time.

实时、用户时间和系统时间等术语。

>👇[29:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1786)

Real time is what I explained, which is kind of the entire length of time from start to finish.

实时就是我所解释的，也就是 从开始到结束的整个时间长度。

>👇[29:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1791)

Then there is the user time, which is the amount of time your program spent on the CPU doing user level cycles.

然后是用户时间，这是 您的程序在 CPU 上执行用户级循环所花费的时间。

>👇[29:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1799)

So as I was mentioning, in UNIX, you can be running user level code or kernel level code.

所以正如我提到的，在 UNIX 中，您可以运行 用户级代码或内核级代码。

>👇[30:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1806)

System is kind of the opposite, it's the amount of CPU, like the amount of time that your program spent on the CPU

系统有点相反，它是 CPU 的数量，比如 你的程序在 CPU 上

>👇[30:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1813)

executing kernel mode instructions. So let's show this with an example.

执行内核模式指令所花费的时间。 因此，让我们用一个例子来说明这一点。

>👇[30:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1818)

Here I'm going to "time", which is a command,

在这里，我将使用“time”，这是一个命令，

>👇[30:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1822)

a shell command that's gonna get these three metrics for the following command, and then I'm just

一个 shell 命令，它将为以下命令获取这三个指标 ，然后我只是

>👇[30:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1828)

grabbing a URL from

从

>👇[30:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1831)

a website that is hosted in Spain. So that's gonna take some extra time to go over there and then go back.

西班牙托管的网站中获取一个 URL。 所以这将需要 一些额外的时间去那里然后回去。

>👇[30:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1837)

If we see, here, if we were to just...

如果我们看到，在这里，如果我们只是......

>👇[30:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1839)

We have two prints, between the beginning and the end of the program.

我们有两个打印，在程序的开头 和结尾之间。

>👇[30:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1843)

We could think that this program is taking like 600 milliseconds to execute, but actually

我们可以认为这个 程序执行大约需要 600 毫秒，但实际上

>👇[30:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1849)

most of that time was spent just waiting for the response on the other side of the network and

大部分时间都花在了等待 网络另一端的响应上，而

>👇[30:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1857)

we actually only spent 16 milliseconds at the user level and like 9 seconds, in total 25 milliseconds, actually

我们实际上只在用户级别花费了 16 毫秒，大约 9 秒， 总共 25 毫秒，实际

>👇[31:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1865)

executing CURL code. Everything else was just waiting.

执行 CURL 代码。 其他一切都只是在等待。

>👇[31:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1872)

Any questions related to timing?

有关于时间的任何问题？

>👇[31:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1879)

Ok, so

好的，所以

>👇[31:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1881)

timing can be

时间可能

>👇[31:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1883)

can become tricky, it's also kind of a black box solution. Or if you start adding print statements,

会变得棘手，这也是一种黑盒解决方案。 或者，如果您开始添加打印语句

>👇[31:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1889)

it's kind of hard to add print statements, with time everywhere. So programmers have figured out better tools.

，添加打印语句有点困难，时间无处不在。 所以程序员想出了更好的工具。

>👇[31:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1896)

These are usually referred to as "profilers".

这些通常被称为“分析器”。

>👇[31:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1899)

One quick note that I'm gonna make, is that

我要做的一个简短说明是，

>👇[31:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1904)

profilers, like usually when people

分析器，就像通常当人们

>👇[31:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1906)

refer to profilers they usually talk about

提到分析器时，他们通常谈论

>👇[31:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1909)

CPU profilers because they are the most common, at identifying where like time is being spent on the CPU.

CPU 分析器，因为它们是最常见的，用于识别 在 CPU 上花费了哪些时间。

>👇[31:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1916)

Profilers usually come in kind of two flavors:

分析器通常有两种类型

>👇[31:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1919)

there's tracing profilers and sampling profilers.

：跟踪分析器和采样分析器。

>👇[32:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1922)

and it's kind of good to know the difference because the output might be different.

知道其中的区别是件好事， 因为输出可能会有所不同。

>👇[32:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1927)

Tracing profilers kind of instrument your code.

跟踪分析器可以检测您的代码。

>👇[32:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1930)

So they kind of execute with your code and every time your code enters a function call,

所以他们会执行你的代码， 每次你的代码进入函数调用时，

>👇[32:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1935)

they kind of take a note of it. It's like, oh we're entering this function call at this moment in time and

他们都会记录下来。 就像，哦，我们此时正 及时进入这个函数调用，

>👇[32:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1941)

they keep going and, once they finish, they can report

他们继续进行，一旦 完成，他们就可以报告，

>👇[32:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1944)

oh, you spent this much time executing in this function and

哦，你 在这个函数上花费了

>👇[32:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1948)

this much time in this other function. So on, so forth, which is the example that we're gonna see now.

这么多时间，在另一个函数上花费了这么多时间。 依此类推， 这就是我们现在要看到的例子。

>👇[32:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1954)

Another type of tools are tracing, sorry, sampling profilers.

另一种类型的工具是跟踪， 对不起，采样分析器。

>👇[32:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1958)

The issue with tracing profilers is they add a lot of overhead. Like you might be running your code and having these kind of

跟踪分析器的问题是它们增加了很多开销。 就像您可能正在运行您的代码并且在您旁边进行这些类型的

>👇[32:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1966)

profiling next to you making all these counts,

分析以进行所有这些计数一样，

>👇[32:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1969)

will hinder the performance of your program, so you might get counts that are slightly off.

会影响您的程序的性能，因此 您可能会得到稍微偏离的计数。

>👇[32:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1975)

A sampling profiler, what it's gonna do is gonna execute your program and every

一个采样分析器，它要做的 是执行你的程序，每隔

>👇[32:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1979)

100 milliseconds, 10 milliseconds, like some defined period, it's gonna stop your program. It's gonna halt it,

100 毫秒，10 毫秒，就像某个定义的周期， 它会停止你的程序。 它会停止它，

>👇[33:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1985)

it's gonna look at the stack trace and say, oh, you're right now in this point in the hierarchy, and

它会查看堆栈跟踪并说，哦，你 现在正处于层次结构中的这一点，并

>👇[33:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1992)

identify which function is gonna be executing at that point.

确定此时将执行哪个函数。

>👇[33:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1996)

The idea is that as long as you execute this for long enough,

这个想法是，只要你 执行这个足够长的时间，

>👇[33:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=1999)

you're gonna get enough statistics to know where most of the time is being spent.

你就会得到足够的统计数据来 知道大部分时间花在了哪里。

>👇[33:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2005)

So, let's see an example of a tracing profiling.

那么，让我们看一个跟踪分析的例子。

>👇[33:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2008)

So here we have a piece of code that is just like a

所以这里我们有一段 代码，就像用 Python 完成

>👇[33:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2013)

really simple re-implementation of grep

的 grep 的一个非常简单的重新实现

>👇[33:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2016)

done in Python.

。

>👇[33:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2018)

What we want to check is what is the bottleneck of this program? Like we're just opening a bunch of files,

我们要检查的是这个程序的瓶颈是什么 ？ 就像我们只是打开一堆文件，

>👇[33:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2024)

trying to match this pattern, and then printing whenever we find a match.

试图匹配这个模式，然后 在我们找到匹配项时打印出来。

>👇[33:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2029)

And maybe it's the regex, maybe it's the print...

也许是正则表达式，也许是打印...

>👇[33:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2032)

We don't really know.

我们真的不知道。

>👇[33:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2033)

So to do this in Python, we have the "cProfile".

所以要在 Python 中做到这一点，我们有“cProfile”。

>👇[33:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2039)

And

-

>👇[34:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2040)

here I'm just calling this module and saying I want to sort this by the total amount of time, that

在这里，我只是调用这个模块，并说我想 按总时间对它进行排序，

>👇[34:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2046)

we're gonna see briefly. I'm calling the program we just saw in the editor.

我们将简要介绍一下。 我正在 调用我们刚刚在编辑器中看到的程序。

>👇[34:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2053)

I'm gonna execute this a thousand times and then I want to match (the grep

我要执行这个一千次 ，然后我想匹配（这里的 grep

>👇[34:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2058)

Arguments here) is I want to match these regex

参数）是我想将这些正则表达式匹配

>👇[34:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2062)

to all the Python files in here. And this is gonna output some...

到这里的所有 Python 文件。 这将输出一些...

>👇[34:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2070)

This is gonna produce some output, then we're gonna look at it. First,

这将产生一些输出， 然后我们将查看它。 首先，

>👇[34:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2074)

is all the output from the greps, but at the very end, we're getting

是 greps 的所有输出， 但在最后，我们

>👇[34:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2079)

output from the profiler itself. If we go up

从分析器本身获得输出。 如果我们往上

>👇[34:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2084)

we can see that, hey,

看，我们可以看到，嘿，

>👇[34:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2087)

by sorting we can see that the total number of calls. So we did 8000 calls, because we executed this 1000 times and

通过排序我们可以看到呼叫总数。 所以我们 进行了 8000 次调用，因为我们执行了 1000 次，

>👇[34:57](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2097)

this is the total amount of time we spent in this function (cumulative time). And here we can start to identify

这是我们在此函数中花费的总时间 （累计时间）。 在这里我们可以开始确定

>👇[35:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2103)

where the bottleneck is.

瓶颈在哪里。

>👇[35:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2106)

So here, this built-in method IO open, is saying that we're spending a lot of the time just waiting for

所以在这里，这个内置方法 IO open，是说 我们花了很多时间等待

>👇[35:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2112)

reading from the disk or...

从磁盘读取或者...

>👇[35:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2114)

There, we can check, hey,

在那里，我们可以检查，嘿

>👇[35:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2115)

a lot of time is also being spent trying to match the regex.

，很多时间也被花费了 试图匹配正则表达式。

>👇[35:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2119)

Which is something that you will expect.

这是您所期望的。

>👇[35:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2122)

One of the caveats of using this

使用此

>👇[35:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2126)

tracing profiler is that, as you can see, here

跟踪分析器的注意事项之一是，如您所见，

>👇[35:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2129)

we're seeing our function but we're also seeing a lot of functions that correspond to built-ins.

我们在这里看到了我们的函数，但我们也看到 了许多与内置函数相对应的函数。

>👇[35:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2135)

So like,

就像

>👇[35:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2135)

functions that are third party functions from the libraries. And as you start building more and more complex code,

库中的第三方函数一样。 随着您开始构建越来越复杂的代码，

>👇[35:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2141)

This is gonna be much harder.

这将变得更加困难。

>👇[35:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2144)

So

所以

>👇[35:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2146)

here is another piece of Python code that,

这是另一段 Python 代码，

>👇[35:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2151)

don't read through it, what it's doing is just

不要通读它，它所做的只是

>👇[35:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2154)

grabbing the course website and then it's printing all the...

抓取课程网站， 然后打印所有

>👇[35:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2158)

It's parsing it, and then it's printing all the hyperlinks that it has found.

...解析它，然后打印 它找到的所有超链接 .

>👇[36:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2161)

So there are like these two operations:

所以有这两个操作：

>👇[36:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2163)

going there, grabbing a website, and then parsing it, printing the links.

去那里，抓取一个网站， 然后解析它，打印链接。

>👇[36:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2167)

And we might want to get a sense of

我们可能想了解

>👇[36:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2169)

how those two operations compare to each other. If we just try to execute the

一下这两个操作如何相互比较 。 如果我们只是尝试在

>👇[36:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2176)

cProfiler here and

此处执行 cProfiler 并且

>👇[36:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2179)

we're gonna do the same, this is not gonna print anything. I'm using a tool we haven't seen so far,

我们将执行相同的操作，则不会打印任何内容。 我正在使用我们迄今为止从未见过的工具，

>👇[36:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2184)

but I think it's pretty nice.

但我认为它非常好。

>👇[36:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2185)

It's "TAC", which is the opposite of "CAT", and it is going to reverse the output so I don't have to go up and look.

是“TAC”，与“CAT”相反，它是 要反转输出所以我不用上去看。

>👇[36:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2193)

So we do this and...

所以我们这样做......

>👇[36:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2196)

Hey, we get some interesting output.

嘿，我们得到了一些有趣的输出。

>👇[36:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2199)

we're spending a bunch of time in this built-in method socket_getaddr_info and like in _imp_create_dynamic and

我们在这个内置方法 socket_getaddr_info 上花费了大量时间 ，就像在 _imp_create_dynamic 和

>👇[36:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2206)

method_connect and posix_stat...

method_connect 和 posix_stat 中一样......

>👇[36:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2209)

nothing in my code is directly calling these functions so I don't really know what is the split between the operation of

我的代码中没有任何内容直接调用这些函数所以我 真的不知道操作之间的区别是什么

>👇[36:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2216)

making a web request and parsing the output of that web request. So, for that, we can use

发出网络请求并解析该网络请求的输出 。 因此，为此，我们可以

>👇[37:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2224)

a different type of profiler which is

使用不同类型的分析器，

>👇[37:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2229)

a line profiler. And the line profiler is just going to present the same results

即线分析器。 线路分析器

>👇[37:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2234)

but in a more human-readable way, which is just, for this line of code, this is the amount of time things took.

将以一种更易于阅读的方式呈现相同的结果，这就是这 行代码所花费的时间。

>👇[37:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2244)

So it knows it has to do that, we have to add a decorator to the Python function, we do that.

所以它知道它必须这样做，我们必须 向 Python 函数添加一个装饰器，我们就这样做了。

>👇[37:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2254)

And as we do that,

当我们这样做的时候，

>👇[37:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2257)

we now get slightly cropped output,

我们现在得到了稍微裁剪的输出，

>👇[37:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2259)

but the main idea, we can look at the percentage of time and we can see that making this request, get operation, took

但是主要思想，我们可以看看时间的百分比， 我们可以看到发出这个请求，获取操作，花费了

>👇[37:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2266)

88% of the time, whereas parsing the response took only 10.9% of the time.

88% 的时间，而解析 响应花费了 只有 10.9% 的时间。

>👇[37:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2274)

This can be really informative and a lot of different programming languages will support this type of a line profiling.

这可能非常有用，许多不同的编程 语言都支持这种类型的线路分析。

>👇[38:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2284)

Sometimes, you might not care about CPU.

有时，您可能不关心 CPU。

>👇[38:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2287)

Maybe you care about the memory or like some other resource. Similarly, there are memory profilers: in Python

也许您关心内存或喜欢其他资源。 类似地，还有内存分析器：在 Python 中

>👇[38:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2295)

there is "memory_profiler", for C you will have "Valgrind". So here is a fairly simple example,

有“memory_profiler”，对于 C 你会有 “Valgrind”。 所以这是一个相当简单的例子，

>👇[38:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2301)

we just create this list with a million elements. That's going to consume like megabytes of space and

我们只创建了这个包含一百万个元素的列表。 这 将消耗数兆字节的空间，

>👇[38:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2309)

we do the same, creating another one with 20 million elements.

我们也这样做，创建 另一个包含 2000 万个元素的空间。

>👇[38:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2314)

To check, what was the memory allocation?

要检查，内存分配是什么？

>👇[38:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2318)

How it's gonna happen, what's the consumption? We can go through one memory profiler and

会怎样，消耗是多少？ 我们可以通过一个内存分析器

>👇[38:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2324)

we execute it,

并执行它

>👇[38:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2326)

and it's telling us the total memory usage and the increments.

，它会告诉我们总内存 使用量和增量。

>👇[38:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2331)

And we can see that we have some overhead, because this is an interpreted language and when we create

我们可以看到我们有一些开销，因为 这是一种解释型语言，当我们创建

>👇[38:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2338)

this million,

这一百万，

>👇[39:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2343)

this list with a million entries, we're gonna need this many megabytes of information.

这个包含一百万个条目的列表时，我们将 需要这么多兆字节的信息。

>👇[39:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2347)

Then we were getting another 150 megabytes. Then, we're freeing this entry and that's decreasing the total amount.

然后我们又得到了 150 兆字节。 然后，我们将释放 此条目，从而减少总量。

>👇[39:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2355)

We are not getting a negative increment because of a bug, probably in the profiler.

由于错误，可能在分析器中，我们没有得到负增量。

>👇[39:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2359)

But if you know that your program is taking a huge amount of memory and you don't know why, maybe because you're copying

但是，如果您知道您的程序正在占用大量 内存，而您不知道为什么，也许是因为您正在复制

>👇[39:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2366)

objects where you should be doing things in place, then

应该 在适当位置执行操作的对象，那么

>👇[39:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2371)

using a memory profiler can be really useful.

使用内存分析器可能非常有用。

>👇[39:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2373)

And in fact there's an exercise that will kind of work you through that, comparing

事实上，有一个练习可以帮助 您解决这个问题，将

>👇[39:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2377)

an in-place version of quicksort with like a

快速排序的就地版本与非就地版本进行比较

>👇[39:40](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2380)

non-inplace, that keeps making new and new copies. And if you using the memory profiler

，不断制作新的和新的副本。 如果您使用内存分析器，

>👇[39:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2384)

you can get a really good comparison between the two of them

您可以在两者之间获得非常好的比较

>👇[39:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2391)

Any questions so far, with profiling?

到目前为止，关于分析的任何问题？

>👇[39:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2393)

Is the memory profiler running the program in order to get that?

内存分析器是否正在运行该 程序以获得它？

>👇[39:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2398)

Yeah... you might be able to figure out like just looking at the code.

是的......你也许可以 像看代码一样弄清楚。

>👇[40:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2403)

But as you get more and more complex (for this code at least)

但是随着你变得越来越复杂 （至少对于这段代码）

>👇[40:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2406)

But you get more and more complex programs what this is doing is running through the program

但是你得到越来越复杂的程序， 它正在做的是通过程序运行

>👇[40:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2410)

and for every line, at the very beginning, it's looking at the heap and saying

并且对于每一行，在一开始， 它正在查看堆并说

>👇[40:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2416)

"What are the objects that I have allocated now?"

“ 我现在分配的对象是什么？”

>👇[40:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2419)

"I have seven megabytes of objects", and then goes to the next line,

“我有 7 兆字节的对象”， 然后转到下一行，

>👇[40:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2423)

looks again, "Oh now I have 50, so I have now added 43 there".

再次查看，“哦，现在我有 50 个， 所以我现在在那里添加了 43 个”。

>👇[40:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2428)

Again, you could do this yourself by asking for those operations in your code, every single line.

同样，您可以通过 在代码中的每一行中请求这些操作来自己完成此操作。

>👇[40:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2434)

But that's not how you should be doing things since people have already written these tools for you to use.

但这不是您应该做的事情，因为人们 已经编写了这些工具供您使用。

>👇[40:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2443)

As it was the case with...

就像

>👇[40:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2451)

So as in the case with strace, you can do something similar in profiling.

...的情况一样，就像 strace 的情况一样，您可以 在分析中做类似的事情。

>👇[40:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2458)

You might not care about the specific lines of code that you have,

您可能不关心 您拥有的特定代码行，

>👇[41:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2463)

but maybe you want to check for outside events. Like, you maybe want to check how many

但您可能想要检查外部事件。 比如，您可能想检查

>👇[41:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2469)

CPU cycles your computer program is using, or how many page faults it's creating.

您的计算机程序使用了多少 CPU 周期， 或者它产生了多少页面错误。

>👇[41:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2474)

Maybe you have like bad cache locality and that's being manifested somehow.

也许您喜欢糟糕的缓存局部性 ，并且正在以某种方式表现出来。

>👇[41:19](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2479)

So for that, there is the "perf" command.

为此，有“perf”命令。

>👇[41:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2482)

The perf command is gonna do this, where it is gonna run your program and it's gonna

perf 命令会执行此操作， 它会运行您的程序，它会

>👇[41:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2488)

keep track of all these statistics and report them back to you. And this can be really helpful if you are

跟踪所有这些统计数据并将它们报告 给您。 如果您

>👇[41:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2493)

working at a lower level. So

在较低级别工作，这将非常有用。 所以

>👇[41:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2497)

we execute this command, I'm gonna explain briefly what it's doing.

我们执行这个命令，我将 简要解释它在做什么。

>👇[41:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2508)

And this stress program is just

而这个压力程序只是

>👇[41:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2512)

running in the CPU, and it's just a program to just

在CPU中运行，它 只是一个只

>👇[41:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2514)

hog one CPU and like test that you can hog the CPU. And now if we Ctrl-C,

占用一个CPU的程序，就像测试你能不能 占用CPU一样。 现在，如果我们按 Ctrl-C，

>👇[42:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2520)

we can go back and

我们可以返回并从

>👇[42:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2523)

we get some information about the number of page faults that we have or the number of

我们的代码中获得一些关于 我们拥有的页面错误数或

>👇[42:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2529)

CPU cycles that we utilize, and other

我们使用的 CPU 周期数以及其他

>👇[42:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2532)

useful

有用

>👇[42:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2534)

metrics from our code. For some programs you can

指标的信息。 对于某些程序，您可以

>👇[42:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2541)

look at what the functions that were being used were.

查看 正在使用的功能是什么。

>👇[42:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2546)

So we can record what this program is doing,

所以我们可以记录这个程序在做什么

>👇[42:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2550)

which we don't know about because it's a program someone else has written.

，我们不知道，因为它是 别人写的程序。

>👇[42:35](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2555)

And

-

>👇[42:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2558)

we can report what it was doing by looking at the stack trace and we can say oh,

我们可以通过查看堆栈跟踪来报告它在做什么 ，我们可以说哦，

>👇[42:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2562)

It's spending a bunch of time in this

它在这个 __random_r

>👇[42:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2564)

__random_r

-

>👇[42:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2566)

standard library function. And it's mainly because the way of hogging a CPU is by just creating more and more pseudo-random numbers.

标准库函数中花费了大量时间。 这主要是因为 占用 CPU 的方式就是创建越来越多的伪随机数。

>👇[42:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2573)

There are some other

还有一些其他的

>👇[42:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2575)

functions that have not been mapped, because they

函数没有被映射，因为它们

>👇[42:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2578)

belong to the program, but if you know about your program

属于程序，但是如果 你了解你的程序，

>👇[43:01](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2581)

you can display this information using more flags, about perf.

你可以 使用更多的标志来显示这些信息，关于 perf。

>👇[43:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2585)

There are really good tutorials online about how to use this tool.

关于如何使用此工具，网上有非常好的教程。

>👇[43:12](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2592)

Oh

哦，

>👇[43:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2594)

One one more thing regarding profilers is, so far,

关于 分析器的另一件事是，到目前为止，

>👇[43:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2597)

we have seen that these profilers are really good at

我们已经看到这些分析器 非常擅长

>👇[43:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2600)

aggregating all this information and giving you a lot of these numbers so you can

聚合所有这些信息并为 您提供大量这些数字，以便您可以

>👇[43:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2605)

optimize your code or you can reason about what is happening, but

优化代码或者可以 推断正在发生的事情，但是

>👇[43:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2610)

the thing is

问题是

>👇[43:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2611)

humans are not really good at making sense of lots of numbers and since

人类并不擅长 理解大量数字，而且由于

>👇[43:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2616)

humans are more visual creatures, it's much

人类是更多的视觉动物，因此更

>👇[43:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2619)

easier to kind of have some sort of visualization.

容易进行 某种可视化。

>👇[43:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2622)

Again, programmers have already thought about this and have come up with solutions.

同样，程序员已经考虑到 这一点并提出了解决方案。

>👇[43:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2629)

A couple of popular ones, is a FlameGraph. A FlameGraph is a

几个流行的是 FlameGraph。 FlameGraph 是一个

>👇[43:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2636)

sampling profiler. So this is just running your code and taking samples

采样分析器。 所以这只是运行 你的代码并获取

>👇[44:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2640)

And then on the y-axis here

样本然后在 y 轴上

>👇[44:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2643)

we have the depth of the stack so we know that the bash function called this other function, and this called this other function,

我们有堆栈的深度所以我们知道 bash 函数 调用了另一个函数，这个调用了另一个函数

>👇[44:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2651)

so on, so forth. And on the x-axis it's

，依此类推。 在 x 轴上

>👇[44:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2654)

not time, it's not the timestamps.

不是时间，也不是时间戳。

>👇[44:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2657)

Like it's not this function run before, but it's just time taken. Because, again, this is a sampling profiler:

就像之前没有运行过这个功能，但它只是花费了 时间。 因为，这又是一个采样分析器：

>👇[44:23](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2663)

we're just getting small glimpses of what was it going on in the program. But we know that, for example,

我们只是对程序中发生的事情有了一些了解 。 但是我们知道，例如，

>👇[44:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2669)

this main program took the most time because the

这个主程序花费了最多的时间，因为

>👇[44:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2673)

x-axis is proportional to that.

x 轴与它成正比。

>👇[44:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2676)

They are interactive and they can be really useful to identify the hot spots in your program.

它们是交互式的，它们 对于识别程序中的热点非常有用。

>👇[44:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2684)

Another way of displaying information, and there is also an exercise on how to do this, is using a call graph.

另一种显示信息的方法，还有 一个关于如何做到这一点的练习，是使用调用图。

>👇[44:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2690)

So a call graph is going to be displaying information, and it's gonna create a graph of which function called which other function.

因此，调用图将显示信息，并将 创建一个函数调用哪个其他函数的图。

>👇[44:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2698)

And then you get information about, like,

然后你会得到这样的信息，比如，

>👇[45:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2700)

oh, we know that "__main__" called this "Person" function ten times and

哦，我们知道“__main__”调用了这个 “Person”函数十次

>👇[45:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2706)

it took this much time. And as you have

并且花了这么多时间。 当您拥有

>👇[45:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2709)

larger and larger programs, looking at one of these call graphs can be useful to identify

越来越大的程序时，查看其中 一个调用图可能有助于确定

>👇[45:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2714)

what piece of your code is calling this really expensive IO operation, for example.

您的代码的哪一部分正在调用这个非常 昂贵的 IO 操作，例如。

>👇[45:24](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2724)

With that I'm gonna cover the last part of the lecture, which is that

说到这里，我将介绍 讲座的最后一部分，

>👇[45:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2730)

sometimes, you might not even know what exact resource is constrained in your program.

有时您甚至可能不知道 您的程序中具体限制了哪些资源。

>👇[45:36](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2736)

Like how do I know how much CPU

比如我怎么知道

>👇[45:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2739)

my program is using, and I can quickly look in there, or how much memory.

我的程序使用了多少 CPU，我可以快速 查看那里，或者有多少内存。

>👇[45:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2744)

So there are a bunch of really

所以有很多非常

>👇[45:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2746)

nifty tools for doing that one of them is

漂亮的工具可以做到这一点，其中一个就是

>👇[45:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2750)

HTOP. so HTOP is an

HTOP。 所以 HTOP 是一个

>👇[45:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2754)

interactive command-line tool and here it's displaying all the CPUs this machine has,

交互式命令行工具，在这里它 显示了这台机器的所有 CPU，

>👇[46:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2760)

which is 12. It's displaying the amount of memory, it says I'm consuming almost a gigabyte of the 32 gigabytes my machine has.

即 12。它显示了内存量，它说我 消耗了我机器 32 GB 中的近 1 GB。

>👇[46:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2767)

And then I'm getting all the different processes.

然后我得到所有不同的过程。

>👇[46:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2771)

So for example we have

例如，我们有

>👇[46:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2773)

zsh, mysql and other processes that are running in this machine, and I can sort through the amount of CPU

zsh、mysql 和其他进程在这 台机器上运行，我可以通过它们消耗的 CPU 数量

>👇[46:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2780)

they're consuming or through the priority they're running at.

或 它们运行的​​优先级来排序。

>👇[46:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2785)

We can check this, for example. Here

例如，我们可以检查一下。 这里

>👇[46:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2788)

we have the stress command again

我们再次使用压力命令

>👇[46:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2790)

and we're going to

，我们将

>👇[46:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2791)

run it to take over four CPUs and check that we can see that in HTOP.

运行它来接管四个 CPU，并 检查我们是否可以在 HTOP 中看到它。

>👇[46:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2797)

So we did spot those four CPU jobs, and now I have seen that

所以我们确实发现了那四个 CPU 作业，现在我看到

>👇[46:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2803)

besides the ones we had before, now I have this...

除了我们之前的作业之外， 现在我还有这个......

>👇[46:50](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2810)

Like this "stress -c" command running and taking a bunch of our CPU.

就像这个“stress -c”命令正在运行 并占用我们的大量 CPU。

>👇[46:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2816)

Even though you could use a profiler to get similar information to this, the way HTOP displays this kind of in a live interactive

即使您可以使用分析器来获取与此类似的 信息，HTOP 以实时交互方式显示此类信息的

>👇[47:03](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2823)

fashion can be much quicker and much easier to parse.

方式也可以 更快且更容易解析。

>👇[47:07](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2827)

In the notes, there's a

在注释中，有

>👇[47:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2830)

really long list of different tools for evaluating different parts of your system.

一长串用于评估 系统不同部分的不同工具。

>👇[47:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2835)

So that might be tools for analyzing the

所以这可能是分析

>👇[47:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2837)

network performance, about looking the

网络性能的工具，关于查看

>👇[47:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2840)

number of IO operations, so you know whether you're saturating the

IO 操作的数量，这样您就可以知道

>👇[47:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2846)

the reads from your disks,

磁盘读取是否饱和，

>👇[47:28](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2848)

you can also look at what is the space usage.

您还可以查看空间使用情况。

>👇[47:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2852)

Which, I think, here...

我认为，这里...

>👇[47:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2858)

So NCDU... There's a tool called "du" which stands for "disk usage" and

所以 NCDU...有一个名为“du”的工具 ，它代表“磁盘使用”，

>👇[47:45](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2865)

we have the "-h" flag for "human readable output".

我们有“-h”标志代表 “人类可读输出”。

>👇[47:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2871)

We can do videos and we can get output about the size of all the files in this folder.

我们可以做视频，我们可以得到关于 这个文件夹中所有文件大小的输出。

>👇[48:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2888)

Yeah, there we go.

是的，我们开始了。

>👇[48:10](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2890)

There are also interactive versions, like HTOP was an interactive version.

还有交互式版本， 比如 HTOP 就是一个交互式版本。

>👇[48:15](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2895)

So NCDU is an interactive version that will let me navigate through the folders and I can see quickly that

所以 NCDU 是一个交互式版本，可以让我 浏览文件夹，我可以很快看到

>👇[48:21](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2901)

oh, we have... This is one of the folders for the video lectures,

哦，我们有...这 是视频讲座的文件夹之一

>👇[48:26](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2906)

and we can see there are these four files

，我们可以看到这四个

>👇[48:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2909)

that have like almost 9 GB each and I could quickly delete them through this interface.

文件有 每个差不多 9 GB，我可以 通过这个界面快速删除它们。

>👇[48:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2917)

Another neat tool is "LSOF" which stands for "LIST OF OPEN FILES".

另一个简洁的工具是“LSOF”，它 代表“打开文件列表”。

>👇[48:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2924)

Another pattern that you may encounter is you know

您 可能遇到的另一种模式是，您知道

>👇[48:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2927)

some process is using a file, but you don't know exactly which process is using that file. Or, similarly, some process is listening in

某个进程正在使用一个文件，但您不确切知道哪个进程 正在使用该文件。 或者，类似地，某个进程正在监听

>👇[48:55](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2935)

a port, but again, how do you find out which one it is?

一个端口，但同样，您如何 找出它是哪个进程？

>👇[48:59](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2939)

So to set an example.

所以要树立榜样。

>👇[49:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2940)

We just run a Python HTTP server on port

我们只是在端口 444 上运行一个 Python HTTP 服务器

>👇[49:05](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2945)

444

-

>👇[49:06](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2946)

Running there. Maybe we don't know that that's running, but then we can

。 也许我们不知道 它正在运行，但是我们可以

>👇[49:13](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2953)

use...

使用……

>👇[49:17](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2957)

we can use LSOF.

我们可以使用 LSOF。

>👇[49:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2962)

Yeah, we can use LSOF, and the thing is LSOF is gonna print a lot of information.

是的，我们可以使用 LSOF，关键是 LSOF 会打印很多信息。

>👇[49:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2970)

You need SUDO permissions because

您需要 SUDO 权限，因为

>👇[49:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2974)

this is gonna ask for who has all these items.

这将询问谁拥有所有这些项目。

>👇[49:39](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2979)

Since we only care about the one who is listening in this 444 port

因为我们只关心 正在监听这个 444 端口的人，所以

>👇[49:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2984)

we can ask

我们可以请求

>👇[49:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2986)

grep for that.

grep。

>👇[49:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2987)

And we can see, oh, there's like this Python process, with this identifier, that is using the port and then we can

我们可以看到，哦，有一个 Python 进程，带有 这个标识符，它正在使用端口，然后我们可以

>👇[49:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2996)

kill it,

杀死它，

>👇[49:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=2998)

and that terminates that process.

然后终止该进程。

>👇[50:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3002)

Again, there's a lot of different tools. There's even tools for

同样，有很多不同的 工具。 甚至还有用于

>👇[50:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3008)

doing what is called benchmarking.

执行所谓的基准测试的工具。

>👇[50:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3011)

So in the shell tools and scripting lecture, I said like for some tasks "fd" is much faster than "find"

所以在 shell 工具和脚本讲座中，我 说对于某些任务，“fd”比“find”快得多，

>👇[50:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3018)

But like how will you check that?

但是你将如何检查呢？

>👇[50:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3022)

I can test that with "hyperfine" and I have here two commands: one with "fd" that is just

我可以用“hyperfine”测试它，我这里有 两个命令：一个是“fd”，它只是

>👇[50:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3030)

searching for JPEG files and the same one with "find".

搜索 JPEG 文件 ，另一个是“find”。

>👇[50:34](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3034)

If I execute them, it's gonna benchmark these scripts and give me some output about

如果我执行它们，它将对这些脚本进行基准测试， 并给我一些关于

>👇[50:41](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3041)

how much faster "fd" is

“fd”

>👇[50:45](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3045)

compared to "find".

与“find”相比快多少的输出。

>👇[50:47](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3047)

So I think that kind of concludes... yeah, like 23 times for this task.

所以我认为这样的结论...... 是的，这个任务大约 23 次。

>👇[50:52](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3052)

So that kind of concludes the whole overview.

这样就结束了整个概述。

>👇[50:56](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3056)

I know that there's like a lot of different topics and there's like a lot of

我知道有很多不同的 话题，

>👇[51:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3060)

perspectives on doing these things, but again I want to reinforce the idea

做这些事情有很多观点，但 我想再次

>👇[51:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3064)

that you don't need to be a master of all these topics but more...

强调你不需要 成为所有这些话题的大师，但更多

>👇[51:08](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3068)

To be aware that all these things exist.

...... 要知道所有这些东西都存在。

>👇[51:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3071)

So if you run into these issues you don't reinvent the wheel, and you reuse all that other programmers have done.

因此，如果您遇到这些问题，您不会重新发明轮子 ，而是重用其他程序员所做的一切。

>👇[51:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3078)

Given that, I'm happy to take any questions related to this last section or anything in the lecture.

鉴于此，我很乐意回答 与最后一节或讲座中任何内容相关的任何问题。

>👇[51:25](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3085)

Is there any way to sort of think about how long a program should take?

有什么方法可以考虑 一个程序应该花多长时间？

>👇[51:30](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3090)

You know, if it's taking a while to run

你知道，如果需要一段时间才能运行，

>👇[51:33](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3093)

you know, should you be worried? Or depending on your process, let me wait another ten minutes before I start looking at why it's taking so long.

你知道吗，你应该担心吗？ 或者，根据您的流程，让我再等 十分钟，然后再开始查看为什么要花这么长时间。

>👇[51:43](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3103)

Okay, so the...

好吧，所以...

>👇[51:46](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3106)

The task of knowing how long a program

知道程序应该运行多长时间的任务

>👇[51:49](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3109)

should run is pretty infeasible to figure out. It will depend on the type of program.

是很难弄清楚的。 这将取决于程序的类型。

>👇[51:54](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3114)

It depends on whether you're making HTTP requests or you're reading data... one thing that you can do is if you have

这取决于您是在发出 HTTP 请求还是在 读取数据……您可以做的一件事是

>👇[52:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3122)

for example,

，例如，

>👇[52:02](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3122)

if you know you have to read two gigabytes from memory, like from disk, and load that into memory, you can make

如果您知道必须从内存中读取 2 GB 数据， 例如从磁盘读取数据，然后加载 存入内存，您可以

>👇[52:11](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3131)

back-of-the-envelope calculation. So like that shouldn't take longer than like X seconds because this is

进行粗略计算。 所以这样的 时间不应超过 X 秒，因为

>👇[52:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3136)

how things are set up. Or if you are

事情就是这样设置的。 或者，如果您正在

>👇[52:20](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3140)

reading some files from the network and you know kind of what the network link is and they are taking say five times longer than

从网络上读取一些文件，并且您知道 网络链接是什么，并且它们所花费的时间比您预期的时间长五倍，

>👇[52:27](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3147)

what you would expect then you could

那么您可以

>👇[52:29](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3149)

try to do that.

尝试这样做。

>👇[52:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3151)

Otherwise, if you don't really know. Say you're trying to do some mathematical operation in your code and you're not really sure

否则，如果你真的不知道。 假设您正在尝试 在代码中执行一些数学运算，但您不确定

>👇[52:37](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3157)

about how long that will take you can use something like logging and try to kind of print intermediate

这需要多长时间，您可以使用 日志记录之类的东西并尝试打印中间

>👇[52:44](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3164)

stages to get a sense of like, oh I need to do a thousand operations of this and

阶段以获得类似的感觉，哦，我需要 做一千次这样的操作和

>👇[52:51](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3171)

three iterations

三次迭代

>👇[52:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3173)

took ten seconds. Then this is gonna take much longer than I can handle in my case.

需要十秒钟。 那么这将花费 比我能处理的时间更长的时间。

>👇[53:00](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3180)

So I think there are there are ways, it will again like depend on the task,

所以我认为有很多方法，它 会再次喜欢取决于任务，

>👇[53:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3184)

but definitely, given all the tools we've seen really, we probably have like

但肯定的是，考虑到我们 真正看到的所有工具，我们可能

>👇[53:09](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3189)

a couple of really good ways to start tackling that.

有一些非常好的方法 来开始解决这个问题。

>👇[53:14](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3194)

Any other questions?

还有其他问题吗？

>👇[53:16](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3196)

You can also do things like

您还可以执行一些操作，例如

>👇[53:18](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3198)

run HTOP and see if anything is running.

运行 HTOP 并查看是否有任何东西正在运行。

>👇[53:22](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3202)

Like if your CPU is at 0%, something is probably wrong.

就像如果您的 CPU 为 0%， 则可能有问题。

>👇[53:31](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3211)

Okay.

好的。

>👇[53:32](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3212)

There's a lot of exercises for all the topics that we have covered in today's class,

我们在今天的课程中涵盖的所有主题都有很多练习，

>👇[53:38](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3218)

so feel free to do the ones that are more interesting.

所以请随意做 更有趣的。

>👇[53:42](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3222)

We're gonna be holding office hours again today.

今天我们将再次开放办公时间。

>👇[53:45](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3225)

Just a reminder, office hours. You can come and ask questions about any lecture.

提醒一下，办公时间。 你可以 来问任何讲座的问题。

>👇[53:48](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3228)

Like we're not gonna expect you to kind of do the exercises in a couple of minutes.

就像我们不希望您 在几分钟内完成练习一样。

>👇[53:53](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3233)

They take a really long while to get through them, but we're gonna be there

他们需要很长时间才能 完成，但我们会在

>👇[53:58](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3238)

to answer any questions from previous classes, or even not related to exercises. Like if you want to know more about how you

那里回答以前课程中的任何问题，甚至与练习无关的问题 。 就像你想知道更多关于如何

>👇[54:04](https://www.youtube.com/watch?v=l812pUnKxME&t=31s#t=3244)

would use TMUX in a way to kind of quickly switch between panes, anything that comes to your mind.

使用 TMUX 来在窗格之间快速切换的方式 ，任何你想到的。

### Summary
Highlight 
==what’s important!==