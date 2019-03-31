# sematicTagging

例子：https://en.wikipedia.org/wiki/World_Wide_Web
      备份页面:http://static001.geekbang.org/static/time/quote/World_Wide_Web-Wikipedia.html

## 标签语义化
### aside和article
其实aside和article自带有的css就是说明他们为块级元素
```
article, aside, footer, header, hgroup, main, nav, section {
    display: block;
}
```

### hgroup,h1,h2
hgroup是标题组

### abbr
表示缩写

### em和strong
em标签：emphasis表示被强调的文本
strong：定义为重要的文本（在 HTML 4.01 中，<strong> 标签定义加粗的被强调的文本，在 HTML 5 中，<strong> 标签定义重要的文本。）

### blockquote,q,cite
blockquote表示段落级引述内容
q表示行内的引述内容
cite表示引述内容的作品名

### time
time标签可以让机器阅读更加方便

### figure
插入文章的内容，只要具有一定自包含性的内容（不限于图片。代码，表格等），都可以用figure其中<figcaption>可以表示内容标题

### dfn
用来包裹被定义的名词

### pre,samp,code
pre标签表明包含的内容是预先排版过的，不需要浏览器进行排版。
samp标签用与示例。
如果是代码需要用到code标签，并且需要pre标签包含code标签。还需用到转义符

## css

### aside和article
calc运算的时候要在运算符前后都添上空格
aside和article是标签不是class
font-size用于消除间隔，但是在其子元素中字体会消失，所以重新给字体赋予大小。如果不用这个font-size属性一行会放不下

### hgroup,h1,h2
这边用border来创建长线的原因：hr 表示故事走向的转变或者话题的转变

### tooltip
在做tooltip时用了getElementByClassName死活出不来，后来改用id就可以正常运行。