# css选择器

## 相关问题

1. 如何在css中选择一个元素
2. querySelector参数设置
3. 选择类名以`header-`开头的元素

> css 选择器不仅可以用于在css文件中选择合适的元素设置样式，还可以应用在`document.querySelector`中选择元素，非常方便

| 选择器 | 示例 | 示例说明 | CSS |
| :--- | :--- | :--- | :--- |
| [.class](https://www.runoob.com/cssref/sel-class.html) | .intro | 选择所有class="intro"的元素 | 1 |
| [\#id](https://www.runoob.com/cssref/sel-id.html) | \#firstname | 选择所有id="firstname"的元素 | 1 |
| [\*](https://www.runoob.com/cssref/sel-all.html) | \* | 选择所有元素 | 2 |
| [element](https://www.runoob.com/cssref/sel-element.html) | p | 选择所有&lt;p&gt;元素 | 1 |
| [element,element](https://www.runoob.com/cssref/sel-element-comma.html) | div,p | 选择所有&lt;div&gt;元素和&lt;p&gt;元素 | 1 |
| [element element](https://www.runoob.com/cssref/sel-element-element.html) | div p | 选择&lt;div&gt;元素内的所有&lt;p&gt;元素 | 1 |
| [element&gt;element](https://www.runoob.com/cssref/sel-element-gt.html) | div&gt;p | 选择所有父级是 &lt;div&gt; 元素的 &lt;p&gt; 元素 | 2 |
| [element+element](https://www.runoob.com/cssref/sel-element-pluss.html) | div+p | 选择所有紧接着&lt;div&gt;元素之后的&lt;p&gt;元素 | 2 |
| [\[attribute\]](https://www.runoob.com/cssref/sel-attribute.html) | \[target\] | 选择所有带有target属性元素 | 2 |
| [\[attribute=value\]](https://www.runoob.com/cssref/sel-attribute-value.html) | \[target=-blank\] | 选择所有使用target="-blank"的元素 | 2 |
| [\[attribute~=value\]](https://www.runoob.com/cssref/sel-attribute-value-contains.html) | \[title~=flower\] | 选择标题属性包含单词"flower"的所有元素 | 2 |
| [\[attribute\|=language\]](https://www.runoob.com/cssref/sel-attribute-value-lang.html) | \[lang\|=en\] | 选择 lang 属性以 en 为开头的所有元素 | 2 |
| [:link](https://www.runoob.com/cssref/sel-link.html) | a:link | 选择所有未访问链接 | 1 |
| [:visited](https://www.runoob.com/cssref/sel-visited.html) | a:visited | 选择所有访问过的链接 | 1 |
| [:active](https://www.runoob.com/cssref/sel-active.html) | a:active | 选择活动链接 | 1 |
| [:hover](https://www.runoob.com/cssref/sel-hover.html) | a:hover | 选择鼠标在链接上面时 | 1 |
| [:focus](https://www.runoob.com/cssref/sel-focus.html) | input:focus | 选择具有焦点的输入元素 | 2 |
| [:first-letter](https://www.runoob.com/cssref/sel-firstletter.html) | p:first-letter | 选择每一个&lt;p&gt;元素的第一个字母 | 1 |
| [:first-line](https://www.runoob.com/cssref/sel-firstline.html) | p:first-line | 选择每一个&lt;p&gt;元素的第一行 | 1 |
| [:first-child](https://www.runoob.com/cssref/sel-firstchild.html) | p:first-child | 指定只有当&lt;p&gt;元素是其父级的第一个子级的样式。 | 2 |
| [:before](https://www.runoob.com/cssref/sel-before.html) | p:before | 在每个&lt;p&gt;元素之前插入内容 | 2 |
| [:after](https://www.runoob.com/cssref/sel-after.html) | p:after | 在每个&lt;p&gt;元素之后插入内容 | 2 |
| [:lang\(language\)](https://www.runoob.com/cssref/sel-lang.html) | p:lang\(it\) | 选择一个lang属性的起始值="it"的所有&lt;p&gt;元素 | 2 |
| [element1~element2](https://www.runoob.com/cssref/sel-gen-sibling.html) | p~ul | 选择p元素之后的每一个ul元素 | 3 |
| [\[attribute^=value\]](https://www.runoob.com/cssref/sel-attr-begin.html) | a\[src^=“https”\] | 选择每一个src属性的值以"https"开头的元素 | 3 |
| [\[attribute$=value\]](https://www.runoob.com/cssref/sel-attr-end.html) | a\[src$=".pdf"\] | 选择每一个src属性的值以".pdf"结尾的元素 | 3 |
| [\[attribute\*=value\]](https://www.runoob.com/cssref/sel-attr-contain.html) | a\[src\*=“runoob”\] | 选择每一个src属性的值包含子字符串"runoob"的元素 | 3 |
| [:first-of-type](https://www.runoob.com/cssref/sel-first-of-type.html) | p:first-of-type | 选择每个p元素是其父级的第一个p元素 | 3 |
| [:last-of-type](https://www.runoob.com/cssref/sel-last-of-type.html) | p:last-of-type | 选择每个p元素是其父级的最后一个p元素 | 3 |
| [:only-of-type](https://www.runoob.com/cssref/sel-only-of-type.html) | p:only-of-type | 选择每个p元素是其父级的唯一p元素 | 3 |
| [:only-child](https://www.runoob.com/cssref/sel-only-child.html) | p:only-child | 选择每个p元素是其父级的唯一子元素 | 3 |
| [:nth-child\(n\)](https://www.runoob.com/cssref/sel-nth-child.html) | p:nth-child\(2\) | 选择每个p元素是其父级的第二个子元素 | 3 |
| [:nth-last-child\(n\)](https://www.runoob.com/cssref/sel-nth-last-child.html) | p:nth-last-child\(2\) | 选择每个p元素的是其父级的第二个子元素，从最后一个子项计数 | 3 |
| [:nth-of-type\(n\)](https://www.runoob.com/cssref/sel-nth-of-type.html) | p:nth-of-type\(2\) | 选择每个p元素是其父级的第二个p元素 | 3 |
| [:nth-last-of-type\(n\)](https://www.runoob.com/cssref/sel-nth-last-of-type.html) | p:nth-last-of-type\(2\) | 选择每个p元素的是其父级的第二个p元素，从最后一个子项计数 | 3 |
| [:last-child](https://www.runoob.com/cssref/sel-last-child.html) | p:last-child | 选择每个p元素是其父级的最后一个子级。 | 3 |
| [:root](https://www.runoob.com/cssref/sel-root.html) | :root | 选择文档的根元素 | 3 |
| [:empty](https://www.runoob.com/cssref/sel-empty.html) | p:empty | 选择每个没有任何子级的p元素（包括文本节点） | 3 |
| [:target](https://www.runoob.com/cssref/sel-target.html) | \#news:target | 选择当前活动的\#news元素（包含该锚名称的点击的URL） | 3 |
| [:enabled](https://www.runoob.com/cssref/sel-enabled.html) | input:enabled | 选择每一个已启用的输入元素 | 3 |
| [:disabled](https://www.runoob.com/cssref/sel-disabled.html) | input:disabled | 选择每一个禁用的输入元素 | 3 |
| [:checked](https://www.runoob.com/cssref/sel-checked.html) | input:checked | 选择每个选中的输入元素 | 3 |
| [:not\(selector\)](https://www.runoob.com/cssref/sel-not.html) | :not\(p\) | 选择每个并非p元素的元素 | 3 |
| [::selection](https://www.runoob.com/cssref/sel-selection.html) | ::selection | 匹配元素中被用户选中或处于高亮状态的部分 | 3 |
| [:out-of-range](https://www.runoob.com/cssref/sel-out-of-range.html) | :out-of-range | 匹配值在指定区间之外的input元素 | 3 |
| [:in-range](https://www.runoob.com/cssref/sel-in-range.html) | :in-range | 匹配值在指定区间之内的input元素 | 3 |
| [:read-write](https://www.runoob.com/cssref/sel-read-write.html) | :read-write | 用于匹配可读及可写的元素 | 3 |
| [:read-only](https://www.runoob.com/cssref/sel-read-only.html) | :read-only | 用于匹配设置 “readonly”（只读） 属性的元素 | 3 |
| [:optional](https://www.runoob.com/cssref/sel-optional.html) | :optional | 用于匹配可选的输入元素 | 3 |
| [:required](https://www.runoob.com/cssref/sel-required.html) | :required | 用于匹配设置了 “required” 属性的元素 | 3 |
| [:valid](https://www.runoob.com/cssref/sel-valid.html) | :valid | 用于匹配输入值为合法的元素 | 3 |
| [:invalid](https://www.runoob.com/cssref/sel-invalid.html) | :invalid | 用于匹配输入值为非法的元素 | 3 |

> 表格来自[菜鸟教程](https://www.runoob.com/cssref/css-selectors.html)，在此仅做为笔记参考

