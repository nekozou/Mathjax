# Mathjax

mathjax是一个用于latex、[mathml]([MathML | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/MathML))和[ascimath]([AsciiMath](http://asciimath.org/#syntax))表示法的开源javascript显示引擎，可在所有现代浏览器中工作，并内置了对诸如屏幕阅读器等辅助技术的支持。

mathjax的3.0版是对mathjax的彻底重写，它的使用和配置与mathjax的2版有很大的不同。如果需要，可以使用左侧侧边栏底部的绿色菜单访问版本2文档。

它的设计目标是将web技术的最新进展整合为一个单一的、确定的、支持主要浏览器和操作系统（包括移动设备上的浏览器和操作系统）的web平台上的数学。它不需要用户设置（不需要下载插件或安装软件），因此页面作者可以编写包含数学的web文档，并确信用户能够自然、轻松地查看它。其中一个简单地包括mathjax和web页面中的一些数学，而mathjax完成其余的工作。

mathjax使用基于web的字体来生成高质量的排版，这种排版可以以全分辨率缩放和打印，这与包含在位图图像中的数学不同。使用mathjax，数学是基于文本的，而不是基于图像的，因此它可用于搜索引擎，这意味着可以搜索公式，就像页面的文本一样。mathjax允许页面作者使用tex和latex符号编写公式， [MathML](http://www.w3.org/TR/MathML3) （用XML格式表示数学的万维网联盟标准），或 [AsciiMath](http://asciimath.org/) 表示法。mathjax可以生成多种格式的输出，包括带有css样式的html或可缩放矢量图形（svg）图像。

mathjax包括生成可与屏幕阅读器一起使用的数学表达式的可说出文本版本的能力，为视力受损的人提供可访问性。mathjax中的辅助支持还包括一个交互式表达式浏览器，它可以帮助这些用户一次“遍历”一个表达式，而不必一次听一个复杂的表达式，并且能够“折叠”部分表达式以允许要读取的简化表达式，只有在需要更多详细信息时才展开。

mathjax是模块化的，因此它只能在必要时加载组件，并且可以根据需要进行扩展以包含新功能。mathjax是高度可配置的，允许作者根据其网站的特殊需求对其进行自定义。与mathjax的早期版本不同，版本3可以打包成一个文件，或者作为那些以这种方式管理javascript资产的站点的大型捆绑包的一部分包含。

最后，mathjax有一个丰富的应用程序编程接口（api），可用于使web页面上的数学具有交互性和动态性。版本3已经用typescript（一个包含类型检查和转换到es5的javascript版本）在es6中重写。它被设计成可以很容易地在服务器上使用（作为 `node.js` 应用程序）在浏览器中。这使得对包含数学的网页的预处理比版本2要容易得多，因此网站可以预先执行所有的数学处理，而不是让浏览器在每次查看网页时都这样做。

## **基础知识**

### [什么是mathjax?](https://www.osgeo.cn/mathjax/basic/mathjax.html#what-is-mathjax)

mathjax是一个用于latex、mathml和ascimath表示法的开源javascript显示引擎，可在所有现代浏览器中工作。它的设计目标是将web技术的最新进展整合为一个单一的、确定的、支持主要浏览器和操作系统（包括移动设备上的浏览器和操作系统）的web平台上的数学。它不需要用户设置（不需要下载插件或安装软件），因此页面作者可以编写包含数学的web文档，并确信用户能够自然、轻松地查看它。其中一个简单地包括mathjax和web页面中的一些数学，而mathjax完成其余的工作。

mathjax使用基于web的字体来生成高质量的排版，这种排版可以以全分辨率缩放和打印，这与包含在位图图像中的数学不同。使用mathjax，数学是基于文本的，而不是基于图像的，因此它可用于搜索引擎，这意味着可以搜索公式，就像页面的文本一样。mathjax允许页面作者使用tex和latex符号编写公式， [MathML](http://www.w3.org/TR/MathML3) （用XML格式表示数学的万维网联盟标准），或 [AsciiMath](http://asciimath.org/) 表示法。mathjax可以生成多种格式的输出，包括带有css样式的html或可缩放矢量图形（svg）图像。

mathjax包括生成可与屏幕阅读器一起使用的数学表达式的可说出文本版本的能力，为视力受损的人提供可访问性。mathjax中的辅助支持还包括一个交互式表达式浏览器，它可以帮助这些用户一次“遍历”一个表达式，而不必一次听一个复杂的表达式，并且能够“折叠”部分表达式以允许要读取的简化表达式，只有在需要更多详细信息时才展开。

mathjax是模块化的，因此它只能在必要时加载组件，并且可以根据需要进行扩展以包含新功能。mathjax是高度可配置的，允许作者根据其网站的特殊需求对其进行自定义。与mathjax的早期版本不同，版本3可以打包成一个文件，或者作为那些以这种方式管理javascript资产的站点的大型捆绑包的一部分包含。

最后，mathjax有一个丰富的应用程序编程接口（api），可用于使web页面上的数学具有交互性和动态性。版本3已经用typescript（一个包含类型检查和转换到es5的javascript版本）在es6中重写。它被设计成可以很容易地在服务器上使用（作为 `node.js` 应用程序）在浏览器中。这使得对包含数学的网页的预处理比版本2要容易得多，因此网站可以预先执行所有的数学处理，而不是让浏览器在每次查看网页时都这样做。

##  基本语法

### 1.1 呈现位置

- 行内公式:使用`$…$`定义，此时公式在一行内显示

例子：$\sum_{i=0}^N\int_{a}^{b}g(t,i)\text{d}t$

- 文内公式:使用`$$…$$`定义，此时公式居中放大显示

例子：

```latex
\sum_{i=0}^N\int_{a}^{b}g(t,i)\text{d}t
```

$$
\sum_{i=0}^N\int_{a}^{b}g(t,i)\text{d}t
$$

例子：

```latex
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
```

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$



+ 行内公式也可显示为文内公式的样子，需要在前面加上`\displaystyle`，如$$\displaystyle\sum_{i=0}^N\int_{a}^{b}g(t,i)\text{d}t$$

- 下列语句如非特殊说明均省略**$**

#### 对齐

```latex
$$
\begin{align}
y &= (a-b)(a+b) \\
&= a^2 - b^2
\end{align}
$$
```

$$
\begin{align}
y &= (a-b)(a+b) \\
&= a^2 - b^2
\end{align}
$$

### 1.2 字母与杂项

#### 1.2.1希腊字母

小写和大写的区别在于首字母是否大写。

| 显示(小写/大写)      | 命令     | 显示(小写/大写)  | 命令   |
| -------------------- | -------- | ---------------- | ------ |
| $\alpha\ \Alpha$     | \alpha   | $\beta\ \Beta$   | \beta  |
| $\gamma\ \Gamma$     | \gamma   | $\delta\ \Delta$ | \delta |
| $\epsilon\ \Epsilon$ | \epsilon | $\zeta\ \Zeta$   | \zeta  |
| $\eta\ \Eta$         | \eta     | $\theta\ \Theta$ | \theta |
| $\iota\ \Iota$       | \iota    | $\kappa\ \Kappa$ | \kappa |
| $\lambda\ \Lambda$   | \lambda  | $\mu\ \Mu$       | \mu    |
| $\nu\ \Nu$           | \nu      | $\xi\ \Xi$       | \xi    |
| $\pi\ Pi$            | \pi      | $\rho\ \Rho$     | \rho   |
| $\sigma\ \Sigma$     | \sigma   | $\tau\ \Tau$     | \tau   |
| $\upsilon\ \Upsilon$ | \upsilon | $\phi\ \Phi$     | \phi   |
| $\chi\ \Chi$         | \chi     | $\psi\ \Phi$     | \psi   |
| $\omega\ \Omega$     | \omega   | —                | —      |

- 如果要大写希腊字母，则**首字母大写**即可，如`\Gamma`显示为Γ

+ 如果要使希腊字母显示为斜体，则前面添加var即可，如`\varGamma`显示为Γ

#### 1.2.2字母修饰

##### a.上下标

- 上标：`^`

- 下标：`_`

+ 举例：`C_n^2`显示为$C_n^2$
+ 如果上下标的内容多于一个字符，则需要用`{ }`括起来。
+ 举例：`e^2,e^{ax+b}`显示为$e^2,e^{ax+b}$。

##### b.矢量

- 单字母向量:

+ `\vec a`显示为$\vec a$
+ `\overrightarrow a`显示为$\overrightarrow a$
+ 多字母向量:
+ `\vec{ab}`显示为$\vec{ab}$
+ `\overrightarrow ab`显示为$\overrightarrow ab$

##### c.特殊修饰

+ 字母上`^`:`\hat a`显示为$\hat a$

+ 平均数(上划线):`\overline a`显示为$\overline a$

+ 下划线:`\underline a`显示为$\underline a$

**d.字体**

+ TypeWriter:`\mathtt {MAYDAY}`显示为$\mathtt {MAYDAY}$
+ Blackboard blod:`\mathbb {MAYDAY}`显示为$\mathbb {MAYDAY}$

+ Sans Serif:`\mathsf {MAYDAY}`显示为$\mathsf {MAYDAY}$

**e.空格**

+ 语法本身忽略空格，`ab`和`a b`都显示为$a b$；
+ 小空格：`$a\ b$`显示为$a\ b$；
+ 4格空格：`$a\quad b$`显示为$a\quad b$；
+ 8格空格：`$a\qquad b$`显示为$a\qquad b$；

#### 1.2.3分组

+ 使用`{}`将同一级的括在一起，成组处理
+ 例子：`x_i^2`显示为$x_i^2$，而`x_{i^2}`显示为$x_{i^2}$

#### 1.2.4括号

+ 小括号:`(...)`显示为:$(...)$
+ 中括号:`[...]`显示为$[...]$
+ 大括号:`\{...\}`显示为$\{...\}$
+ 尖括号:`\langle...\rangle`显示为$\langle...\rangle$

+ 绝对值:`\vert...\vert`显示为$\vert...\vert$

+ 双竖线:`\Vert...\Vert`显示为`\Vert...\Vert`
+ 使用`\left`和`\right`使符号大小与邻近的公式相适应，该语句适用于所有括号类型。
+ 例如`\{\frac{(x+y)}{[\alpha+\beta]}\}`显示为$\{\frac{(x+y)}{[\alpha+\beta]}\}$

而，`\left\{\frac{(x+y)}{[\alpha+\beta]}\right\}`显示为$\left\{\frac{(x+y)}{[\alpha+\beta]}\right\}$

#### 1.2.5常用数学[运算符](https://so.csdn.net/so/search?q=运算符&spm=1001.2101.3001.7020)

**注:**想要表达非的概念只需前加`\not`，会添加删除斜线，如:`\not`=显示为$\not=$，`\not\in`显示为$\not\in$。

##### a.基础符号

|   运算符   |    说明    |     应用举例     |       命令        |
| :--------: | :--------: | :--------------: | :---------------: |
|     +      |     加     |      $x+y$       |        x+y        |
|     -      |     减     |      $x-y$       |        x-y        |
|   \times   |    叉乘    |   $x \times y$   |    x \times y     |
|   \cdot    |    点乘    |   $x \cdot y$    |     x \cdot y     |
|  \ast(*)   |    星乘    |    $x \ast y$    | x \ast y or x * y |
|    \div    |     除     |    $x \div y$    |     x \div y      |
|    \pm     |    加减    |    $x \pm y$     |      x \pm y      |
|    \mp     |    减加    |    $x \mp y$     |      x \mp y      |
|     =      |    等于    |      $x=y$       |        x=y        |
|    \leq    |  小于等于  |    $x \leq y$    |     x \leq y      |
|    \geq    |  大于等于  |    $x \geq y$    |     x \geq y      |
|    \ll     |   远小于   |    $x \ll y$     |      x \ll y      |
|    \gg     |   远大于   |    $x \gg y$     |      x \gg y      |
|    \neq    |   不等于   |    $x \neq y$    |     x \neq y      |
|    \sim    |   相似于   |    $x \sim y$    |     x \sim y      |
|  \approx   |   约等于   |  $x \approx y$   |    x \approx y    |
|   \equiv   |   恒等于   |   $x \equiv y$   |    x \equiv y     |
|  \bigodot  | 定义运算符 |  $x \bigodot y$  |   x \bigodot y    |
| \bigotimes | 定义运算符 | $x \bigotimes y$ |  x \bigotimes y   |
|  \bullet   | 定义运算符 |  $x \bullet y$   |    x \bullet y    |
|   \oplus   |    异或    |   $x \oplus y$   |    x \oplus y     |

##### b.[集合](https://so.csdn.net/so/search?q=集合&spm=1001.2101.3001.7020)符号

|   运算符    |  说明  |    应用举例     |     命令      |
| :---------: | :----: | :-------------: | :-----------: |
|     \in     |  属于  |    $x \in y$    |    x \in y    |
|   \subset   |  子集  |  $x \subset y$  |  x \subset y  |
|  \subseteq  | 真子集 | $x \subseteq y$ | x \subseteq y |
|   \supset   |  超集  |  $x \supset y$  |  x \supset y  |
|  \supseteq  |  超集  | $x \supseteq y$ | x \supseteq y |
| \varnothing |  空集  |  $\varnothing$  |  \varnothing  |
|    \cup     |   并   |   $x \cup y$    |   x \cup y    |
|    \cap     |   交   |   $x \cap y$    |   x \cap y    |

##### c.字母修饰

|   运算符    |      说明      |                    应用举例                    |                     命令                     |
| :---------: | :------------: | :--------------------------------------------: | :------------------------------------------: |
|  \overline  | 平均数(上划线) |                 $\overline a$                  |                 \overline a                  |
| \underline  |     下划线     |                 $\underline a$                 |                 \underline a                 |
| \overbrace  |    上大括号    | $\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}$ | \overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0} |
| \underbrace |    下大括号    |              $\underbrace{a+d}_3$              |              \underbrace{a+d}_3              |
|   \hat{y}   |      帽子      |                   $\hat{y}$                    |                                              |

##### d.杂项

|     运算符      |        说明        |            应用举例             |             命令              |
| :-------------: | :----------------: | :-----------------------------: | :---------------------------: |
|    \partial     |       偏导数       | $\frac{\partial z}{\partial x}$ | \frac{\partial z}{\partial x} |
|     \ldots      |  底端对齐的省略号  |         $1,2,\ldots,n$          |         1,2,\ldots,n          |
|     \cdots      |  中线对齐的省略号  |         $1,2,\cdots,n$          |         1,2,\cdots,n          |
|    \uparrow     |       上箭头       |                ↑                |           \uparrow            |
|    \Uparrow     |      双上箭头      |           $\Uparrow$            |           \Uparrow            |
|   \downarrow    |       下箭头       |          $\downarrow$           |          \downarrow           |
|   \Downarrow    |      双下箭头      |                ⇓                |          \Downarrow           |
|   \leftarrow    |       左箭头       |          $\leftarrow$           |          \leftarrow           |
|   \Leftarrow    |      双左箭头      |          $\Leftarrow$           |          \Leftarrow           |
|   \rightarrow   |       右箭头       |          $\rightarrow$          |          \rightarrow          |
|   \Rightarrow   |      双右箭头      |          $\Rightarrow$          |          \Rightarrow          |
| \leftrightarrow |       双箭头       |        $\leftrightarrow$        |        \leftrightarrow        |
|   \triangleq    | 定义为$\triangleq$ |          $\triangleq$           |          \triangleq           |
|      \prec      |      拓扑表示      |             $\prec$             |             \prec             |
|      \succ      |      拓扑表示      |             $\succ$             |             \succ             |
|     \propto     |       正比于       |            $\propto$            |            \propto            |
|  \to`、`\gets   |     $\propto$      |          $\to、\gets$           |         \to`、`\gets          |
|    \nearrow     |      右上箭头      |           $\nearrow$            |           \nearrow            |
|    \searrow     |      右下箭头      |           $\searrow$            |           \searrow            |
|    \swarrow     |      左下箭头      |           $ \swarrow$           |           \swarrow            |
|    \nwarrow     |      左上箭头      |           $\nwarrow$            |           \nwarrow            |

##### f.对数$$

- 普通对数：`$\log_2{8}$` ：$log_2{8}$
- 自然对数：`$\ln 8$` ：$ln 8$
- 常用对数：`$\lg 100$` ：$lg 100$

##### g.取模

+ `$a\ mod\ b$`：$a\ mod\ b$

##### h.上取整与下取整

上取整：使用`\lceil` 和 `\rceil` 表示。 如，`\lceil x \rceil`:$\lceil x \rceil$。

下取整：使用`\lfloor` 和`\rfloor`表示。如，`\lfloor x \rfloor`：$\lfloor x \rfloor$。

##### i.标签

语法：`\tag{数字}`
$$
(a+b)(a-b)=a^2-b^2 \tag{1.1}
$$

##### j.最大、最小

最大：`\max_{x} y`
$$
\max_{x} y
$$
最小：`\min_{x} y`
$$
\min_{x} y
$$
arg max：`\mathop{\arg\max}_{x} y`
$$
\mathop{\arg\max}_{x} y
$$
arg min：`\mathop{\arg\min}_{x} y`
$$
\mathop{\arg\min}_{x} y
$$

##### k.统计估计

$$
\hat y
$$

##### l.绝对值与范数

- 绝对值：`\lvert x \rvert` =>$\lvert x \rvert$
- 范数：`\lVert x \rVert` => $\lVert x \rVert$

### 1.3 求和、累乘、极限与积分

#### 1.3.1 求和与累乘

+ 求和符号`\sum`：$\sum$
  + 举例：`\sum_{i=0}^n`显示为$\sum_{i=0}^n$
  + 举例：`\displaystyle\sum_{i=0}^n`显示为$\displaystyle\sum_{i=0}^n$
+ 累乘符号`\prod`：$\prod$
  + 举例：$\sum_{i=1}^n (i^2+2i+1)$
  + 举例：$\prod_{i=1}^n \frac{1}{i^2}$

#### 1.3.2 极限

+ 极限符号`\lim`显示为$\lim$
  + 举例：`\lim_{x\to\infty}`显示为$\lim_{x\to\infty}$
  + 举例：`\displaystyle\lim_{x\to\infty}`显示为$\displaystyle\lim_{x\to\infty}$

#### 1.3.3 积分

- 积分符号

  |  命令  |   显示   |
  | :----: | :------: |
  |  \int  |  $\int$  |
  | \iint  | $\iint$  |
  | \iiint | $\iiint$ |
  | \oint  | $\oint$  |

  + 举例:`\int_0^\infty{fxdx}`显示为$\int_0^{\infty}{fxdx}$

#### 1.3.4 导数

求导：`\mathrm{d} x`：$\frac{\mathrm{d} y } {\mathrm{d} x }$

梯度：`\nabla`：$\nabla f$

### 1.4 分式与根式

#### 1.4.1 分式

+ `\frac{公式1}{公式2}`显示为$\frac{公式1}{公式2}$或者`$1 \over 3$`
+ 例子：$$\frac{b_i^2}{a_i^2}$$和$$1 \over 3$$

#### 1.4.2 根式

+ `\sqrt[x]{y}`显示为$$\sqrt[x]{y}$$

### 1.5 特殊函数

+ `\函数名`

+ 例子：`\sin x`、`\ln x`、`\log_n^2 5`、`\max(A,B,C)`显示为$\sin x,\ln x,\log_n^2 5,\max(A,B,C)$

### 1.6 逻辑运算符

|  命令   |   显示    |   命令    |    显示     |
| :-----: | :-------: | :-------: | :---------: |
| \infty  | $\infty$  | \partial  | $\partial$  |
| \nabla  | $\nabla$  | \triangle | $\triangle$ |
| \forall | $\forall$ |  \exists  |  $\exists$  |
|  \lnot  |  $\lnot$  |  `land`   |   $\land$   |
|  \lor   |  $\lor$   |           |             |

示例1：$\frac{\partial f(x,y)}{\partial x}$

### 1.7 矩阵

#### 1.7.1 基本语法

+ 起始标记：`\begin{matrix}`

+ 结束标记：`\end{matrix}`

+ 每一行末尾标记`\\`，行间元素之间以`&`分隔

+ 举例：

  ```latex
  $$
  \begin{matrix} 
  1&0&0\\0&1&0\\0&0&1\\ 
  \end{matrix}
  $$
  ```

  $$\begin{matrix} 1&0&0\\0&1&0\\0&0&1\\ \end{matrix}$$

#### 1.7.2 矩阵边框

+ 在起始、结束标记处用下列词**替换matrix**

|    类型    |  命令   |                    矩阵边框显示效果                     |
| :--------: | :-----: | :-----------------------------------------------------: |
| 小括号边框 | pmatrix | $$\begin{pmatrix} 1&0&0\\0&1&0\\0&0&1\\ \end{pmatrix}$$ |
| 中括号边框 | bmatrix | $$\begin{bmatrix} 1&0&0\\0&1&0\\0&0&1\\ \end{bmatrix}$$ |
| 大括号边框 | Bmatrix | $$\begin{Bmatrix} 1&0&0\\0&1&0\\0&0&1\\ \end{Bmatrix}$$ |
| 单竖线边框 | vmatix  | $$\begin{vmatrix} 1&0&0\\0&1&0\\0&0&1\\ \end{vmatrix}$$ |
| 双竖线边框 | Vmatrix | $$\begin{Vmatrix} 1&0&0\\0&1&0\\0&0&1\\ \end{Vmatrix}$$ |

#### 1.7.3 省略元素

+ 横省略号：`\cdots`
+ 竖省略号：`\vdots`

+ 斜省略号：`\ddots`

```latex
$$\begin{bmatrix}
{a_{11}}&{a_{12}}&{\cdots}&{a_{1n}}\\
{a_{21}}&{a_{22}}&{\cdots}&{a_{2n}}\\
{\vdots}&{\vdots}&{\ddots}&{\vdots}\\
{a_{m1}}&{a_{m2}}&{\cdots}&{a_{mn}}\\
\end{bmatrix}$$
```

$$\begin{bmatrix}
{a_{11}}&{a_{12}}&{\cdots}&{a_{1n}}\\
{a_{21}}&{a_{22}}&{\cdots}&{a_{2n}}\\
{\vdots}&{\vdots}&{\ddots}&{\vdots}\\
{a_{m1}}&{a_{m2}}&{\cdots}&{a_{mn}}\\
\end{bmatrix}$$

### 1.8 阵列

- 需要array环境：起始、结束处以{array}声明

- 对齐方式：在`{array}`后以`{}`逐行统一声明

- 左对齐：l；居中：c；右对齐：r

- 竖直线：在声明对齐方式时，插入|建立竖直线

- 插入水平线：\hline

- 举例：

  ```latex
  $$\begin{array}{c|lll}
  {↓}&{a}&{b}&{c}\\
  \hline
  {R_1}&{c}&{b}&{a}\\
  {R_2}&{b}&{c}&{c}\\
  \end{array}$$
  ```

  $$\begin{array}{c|lll}
  {↓}&{a}&{b}&{c}\\
  \hline
  {R_1}&{c}&{b}&{a}\\
  {R_2}&{b}&{c}&{c}\\
  \end{array}$$

### 1.9 方程组

- 需要cases环境:起始、结束处以{cases}声明

- 举例：

  ```latex
  $$
  \begin{cases}
  a_1x+b_1y+c_1z=d_1\\
  a_2x+b_2y+c_2z=d_2\\
  a_3x+b_3y+c_3z=d_3\\
  \end{cases}
  $$
  ```
  
  $$\begin{cases}
  a_1x+b_1y+c_1z=d_1\\
  a_2x+b_2y+c_2z=d_2\\
  a_3x+b_3y+c_3z=d_3\\
  \end{cases}
  $$

### 1.10 分段函数

语法：

```latex
函数名=
\begin{cases}
公式1 & 条件1 \\
公式2 & 条件2 \\
公式3 & 条件3 
\end{cases}
```

$$
函数名=
\begin{cases}
公式1 & 条件1 \\
公式2 & 条件2 \\
公式3 & 条件3 
\end{cases}
$$

`&`表示对齐，`\\`表示换行

#### 公式推导过程

```latex
$$
\begin{aligned}
A&=B \\
&=C \\
&=D
\end{aligned}
$$
```

$$
\begin {aligned}
A&=B \\
&=C \\
&=D
\end {aligned}
$$

#### 并排显示两个公式

使用`\quad`或`\qquad`

```latex
$$
h(n)=
\begin{cases}
h_d(n) & 0\le n\le M-1 \\
0 & elsewhere 
\end{cases}
~~
and
~~
\alpha = \frac{M-1}{2}
$$
```

$$
h(n)=\begin{cases}
 h_d(n) & 0\le n\le M-1 \\
 0 & elsewhere 
 \end{cases}
 ~~
 and
 ~~
 \alpha = \frac{M-1}{2}
$$

#### 把括号放右边

```latex
\left.
\begin{array}{l}
\text{if $n$ is even:}&n/2\\
\text{if $n$ is odd:}&3n+1
\end{array}
\right\}
=f(n)
```

$$
\left.
\begin{array}{l}
\text{if $n$ is even:}&n/2\\
\text{if $n$ is odd:}&3n+1
\end{array}
\right\}
=f(n)
$$

#### 调整两行间距

让两行之间的间隔变得更大一些，就可以用 `\\[2ex]` 代替 `\\`。`ex`是指字母`x`的高度，`\\[2ex]`就表示两倍的字母`x`的高度。

```latex
f(n) =
\begin{cases}
\frac{n}{2}, & \text{if $n$ is even} \\[2ex]
3n+1, & \text{if $n$ is odd}
\end{cases}
```

$$
f(n) =
\begin{cases}
\frac{n}{2},  & \text{if $n$ is even} \\[2ex]
3n+1, & \text{if $n$ is odd}
\end{cases}
$$

### 1.11 特殊符号

