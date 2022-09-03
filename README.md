# MarkDown 笔记  

Markdown是一种轻量级标记语言，排版语法简洁，让人们更多地关注内容本身而非排版。它使用易读易写的纯文本格式编写文档，可与HTML混编，可导出 HTML、PDF 以及本身的 .md 格式的文件。因简洁、高效、易读、易写，Markdown被大量使用，如Github、Wikipedia、简书等

# 基础语法
## 1 标题
不同数量的 `#` 可以完成不同的标题，如下：
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
```

``` md
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
```
依此类推

## 2 字体
粗体、斜体、粗体和斜体，删除线，需要在文字前后加不同的标记符号。如下：  
```
*这个是斜体*  
**这个是粗体**  
***这个是粗体加斜体***  
~~这里想用删除线~~ 
```

``` md
*这个是斜体*  
**这个是粗体**  
***这个是粗体加斜体***  
~~这里想用删除线~~  
```
| 字体 | 对应标记符号 |
| - | - |
| 斜体 | * |
| 粗体 | ** |
| 斜体加粗 | *** |
| 删除线 | ~~ |

**注**：如果想给字体换颜色、字体或者居中显示，需要使用内嵌 HTML 来实现。

## 3 列表
### 3.1 无序列表
无序列表的使用，在符号 `-` 后加空格使用。如下：
```
- 无序列表 1
- 无序列表 2
  - 无序列表 2.1
  - 无序列表 2.2
- 无序列表 3
```

- 无序列表 1
- 无序列表 2
  - 无序列表 2.1
  - 无序列表 2.2
- 无序列表 3

### 3.2 有序列表
有序列表的使用，在数字及符号 `.` 后加空格后输入内容，如下：
```
1. 有序列表 1
2. 有序列表 2
3. 有序列表 3
```

``` md
1. 有序列表 1
2. 有序列表 2
3. 有序列表 3
```

## 4 引用
引用的格式是在符号 `>` 后面书写文字。如下：
```
> 读一本好书，就是在和高尚的人谈话。 —— 歌德
```

> 读一本好书，就是在和高尚的人谈话。 —— 歌德

> 雇用制度对工人不利，但工人根本无力摆脱这个制度。 —— 阮一峰

## 5 链接
```
[<链接文字>](<链接>)
```
[点我去百度](https://www.baidu.com)

## 6 图片

插入图片，格式如下：
```
![<图片未加载成功展示的文本>](<图片地址>)
```

![这里是图片未加载成功展示的文本](https://cdn.pixabay.com/photo/2020/03/31/19/20/dog-4988985_960_720.jpg)  

![这里是图片未加载成功展示的文本](https://www.nginx.cn/wp-content//2020/03/qrcode_for_gh_82cf87d482f0_258.jpg)  

支持 **jpg**、**png**、**gif**、**svg** 等图片格式，**其中 svg 文件仅可在微信公众平台中使用**


## 7 分割线
可以在一行中用三个以上的减号来建立一个分隔线，同时需要在分隔线的上面空一行。如下：
```
---
```

这里有个分割线 👇

---

这里有个分割线 👆

## 8 表格
可以使用冒号(：)来定义表格的对齐方式，如下：
```
| 姓名   | 年龄 |     工作 |
| :----- | :--: | -------: |
| 小可爱 |  18  | 吃可爱多 |
| 小小勇敢 |  20  | 爬棵勇敢树 |
| 小小小机智 |  22  | 看一本机智书 |
```

| 姓名   | 年龄 |     工作 |
| :----- | :--: | -------: |
| 小可爱 |  18  | 吃可爱多 |
| 小小勇敢 |  20  | 爬棵勇敢树 |
| 小小小机智 |  22  | 看一本机智书 |

# 特殊语法

## 1 脚注
> 支持平台：微信公众号、知乎。

脚注与链接的区别如下所示：

``` md
链接：[文字](链接)  
脚注：[文字](脚注解释 "脚注名字")  
```

## 2 代码块
> 支持平台：微信代码主题仅支持微信公众号！其他主题无限制。

如果在一个行内需要引用代码，只要用反引号引起来就好，如下：
```
Use the `printf()` function.
```
Use the `printf()` function.

在需要高亮的代码块的前一行及后一行使用三个反引号，同时**第一行反引号后面表示代码块所使用的语言**，如下：
```
    ``` java
    // FileName: HelloWorld.java
    public class HelloWorld {
        // Java 入口程序，程序从此入口
        public static void main(String[] args) {
            System.out.println("Hello,World!"); // 向控制台打印一条语句
        }
    }
    ```
```


``` java
// FileName: HelloWorld.java
public class HelloWorld {
  // Java 入口程序，程序从此入口
  public static void main(String[] args) {
    System.out.println("Hello,World!"); // 向控制台打印一条语句
  }
}
```

支持以下语言种类：
```
bash
clojure，cpp，cs，css
dart，dockerfile, diff
erlang
go，gradle，groovy
haskell
java，javascript，json，julia
kotlin
lisp，lua
makefile，markdown，matlab
objectivec
perl，php，python
r，ruby，rust
scala，shell，sql，swift
tex，typescript
verilog，vhdl
xml
yaml
```

其中**微信代码主题与微信官方一致**，有以下注意事项：

- 带行号且不换行，代码大小与官方一致
- 需要在代码块处标志语言，否则无法高亮
- 粘贴到公众号后，用鼠标点代码块内外一次，完成高亮

diff 不能同时和其他语言的高亮同时显示，且需要调整代码主题为微信代码主题以外的代码主题才能看到 diff 效果，使用效果如下:

``` diff
+ 新增项
- 删除项
```

## 3 数学公式
> 支持平台：微信公众号、知乎

块公式使用方法如下：  
$$ H(D_2) = -\left(\frac{2}{4}\log_2 \frac{2}{4} + \frac{2}{4}\log_2 \frac{2}{4}\right) = 1 $$

矩阵：
$$
  \begin{pmatrix}
  1 & a_1 & a_1^2 & \cdots & a_1^n \\
  1 & a_2 & a_2^2 & \cdots & a_2^n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  1 & a_m & a_m^2 & \cdots & a_m^n \\
  \end{pmatrix}
$$

公式由于微信不支持，目前的解决方案是转成 svg 放到微信中，无需调整，矢量不失真。  
目前测试如果公式量过大，在 Chrome 下会存在粘贴后无响应，但是在 Firefox 中始终能够成功。  

## 4 HTML

支持原生 HTML 语法，请写内联样式，如下：

<span style="display:block;text-align:right;color:orangered;">橙色居右</span>
<span style="display:block;text-align:center;color:orangered;">橙色居中</span>

搬运自 [MarkDown官方文档](https://markdown.com.cn/)