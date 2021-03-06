# html: 语义化标签
> [html5语义化标签](http://www.html5jscss.com/html5-semantics-section.html)

> [html5语义化标签](http://caibaojian.com/html5/ele.html)

> [html5语义化标签](https://www.douban.com/note/320420676/)
# 目录
 * header元素
 * footer元素
 * hgroup元素
 * nav元素
 * aside元素
 * section元素
 * article元素
 * HTML5其他结构元素标签
## header

```
header 元素代表“网页”或“section”的页眉。
通常包含h1-h6元素或hgroup，作为整个页面或者一个内容块的标题。也可以包裹一节的目录部分，一个搜索框，一个nav，或者任何相关logo。
整个页面没有限制header元素的个数，可以拥有多个，可以为每个内容块增加一个header元素
header的示例代码：
*
<header>
    <hgroup>
        <h1>网站标题</h1>
        <h1>网站副标题</h1>
    </hgroup>
</header>
*
header使用注意：
* 可以是“网页”或任意“section”的头部部分；
* 没有个数限制。
* 如果hgroup或h1-h6自己就能工作的很好，那就不要用header。
```

## footer元素

```
footer元素代表“网页”或“section”的页脚，通常含有该节的一些基本信息，譬如：作者，相关文档链接，版权资料。如果footer元素包含了整个节，那么它们就代表附录，索引，提拔，许可协议，标签，类别等一些其他类似信息。
*
<footer>
    COPYRIGHT@小北
</footer>
*
footer使用注意：

* 可以是“网页”或任意“section”的底部部分；
* 没有个数限制，除了包裹的内容不一样，其他跟header类似。
```
## hgroup元素

```
hgroup元素代表“网页”或“section”的标题，当元素有多个层级时，该元素可以将h1到h6元素放在其内，譬如文章的主标题和副标题的组合
*
<hgroup>
    <h1>这是一篇介绍HTML 5语义化标签和更简洁的结构</h1>
    <h2>HTML 5</h2>
</hgroup>
*
hgroup使用注意：
* 如果只需要一个h1-h6标签就不用hgroup
* 如果有连续多个h1-h6标签就用hgroup
* 如果有连续多个标题和其他文章数据，h1-h6标签就用hgroup包住，和其他文章元数据一起放入header标签
```
## nav元素
```
nav元素代表页面的导航链接区域。用于定义页面的主要导航部分。
*
<nav>
    <ul>
        <li>HTML 5</li>
        <li>CSS3</li>
        <li>JavaScript</li>
    </ul>
</nav>
*
但是我在有些时候却情不自禁的想用它，譬如：侧边栏上目录，面包屑导航，搜索样式，或者下一篇上一篇文章，但是事实上规范上说nav只能用在页面主要导航部分上。页脚区域中的链接列表，虽然指向不同网站的不同区域，譬如服务条款，版权页等，这些footer元素就能够用了。
-
nav使用注意：
* 用在整个页面主要导航部分上，不合适就不要用nav元素；
```

## aside元素

```
aside元素被包含在article元素中作为主要内容的附属信息部分，其中的内容可以是与当前文章有关的相关资料、标签、名次解释等。（特殊的section）
在article元素之外使用作为页面或站点全局的附属信息部分。最典型的是侧边栏，其中的内容可以是日志串连，其他组的导航，甚至广告，这些内容相关的页面。
*
<article>
    <p>内容</p>
    <aside>
        <h1>作者简介</h1>
        <p>小北，前端一枚</p>
    </aside>
</article>
*
aside使用总结：
* aside在article内表示主要内容的附属信息，
* 在article之外则可做侧边栏，没有article与之对应，最好不用。
* 如果是广告，其他日志链接或者其他分类导航也可以用
```

## section元素

```
section元素代表文档中的“节”或“段”，“段”可以是指一篇文章里按照主题的分段；“节”可以是指一个页面里的分组。
section通常还带标题，虽然html5中section会自动给标题h1-h6降级，但是最好手动给他们降级。如下：
*
<section>
    <h1>section是啥？</h1>
    <article>
        <h2>关于section</h1>
        <p>section的介绍</p>
        <section>
            <h3>关于其他</h3>
            <p>关于其他section的介绍</p>
        </section>
    </article>
</section>
*
section使用注意：
* 一张页面可以用section划分为简介、文章条目和联系信息。不过在文章内页，最好用article。section不是一般意义上的容器元素，如果想作为样式展示和脚本的便利，可以用div。
* 表示文档中的节或者段；
* article、nav、aside可以理解为特殊的section，所以如果可以用article、nav、aside就不要用section，没实际意义的就用div
```

## article

```
article元素最容易跟section和div容易混淆，其实article代表一个在文档，页面或者网站中自成一体的内容，其目的是为了让开发者独立开发或重用。譬如论坛的帖子，博客上的文章，一篇用户的评论，一个互动的widget小工具。（特殊的section）
除了它的内容，article会有一个标题（通常会在header里），会有一个footer页脚。我们举几个例子介绍一下article，好更好区分article、section、div
*
<article>
    <h1>一篇文章</h1>
    <p>文章内容..</p>
    <footer>
        <p><small>版权：html5jscss网所属，作者：小北</small></p>
    </footer>
</article>
*
上例是最好简单的article标签使用情况，如果在article内部再嵌套article，那就代表内嵌的article是与它外部的内容有关联的，如博客文章下面的评论，如下：
*
<article>

    <header>
        <h1>一篇文章</h1>
        <p><time pubdate datetime="2012-10-03">2012/10/03</time></p>
    </header>

    <p>文章内容..</p>

    <article>
        <h2>评论</h2>

        <article>
            <header>
                <h3>评论者: XXX</h3>
                <p><time pubdate datetime="2012-10-03T19:10-08:00">~1 hour ago</time></p>
            </header>
            <p>哈哈哈</p>
        </article>

        <article>
            <header>
                <h3>评论者: XXX</h3>
                <p><time pubdate datetime="2012-10-03T19:10-08:00">~1 hour ago</time></p>
            </header>
            <p>哈？哈？哈？</p>
        </article>

    </article>

</article>
* 文章里的评论，一个article嵌套article来表示的实例
article内部嵌套article，有可能是评论或其他跟文章有关联的内容。那article内部嵌套section一般是什么情况呢。如下：

<article>

    <h1>前端技术</h1>
    <p>前端技术有那些</p>

    <section>
        <h2>CSS</h2>
        <p>样式..</p>
    </section>

    <section>
        <h2>JS</h2>
        <p>脚本</p>
    </section>

</article>
*  文章里的章节，一个article里的section实例
因为文章内section部分虽然也是独立的部分，但是它门只能算是组成整体的一部分，从属关系，article是大主体，section是构成这个大主体的一部分。本网站的全部文章都是article嵌套一个个section章节，这样能让浏览器更容易区分各个章节所包括的内容。

那section内部嵌套article又有哪些情况呢，如下
*
<section>

    <h1>介绍: 网站制作成员配备</h1>

    <article>
        <h2>设计师</h2>
        <p>设计网页的...</p>
    </article>

    <article>
        <h2>程序员</h2>
        <p>后台写程序的..</p>
    </article>

    <article>
        <h2>前端工程师</h2>
        <p>给楼上两位打杂的..</p>
    </article>

</section>
** 一个section里的article实例
设计师、程序员、前端工程师都是一个独立的整体，他们组成了网站制作基本配备，当然还有其他成员~~。设计师、程序员、前端工程师就像article，是一个个独立的整体，而section将这些自成一体的article包裹，就组成了一个团体。
article和section和例子就例举这么多了，具体情况具体分析，不易深究。漏了divd，其实div就是只是想用来把元素组合或者给它们加样式时使用。
article使用注意：
* 自身独立的情况下：用article
* 是相关内容：用section
* 没有语义的：用div
```

## HTML5其他结构元素标签

```
HTML5节元素标签包括body article nav aside section header footer hgroup ，还有h1-h6 address。
address代表区块容器，必须是作为联系信息出现，邮编地址、邮件地址等等,一般出现在footer。
h1-h6因为hgroup，section和article的出现，h1-h6定义也发生了变化，允许一张页面出现多个h1。
我们不应该滥用超语义化的元素。
```