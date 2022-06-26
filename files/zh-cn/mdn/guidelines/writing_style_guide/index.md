---
title: MDN Web 文档写作规范
slug: MDN/Guidelines/Writing_style_guide
tags:
  - MDN
  - MDN Meta
  - MDN Web 文档
  - MDN 规范
  - 写作规范
  - 准则
  - 教程
  - 文档
  - 规范
translation_of: MDN/Guidelines/Writing_style_guide
original_slug: MDN/Guidelines/Style_guide
---
<div>{{MDNSidebar}}</div>

<p>为了提供更加组织化、标准化且易于阅读的文档，MDN Web 文档写作规范明确了文本的组织方式、拼写规则、固定格式等内容，不过这些内容只是指导性的而不是严格的规定，因为比起格式我们对内容更感兴趣，所以没有必要在参与贡献之前强迫自己学习本规范。但是如果有一位勤劳的志愿者在之后编辑了你的文档使它更加符合本规范，也请不要感到惊讶或难过。</p>

<p>本规范主要适用于英文文档。其他语言可能也有（也欢迎创建）相应的规范。这些应该作为子页面发布在各个本地化小组的页面中。</p>

<div class="note">
<p><strong>备注：</strong> 本文的写作规范是针对英文所写的，当你在为文档的英文原文作贡献时，你应该参考这份规范。简体中文翻译时的规范请参见《<a href="https://github.com/mdn/translated-content/blob/main/docs/zh-cn/translation-guide.md">针对 MDN 文档的本地化指南</a>》，当然“针对 MDN 文档的本地化指南”仅列出了常见的规范，这份文档较为详细一点，在翻译时，参考一些相关内容也是有益的。</p>
</div>

<h2 id="基础部分">基础部分</h2>

<p>为了使文档保持更好的一致性，所有主流的写作规范指南都是从一些比较基本的写作规范开始的。以下几个小节所概述的这些基本规范内容应该会对你有很大帮助。</p>

<h3 id="页面标题">页面标题</h3>

<p>页面标题不仅会在搜索时用到，在页面顶部的面包屑路径中也会被用来表示文档的层级结构。页面标题（就是显示在页面顶部以及搜索结果中标题的部分）可以与页面 URL“<code>&lt;locale&gt;/docs/</code>”之后的“铭牌（slug）”部分不同。</p>

<h4 id="文章标题和段落标题的大写规则">文章标题和段落标题的大写规则</h4>

<p>页面的标题和章节的标头应当使用语句式大写（只大写第一个单词的首字母以及专有名词的首字母），而不应该使用标题式大写：</p>

<ul>
 <li><strong>正确</strong>: "A new method for creating JavaScript rollovers"</li>
 <li><strong>错误</strong>: "A New Method for Creating JavaScript Rollovers"</li>
</ul>

<p>我们还有很多旧的页面是在这条规范确立之前就已经发布了的。所以只要你愿意，你随时可以更新它们的标题。我们也正在逐步完善它们。</p>

<h4 id="标题和铭牌的选择">标题和铭牌的选择</h4>

<p>页面的铭牌应该尽量简短，当创建一个新的层级时，新层级的铭牌最好只由一到两个单词组成。</p>

<p>而页面的标题长度并没有什么严格的限制，只要合理并且表意明确即可。</p>

<h4 id="创建新的子目录">创建新的子目录</h4>

<p>当你要给某个新的主题或主体添加文章时，你通常需要创建一个引导页，然后再把要添加的文章作为子页面添加进去。引导页开篇应当用一两段话来描述一下当前主题或技术，然后添加一个子页面的目录列表，并简要描述每个页面的内容。你可以使用一些我们已经编写好的宏把相关的子页面自动插入到目录列表中。</p>

<p>例如，<a href="/zh-CN/docs/Web/JavaScript">JavaScript</a> 指南，其结构如下：</p>

<ul>
 <li><a href="/zh-CN/docs/Web/JavaScript/Guide">JavaScript/指南</a> - 主目录页</li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Guide/JavaScript_Overview">JavaScript/指南/JavaScript概述</a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Guide/Functions">JavaScript/指南/函数</a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Guide/Details_of_the_Object_Model">JavaScript/指南/对象模型的细节</a></li>
</ul>

<p>尽量避免把文章内容放置在层次结构的顶层，这会降低网站的访问速度，同时搜索和导航的效率也会下降。</p>

<h3 id="文章内容的通用原则">文章内容的通用原则</h3>

<p>在写任何文档时，知道该写多少是很重要的。如果你写的长篇大论，文章读起来就会冗长无味，更不会有人愿意使用它。保持文章内容适量很重要，原因有很多。这其中的原因就有：为了确保读者能够找到他们真正想要的信息，以及为搜索引擎提供足够的优质素材来对文章进行分析和排名。我们将在这里讨论前者（提供读者可能需要的信息）。如果想了解如何让文章更好地被搜索引擎分类和排名，参阅文章 <a href="/zh-CN/docs/MDN/Contribute/Howto/Write_for_SEO">How to write for SEO on MDN</a>。</p>

<p>我们的目标是在页面中包含读者可能需要的所有信息，但又不至于太过冗长。为了实现这个目标，我们给出了一些建议。</p>

<h4 id="为读者着想">为读者着想</h4>

<p>请记住，这些只是指导性的。其中某些建议并不适用于所有状况。当然你应该始终为你的读者着想。例如，在一篇介绍高级网络技术的文章中，通常不需要像介绍网络编程的文章那样包含过多的网络基本概念。</p>

<h4 id="提供一个有用的简介">提供一个有用的简介</h4>

<p>在开篇或第一个段落标题之前给出文章的简介，以使读者快速了解文章中是否包含他们感兴趣的内容。在指南或教程类的文章中，简介还应该让读者明白文章覆盖了哪些主题，以及文章期望读者能够从中了解到哪些知识。简介中应该包含文章中介绍和讨论的技术、API，并提供相关的链接，同时还应该提供可能会遇到的情况的提示。</p>

<h5 id="示例：过于简短的简介">示例：过于简短的简介</h5>

<p>下面这个例子中的简介太过于简短，很多信息都没有包含进来，比如“stroke text”是什么意思，文本会在哪里等。</p>

<blockquote>
<p><strong><code>CanvasRenderingContext2D.strokeText()</code></strong> draws a string.</p>
</blockquote>

<h5 id="示例：过于冗长的简介">示例：过于冗长的简介</h5>

<p>下面是上面那个简介的修改版，但是这次它又太过冗长了。其中包含了过多的细节，并且还包含了很多其他方法和属性，但实际上它应该将重点聚焦在 <code>strokeText()</code> 方法上，然后给出详细介绍它的文章的链接即可。</p>

<blockquote>
<p>When called, the Canvas 2D API method <strong><code>CanvasRenderingContext2D.strokeText()</code></strong>strokes the characters in the specified string beginning at the coordinates specified, using the current pen color. In the terminology of computer graphics, "stroking" text means to draw the outlines of the glyphs in the string without filling in the contents of each character with color.</p>

<p>The text is drawn using the context's current font as specified in the context's {{domxref("CanvasRenderingContext2D.font", "font")}} property.</p>

<p>The placement of the text relative to the specified coordinates are determined by the context's <code>textAlign</code>, <code>textBaseline</code>, and <code>direction</code> properties. <code>textAlign</code> controls the placement of the string relative to the X coordinate specified; if the value is <code>"center"</code>, then the string is drawn starting at <code>x - (stringWidth / 2)</code>, placing the specified X-coordinate in the middle of the string. If the value is <code>"left"</code>, the string is drawn starting at the specified value of <code>x</code>. And if <code>textAlign</code> is <code>"right"</code>, the text is drawn such that it ends at the specified X-coordinate.</p>

<p>(etc etc etc...)</p>

<p>You can, optionally, provide a fourth parameter that lets you specify a maximum width for the string, in pixels. If you provide this parameter, the text is compressed horizontally or scaled (or otherwise adjusted) to fit inside a space that wide when being drawn.</p>

<p>You can call the <strong><code>fillText()</code></strong> method to draw a string's characters as filled with color instead of only drawing the outlines of the characters.</p>
</blockquote>

<h5 id="示例：这次好多了">示例：这次好多了</h5>

<p>下面这个简介比前两个要好很多。</p>

<blockquote>
<p>The {{domxref("CanvasRenderingContext2D")}} method <code><strong>strokeText()</strong></code>, part of the <a href="/en-US/docs/Web/API/Canvas_API">Canvas 2D API</a>, strokes—that is, draws the outlines of—the characters of a specified string, anchored at the position indicated by the given X and Y coordinates. The text is drawn using the context's current {{domxref("CanvasRenderingContext2D.font", "font")}}, and is justified and aligned according to the {{domxref("CanvasRenderingContext2D.textAlign", "textAlign")}}, {{domxref("CanvasRenderingContext2D.textBaseline", "textBaseline")}}, and {{domxref("CanvasRenderingContext2D.direction", "direction")}} properties.</p>

<p>For more details and further examples, see {{SectionOnPage("/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Drawing_graphics", "Text")}} in the Learning Area as well as our main article on the subject, <a href="/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text">Drawing text</a>.</p>
</blockquote>

<h4 id="多提供一些示例">多提供一些示例</h4>

<p>文章应该尽量多提供一些示例。实际上，大多数文章都应该包含不止一个例子。使用例子来说明每个参数的用途或每个可能的边界条件是很有必要的。同时还应该用例子来演示常见问题的解决方法，以及应该如何解决使用过程中可能碰到的一些问题。</p>

<p>每个例子都应该先给出解释，说明它做了什么，以及读者在阅读或动手尝试之前需要了解的内容。</p>

<h5 id="关于示例代码">关于示例代码</h5>

<p>每段示例代码都应该就其工作原理给出说明。最好将一段较长的代码分解成多个较小的部分，并提供每个部分的说明，说明时注意细节的层次。如果代码很简单并且不直接涉及到当前 API，可以只给出一个简单的介绍，说明其用途，以及为何要把它放在这里；而如果代码比较复杂、或用到了当前的 API、或在技术上比较有创造性，那么你应该提供更详细的说明。</p>

<p>如果使用的是<a href="/zh-CN/docs/MDN/Structures/Live_samples">在线演示</a>的方式，则可以将 HTML、CSS、JavaScript 拆分到不同的 {{HTMLElement("pre")}} 中，它们在运行时会自动组合到一起，但使用这种方式每个里面都可以有自己的说明。因此这是一种很好很强大的方式。</p>

<h4 id="过短的文章难以被搜索到">过短的文章难以被搜索到</h4>

<p>如果文章过短，那么搜索引擎可能会难以甚至无法对其建立关键字索引。一般来说，文章的主体内容应该至少包含 250-300 个单词。但是也不要对内容确实很少的文章进行刻意的扩充，在可能的情况下尽量遵守该指导原则即可。</p>

<h3 id="标题">标题</h3>

<p>对于小节的标题，应使用从大到小的方式来定义级别：{{HTMLElement("h2")}}、{{HTMLElement("h3")}}、{{HTMLElement("h4")}} 这样，并且中间不要跳过某一级。因为 H1 已用于文章的标题，因此小节的标题应该从 H2 开始。如果你的文章中小节的层次超过了 3 到 4 级，那么你可能需要考虑将整篇文章拆分成几篇小的文章。</p>

<p>按下回车键（Enter 或 Return）可以开始一个新的段落。如果只是想换行而不是另起一段，可以按住 Shift 并敲下回车。</p>

<p>不要创建只包含一个小节的子级别，如果只有一个小节，那么拆分主题就是没有意义的。至少包含两个小节，要么就不要拆分。</p>

<p>不要让两个小节标题紧挨在一起，这样看起来很丑。每个小节标题的下面至少要放上一段对后面各子小节的简短说明，这会对阅读的人很有帮助。</p>

<h3 id="列表">列表</h3>

<p>列表的格式应该在所有文章中保持一致，并且应在列表中恰当使用标点和结构合理的句子。不管是哪种类型的列表，都需要对格式进行适当的调整。下面的内容说明了每种列表之间的不同。</p>

<h4 id="无序列表">无序列表</h4>

<p>无序列表可以以简洁且有效的方式对内容进行分组显示。每个条目都会以类似“•”的符号来标识。在无序列表中要注意正确使用标点，尤其是每句的最后不要遗漏掉句号。应该以标准写作方式来对待无序列表。</p>

<p>下面是一个结构良好的无序列表的例子：</p>

<p>在这个例子中需要包括：</p>

<ul>
 <li>一种情况，然后跟上一个简短的说明。</li>
 <li>一种情况，然后跟上一个简短的说明。</li>
 <li>另一种情况，并跟上一些解释和说明。</li>
</ul>

<p>可以看到，每个条目的格式都是一致的：首先显示一个“•”符号，然后列出一种情况，然后写上逗号，并在逗号后面添加一些对当前情况的简单说明。</p>

<h4 id="有序列表">有序列表</h4>

<p>有序列表用序号来标识每个条目。同样要注意应该在有序列表中使用适当的格式，保持列表的清晰和简洁，这一点与无序列表是类似的。但是有序列表中的某些条目内容可能会很多，因此正确使用标点就更为重要了，因为难免会遇到必须使用复杂句子的情况。</p>

<p>下面是一个结构良好的有序列表的例子：</p>

<p>为了创建一个好的有序列表，你需要：</p>

<ol>
 <li>以一个介绍性的标题开始，以引出后续的序列。我们可以在开始有序列表的序列之前提供这一内容。</li>
 <li>开始创建各个序列，这些序列会用数字依次编号。这是有序列表的标准格式，能够很容易地被读者理解。有序列表中的某些条目内容可能会很多，因此正确使用标点是很重要的。</li>
 <li>列表序列完成之后，应在后面再提供一段简短的总结。</li>
</ol>

<p>这段内容就是一个总结。我们已经创建了一个简短的有序列表，解释了创建良好格式的有序列表应遵循的步骤。</p>

<p>有序列表基本都用来表示具有连续性关系的内容，因此应该先深入思考你要用这些内容达到什么目的，然后再去撰写。</p>

<h3 id="文本格式和样式">文本格式和样式</h3>

<p>可以使用“样式”下拉列表中的预定义样式来格式化你选定的内容。</p>

<div class="note">
<p><strong>备注：</strong> “Note”样式用来强调重要提示，就像这个。</p>
</div>

<div class="warning">
<p><strong>警告：</strong> 类似地，“Warning”样式用来创建一个警告框。</p>
</div>

<p>除非有特殊需要，否则请不要用 HTML 的 <code>style</code> 属性来手动给内容添加样式。如果你没有找到你需要的预定义样式，可以在 <a href="https://discourse.mozilla.org/c/mdn/236">MDN 论坛</a>寻求帮助。</p>

<h3 id="示例代码的格式和样式">示例代码的格式和样式</h3>

<div class="note">
<p><strong>备注：</strong> 这一小节只是讨论 MDN 文章中的示例代码的样式和格式问题，如果你想了解如何编写示例代码，请参考<a href="/zh-CN/docs/MDN/Contribute/Guidelines/Code_samples">示例代码指南</a>。</p>
</div>

<h4 id="缩进和换行符">缩进和换行符</h4>

<p>每级缩进都使用两个空格来缩进，并在所有的示例中保持一致。对于代码块的起始语句，应将开大括号“{”与当前语句写在一行上，比如：</p>

<pre class="brush: js">if (condition) {
  /* handle the condition */
} else {
  /* handle the "else" case */
}
</pre>

<p>如果一行的代码很长，应在适当的地方换行以避免出现水平滚动条。下面是一个例子：</p>

<pre class="brush: js">if (class.CONDITION || class.OTHER_CONDITION || class.SOME_OTHER_CONDITION
       || class.YET_ANOTHER_CONDITION ) {
  /* something */
}

var toolkitProfileService = Components.classes["@mozilla.org/toolkit/profile-service;1"]
                           .createInstance(Components.interfaces.nsIToolkitProfileService);
</pre>

<h4 id="内联代码格式">内联代码格式</h4>

<p>对于函数名、变量名、方法名等，应使用“Inline Code”按钮（编辑器中显示为“&lt;&gt;”的按钮）将其设置为内联代码格式（内联代码使用的是 {{HTMLElement("code")}} 元素）。比如：<code>frenchText()</code> 函数。</p>

<p>方法名后面应该加上小括号：<code>doSomethingUseful()</code>，这样会比较容易将方法与其他代码元素区分开来。</p>

<h4 id="语法高亮">语法高亮</h4>

<p>对于整行或多行代码，此时别再使用 {{HTMLElement("code")}} 元素来格式化了，而应该对其进行<a href="/zh-CN/docs/MDN/Contribute/Markdown_in_MDN#示例代码块">语法高亮</a>。</p>

<h4 id="HTML_元素的样式">HTML 元素的样式</h4>

<p>HTML 元素的样式有一套自己的规则。遵守这些规则可以让元素及其组件的描述方式保持统一，并且还可以保证能够正确链接到各元素的详细文档页面。</p>

<dl>
 <dt>元素名称</dt>
 <dd>使用 <a href="https://github.com/mdn/yari/blob/main/kumascript/macros/HTMLElement.ejs"><code>HTMLElement</code></a> 宏会生成一个指向该元素详情页的链接。比如，\{{HTMLElement("title")}} 会生成”{{HTMLElement("title")}}“。如果不想生成链接，就将元素名称用尖括号括起来，然后将其设置为内联代码样式，比如 <code>&lt;title&gt;</code>。</dd>
 <dt>属性名称</dt>
 <dd>请使用<strong>粗体</strong>。</dd>
 <dt>属性定义</dt>
 <dd>对正在定义的术语使用 <a href="https://github.com/mdn/yari/blob/main/kumascript/macros/htmlattrdef.ejs"><code>htmlattrdef</code></a> 宏（如 \{{htmlattrdef("type")}}），这样其他页面就可以使用 <a href="https://github.com/mdn/yari/blob/main/kumascript/macros/htmlattrxref.ejs"><code>htmlattrxref</code></a> 宏来链接到该页面了（例如 \{{htmlattrxref("attr","属性")}}）。</dd>
 <dt>属性值</dt>
 <dd>请使用内联代码样式，并且注意字符串两边不要加引号，除非是代码的语法要求加引号。举例：当将 <code>&lt;input&gt;</code> 元素的 <strong>type</strong> 属性设置为 <code>email</code> 或 <code>tel</code> 时……</dd>
</dl>

<h3 id="拉丁文缩写">拉丁文缩写</h3>

<h4 id="在补充说明的括号中">在补充说明的括号中</h4>

<p>一般的拉丁文缩写（如：“etc.”、“i.e.”、“e.g.”）都可以用在起补充说明的括号里面。这时应在缩写中添加句号，后面加上逗号或其他恰当的标点。</p>

<ul>
 <li><strong>正确</strong>：Web browsers (e.g., Firefox) can be used ...</li>
 <li><strong>错误</strong>：Web browsers e.g. Firefox can be used ...</li>
 <li><strong>错误</strong>：Web browsers, e.g. Firefox, can be used ...</li>
 <li><strong>错误</strong>：Web browsers, (eg: Firefox) can be used ...</li>
</ul>

<h4 id="在一般句子中">在一般句子中</h4>

<p>在普通的句子中（即括号的外面），请使用与缩写等价的英文单词或短语。</p>

<ul>
 <li><strong>正确</strong>：... web browsers, and so on.</li>
 <li><strong>错误</strong>：... web browsers, etc.</li>
 <li><strong>正确</strong>：Web browsers such as Firefox can be used ...</li>
 <li><strong>错误</strong>：Web browsers e.g. Firefox can be used ...</li>
</ul>

<h4 id="缩写、拉丁文原文和英文的对照表">缩写、拉丁文原文和英文的对照表</h4>

<table>
 <tbody>
  <tr>
   <th>缩写</th>
   <th>拉丁文</th>
   <th>英文</th>
  </tr>
  <tr>
   <td>cf.</td>
   <td><em>confer</em></td>
   <td>compare</td>
  </tr>
  <tr>
   <td>e.g.</td>
   <td><em>exempli gratia</em></td>
   <td>for example</td>
  </tr>
  <tr>
   <td>et al.</td>
   <td><em>et alii</em></td>
   <td>and others</td>
  </tr>
  <tr>
   <td>etc.</td>
   <td><em>et cetera</em></td>
   <td>and so forth, and so on</td>
  </tr>
  <tr>
   <td>i.e.</td>
   <td><em>id est</em></td>
   <td>that is, in other words</td>
  </tr>
  <tr>
   <td>N.B.</td>
   <td><em>nota bene</em></td>
   <td>note well</td>
  </tr>
  <tr>
   <td>P.S.</td>
   <td><em>post scriptum</em></td>
   <td>postscript</td>
  </tr>
 </tbody>
</table>

<div class="note">
<p><strong>备注：</strong> 在使用前请仔细思考使用拉丁文缩写是否真的能带来好处。上面列出的某些缩写很少用到，很多读者可能不知道其意思，还有一些读者可能会分不清其中的某些缩写。另外，如果你决定使用缩写，那么请确保你的用法是正确的。比如，一个很多人经常会犯的错误是将“e.g.”和“i.e.”弄混。</p>
</div>

<h4 id="首字母缩写和一般缩写">首字母缩写和一般缩写</h4>

<dl>
 <dt>大写与句号</dt>
 <dd>在这两种缩写中（包括国家和组织的缩写，如“US”、“UN”），请使用全大写且不要添加句号。
 <ul>
  <li><strong>正确</strong>: XUL</li>
  <li><strong>错误</strong>: X.U.L.、Xul</li>
 </ul>
 </dd>
 <dt>缩写展开</dt>
 <dd>文章中第一次遇到某个缩写术语时，应该同时给出其展开形式，从而让不了解该缩写的读者能够知道它所指代的内容。如果不确定要不要展开那么就选择展开，或者更好的办法是将其链接到<a href="/zh-CN/docs/Glossary">术语表</a>中的对应条目。
 <ul>
  <li><strong>正确</strong>: XUL (XML User Interface Language) is Mozilla's XML-based language...</li>
  <li><strong>错误</strong>: XUL is Mozilla's XML-based language...</li>
 </ul>
 </dd>
 <dt>缩写的复数形式</dt>
 <dd>当需要使用复数形式的缩写时，直接在后面加上“s”即可，请务必不要加撇号。
 <ul>
  <li><strong>正确</strong>: CD-ROMs</li>
  <li><strong>错误</strong>: CD-ROM's</li>
 </ul>
 </dd>
 <dt>“Versus”、“vs.”和“v.”</dt>
 <dd>推荐使用“vs.”。
 <ul>
  <li><strong>正确</strong>: this vs. that</li>
  <li><strong>错误</strong>: this v. that</li>
  <li><strong>错误</strong>: this versus that</li>
 </ul>
 </dd>
</dl>

<h3 id="大写">大写</h3>

<p>在文章内容中请使用标准英文大写规则，比如对于“World Wide Web”需大写每个单词的首字母。如果“web”和“internet”是单独使用或作为修饰词使用，那么将其全小写也可以——这一指导原则是后来修改过的，所以在 MDN 中你也许会看到很多首字母大写的“Web”和“Internet”。当你编辑文章的时候遇到这种情况，可以随它去，也可以随手修改一下。但是仅仅只是为了修改一下大写的话就没必要专门去编辑一下了。</p>

<p>对于键盘按键，应该使用普通的大写规则，而不是全大写。比如，是“Enter”而不是“ENTER”。</p>

<h3 id="简写">简写</h3>

<p>我们倾向于宽松的写作风格，所以你可以按你的喜好来决定是否使用简写（如”don't“、”can't“、”shouldn't“）。</p>

<h3 id="名称复数">名称复数</h3>

<p>请使用英文风格的复数形式，不要使用拉丁文或希腊文的形式。</p>

<ul>
 <li><strong>正确</strong>: syllabuses、octopuses</li>
 <li><strong>错误</strong>: syllabi、octopi</li>
</ul>

<h3 id="连字符">连字符</h3>

<p>当两个单词连起来组成另一个单词时，如果前一个单词的最后一个字母是元音字母，并且与后一个单词的第一个字母相同时，应使用连字符。</p>

<ul>
 <li><strong>正确</strong>: email、re-elect、co-op</li>
 <li><strong>错误</strong>: e-mail、reelect、coop</li>
</ul>

<h3 id="使用性别中立的表述">使用性别中立的表述</h3>

<p>在任何性别无关的场合使用性别中立的表述方式是一种比较好的做法，这样可以使你的文章具有普适性。举个例子，如果你正在写的是关于某个男人的行为，那么使用“he”来指代是没问题的；但如果内容并没有特指是男还是女，那么再使用“he”就不太恰当了。</p>

<p>让我们再看几个例子：</p>

<p>
<em>A confirmation dialog appears, asking the user if he allows the Web page to make use of his Web cam.</em>
</p>

<p>
<em>A confirmation dialog appears, asking the user if she allows the Web page to make use of her Web cam.</em>
</p>

<p>这两句话使用的都是特定性别的表述方式，我们可以将其修改为性别中立的代词：</p>

<p>
<em>A confirmation dialog appears, asking the user if they allow the Web page to make use of their Web cam.</em>
</p>

<div class="note">
<p><strong>备注：</strong> MDN 允许使用这种通用性的语法（尽管在正式用法中这一点还存在争议）来弥补英语在表达中立性别时的不足。将第三人称复数的代词用来表示性别中立代词（即使用“they”、“them”、“their”、“theirs”）是可以接受的，也就是通常所说的“单数形式的‘they’”。</p>
</div>

<p>或者使用复数形式的“users”：</p>

<p>
<em>A confirmation dialog appears, asking the users if they allow the web page to make use of their web cams.</em>
</p>

<p>当然，最好的方法还是重写句子，去掉其中的代词：</p>

<p>
<em>A confirmation dialog appears, requesting the user's permission for web cam access.</em>
</p>

<p>
<em>A confirmation dialog box appears, which asks the user for permission to use the web cam.</em>
</p>

<p>最后一种方法（译注：意指去除代词的方法）可能更好一些，因为它不但语法上更加正确，而且还能消除不同语言处理性别问题时所带来的复杂性，因为不同语言对性别的处理可能有不同的规则。因此这种方法无论是对读者（译注：意为阅读英语原文的非英语读者）还是翻译者来说都可以让翻译更简单。</p>

<h3 id="数字和数词">数字和数词</h3>

<h4 id="日期">日期</h4>

<p>请用“January 1, 1990”这样的形式来表达日期（不包括代码中的日期）。</p>

<ul>
 <li><strong>正确</strong>: February 24, 2006</li>
 <li><strong>错误</strong>: February 24th, 2006、24 February, 2006、24/02/2006</li>
</ul>

<p>或者你也可以使用“YYYY/MM/DD”的形式：</p>

<ul>
 <li><strong>正确</strong>: 2006/02/24</li>
 <li><strong>错误</strong>: 02/24/2006、24/02/2006、02/24/06</li>
</ul>

<h4 id="年代">年代</h4>

<p>请使用“1990s”这种形式来表示年代，但不要使用撇号：</p>

<ul>
 <li><strong>正确</strong>: 1990s</li>
 <li><strong>错误</strong>: 1990's</li>
</ul>

<h4 id="数词的复数">数词的复数</h4>

<p>数词的复数直接在后面加“s”，同样不要使用撇号：</p>

<ul>
 <li><strong>正确</strong>: 486s</li>
 <li><strong>错误</strong>: 486's</li>
</ul>

<h4 id="逗号">逗号</h4>

<p>应该仅在数字的位数大于等于 5 位时才使用逗号分隔符：</p>

<ul>
 <li><strong>正确</strong>: 4000、54,000</li>
 <li><strong>错误</strong>: 4,000、54000</li>
</ul>

<h3 id="标点符号">标点符号</h3>

<h4 id="连续逗号">连续逗号</h4>

<p>请使用连续逗号。连续逗号（也叫牛津逗号）是在一个包含三个或以上单词或短语的序列中位于连词前的那个逗号。</p>

<ul>
 <li><strong>正确</strong>: I will travel on trains, planes, and automobiles.</li>
 <li><strong>错误</strong>: I will travel on trains, planes and automobiles.</li>
</ul>

<div class="note">
<p><strong>备注：</strong> 这种情况在翻译时应将逗号翻译为顿号。“针对 MDN 文档的本地化指南”一文的<a href="https://github.com/mdn/translated-content/blob/main/docs/zh-cn/translation-guide.md#标点符号">标点符号</a>”一节中也提到了这个问题。</p>
</div>

<h3 id="拼写">拼写</h3>

<p>如果一个单词具有多种拼写，请使用美国英语的拼写。一般来说，<a href="https://www.dictionary.com/">Dictionary.com</a> 上的第一个拼写是符合此要求的，除非单词本身即为其他变体形式或主要用于美国以外的国家中。例如，如果你去查“<a href="https://dictionary.reference.com/browse/honour">honour</a>”，你会看到一个标注“Chiefly British”，并在其后有一个指向美语标准形式的链接。请不要使用其他的拼写变体。</p>

<ul>
 <li><strong>正确</strong>: localize、honor</li>
 <li><strong>错误</strong>: localise、honour</li>
</ul>

<h3 id="术语">术语</h3>

<h4 id="HTML_元素">HTML 元素</h4>

<p>请使用”元素“来表示 HTML 和 XML 元素，不要使用”标记“。另外，请在元素名称两边使用尖括号”&lt;&gt;“括起来，并使用 {{HTMLElement("code")}} 样式。当文章中第一次出现某个元素的时候，应该用 <a href="https://github.com/mdn/yari/blob/main/kumascript/macros/HTMLElement.ejs"><code>HTMLElement</code></a> 宏创建一个指向该元素文档的链接（除非你正在撰写的恰好是该元素的文档页面）。</p>

<ul>
 <li><strong>正确</strong>: {{HTMLElement("span")}} 元素</li>
 <li><strong>错误</strong>: span 标记</li>
</ul>

<h4 id="函数参数">函数参数</h4>

<p>在 MDN 上推荐使用 <strong>parameters</strong> 来表示函数的参数，为了保持一致性，如果可能的话请尽量避免使用”arguments“。</p>

<h4 id="描述用户的操作">描述用户的操作</h4>

<p>在说明一系列操作步骤时，应使用祈使语气来描述用户的操作，并用 UI 组件的名称和其元素类型来标识操作对象。</p>

<ul>
 <li><strong>正确</strong>: 点击编辑按钮</li>
 <li><strong>错误</strong>: 点击编辑</li>
</ul>

<h3 id="语态">语态</h3>

<p>推荐使用主动语态，但被动语态也可以接受，只是可能会让文章看起来不太正式。建议选择一种并在文章中尽量保持统一。</p>

<h2 id="其他参考资料">其他参考资料</h2>

<h3 id="推荐样式指南">推荐样式指南</h3>

<p>如果你在撰写过程中或在格式方面遇到了本文尚未提及的问题，我们建议你参考 <a href="https://docs.microsoft.com/zh-cn/style-guide">微软的风格指南</a>，如果还是不能解决问题，还可参考<a href="https://www.amazon.com/Chicago-Manual-Style-16th/dp/0226104206">芝加哥论文格式</a>，网络上有一份非官方的<a href="https://faculty.cascadia.edu/cma/HIST148/cmscrib.pdf">PDF版本</a></p>

<h3 id="推荐词典">推荐词典</h3>

<p>如果有拼写方面的问题，请参考 <a href="http://www.dictionary.com/">Dictionary.com</a>。本网站的拼写检查采用美国英语规则，因此请不要使用其他拼写规则（例如应该使用“color”而不是“colour”）。</p>

<p>我们会继续扩充本指南，因此如果你遇到了本文未提及的问题，请<a href="/zh-CN/docs/MDN/Contribute/Getting_started#第四步：寻求帮助">联系我们</a>，让我们了解还需要加入哪些内容。</p>

<h3 id="MDN">MDN</h3>

<p>MDN 中<a href="/zh-CN/docs/MDN/Contribute/Structures/Macros/Commonly-used_macros">常用的宏</a>及其说明。</p>

<h3 id="语言、语法和拼写">语言、语法和拼写</h3>

<p>如果你对提高写作和编辑能力感兴趣，下面的资料会对你有所帮助：</p>

<ul>
 <li><a href="https://www.amazon.com/Writing-Well-30th-Anniversary-Nonfiction/dp/0060891548">更好的写作</a>（Amazon），作者 William Zinsser</li>
 <li><a href="https://www.amazon.com/Style-Basics-Clarity-Grace-4th/dp/0205830765/">清晰与优雅的格式基础</a>（Amazon），作者 Joseph Williams 和 Gregory Colomb</li>
 <li><a href="https://brians.wsu.edu/common-errors-in-english-usage/">使用英文时的常见错误</a></li>
 <li><a href="https://www-personal.umich.edu/~jlawler/aue.html">英语语法 FAQ</a></li>
 <li><a href="https://www.angryflower.com/bobsqu.gif">Bob 的撇号快速指南，你个笨蛋</a>（这很有趣）</li>
 <li><a href="https://www.amazon.com/Merriam-Websters-Concise-Dictionary-English-Usage/dp/B004L2KNI2">Merriam-Webster 的简明英语用法词典</a>（Amazon），虽是学术著作但很容易理解，基于实际例子并给出解释，对非英语国家的人很有帮助，特别是介词的使用方面。</li>
 <li><a href="http://english.stackexchange.com/">StackExchange 网站的英语子站</a>，关于英语使用的问答网站。</li>
</ul>