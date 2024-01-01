---
tags:
  - Lisp
  - Common-Lisp
  - CLHS
number headings: auto, first-level 1, max 6, 1.1
---
缩写:

|Abbreviation  |Meaning|
|:-------------|:------|
|adj.          |adjective|
|adv.          |adverb|
|ANSI          |compatible with one or more ANSI standards|
|Comp.         |computers|
|Idiom.        |idiomatic|
|IEEE          |compatible with one or more IEEE standards|
|ISO           |compatible with one or more ISO standards|
|Math.         |mathematics|
|Trad.         |traditional|
|n.            |noun|
|v.            |verb|
|v.t.          |transitive verb|
## 0.1 ()
> [!note] "()"
> n.
> 符号`nil`的另一个记法, 强调`nil`表示空列表.
## 0.2 absolute
> [!note] "绝对的"
> adj.
> 1 特定的时间点, 见[time](#time).
> 2 目录层次中特定位置, 见[pathname](#pathname).
> 见[relative](#relative)
## 0.3 access
> [!note] "访问"
> n., v.t.
> 1 读或写位置的值或数组中元素的值.
> 2 尝试访问位置的值.
> 见[place](#place), [value](#value), [array](#array)
## 0.4 accessibility
> [!note] "可访问性"
> n.
> 可访问的状态.
## 0.5 accessible
> [!note] "可访问的"
> adj.
> 1 (对象)被引用的能力.
> 2 (类的实现的共享或本地槽)已在实例的类或超类中定义.
> 3 (包中符号)在当前包中不使用包前缀可被引用的能力, 不管符号存在于包中还是继承获得的.
> 见[object](#object), [instance](#instance), [symbol](#symbol)
## 0.6 accessor
> [!note] "访问器"
> n.
> 执行访问的操作符.
> 见[operator](#operator), [reader](#reader), [writer](#writer)
## 0.7 active
> [!note] "活跃的"
> adj.
> 1 (处理器, 重启器或捕获标签)已被建立但还未被解除
> 2 (数组中元素)由大于等于0但小于填充指针的索引. 对没有填充指针的数组, 所有元素被认为是获取的.
> 见[handler](#handler), [restart](#restart), [catch tag](#catch tag), [fill pointer](#fill pointer)
## 0.8 actual adjustability
> [!note] "实际可调整性"
> n.
> 数组相关的一个广义布尔值, 标识数组是否是实际可调整的.
> 见[actually adjustable](#actually adjustable), [expressed adjustability](#expressed adjustability), [adjustable-array-p](../Symbols#adjustable-array-p)
## 0.9 actual argument
> [!note] "实参"
> n. Trad.
> 参数.
> 见[argument](#argument)
## 0.10 actual array element type
> [!note] "实际数组元素类型"
> n.
> 数组实际被特化后的类型, 是数组的被表达的数组元组类型的升级的数组元素类型.
> 见[array](#array), [array-element-type](../Symbols#array-element-type), [expressed array element type](#expressed array element type), [upgraded array element type](#upgraded array element type)
## 0.11 actual complex part type
> [!note] "实际复数部分类型"
> n.
> 复数的实部和虚部的实际表示的类型, 是复数的被表达的复数部分类型的升级的复数部分类型.
> 见[complext](#complext), [expressed complex part type ](#expressed complex part type ), [upgraded complex part type](#upgraded complex part type)
## 0.12 actual parameter
> [!note] "实参"
> n. Trad.
> 参数.
> 见[argument](#argument)
## 0.13 actually adjustable
> [!note] "实际可调整的"
> adj.
> 可用函数`ADJUST-ARRAY`直接修改数组特性. 需要满足: 数组被表达为可调整的 或 显式用`ADJUSTABLE-ARRY-P`测试.
> 见[expressly adjustable](#expressly adjustable), [adjust-array](../Symbols#adjust-array), [adjustable-array-p](../Symbols#adjustable-array-p)
## 0.14 adjustability
> [!note] "可调整性"
> n.
> 1 被表达的可调整性
> 2 实际可调整性
> 见[expressed adjustability](#expressed adjustability), [actual adjustability](#actual adjustability)
## 0.15 adjustable
> [!note] "可调整的"
> adj.
> 1 表达的可调整性
> 2 实际可调整性
> 见[expressly adjustable](#expressly adjustable), [actually adjustable](#actually adjustable)
## 0.16 after method
> [!note] ":after方法"
> n.
> 由限定符`:after`的方法.
> 见[method](#method), [qualifier](#qualifier)
## 0.17 alist
> [!note] "关联列表"
> n.
> 关联列表.
> 见[association list](#association list)
## 0.18 alphabetic
> [!note] "字母的"
> n. adj.
> 1 字符: 标准字符, 实现定义的字符, 图形字符
> 2 字符的要素特质, 见2.1.4.1和2.2
> 3 当前`readtable`中有语法类型要素和有要素特质的字符, 见图2-8
> 见[character](#character)
## 0.19 alphanumeric
> [!note] "字母或数字的"
> adj.
> 字母字符或数值字符.
> 见[alphabetic](#alphabetic), [numeric](#numeric)
## 0.20 ampersand
> [!note] "&"
> n.
> `&`的标准字符. 见图2-5.
> 见[standard character](#standard character)
## 0.21 anonymous
> [!note] "匿名的"
> adj.
> 1 (类或函数)没有名字
> 2 (重启器)有名字nil
> 见[mame](#name)
## 0.22 apparently uninterned
> [!note] "明显未内部化的"
> adj.
> 主包为`nil`.
> 见[home package](#home package)
## 0.23 applicable
> [!note] "可应用的"
> adj.
> 1 处理器可应用
> 2 方法可应用
> 3 重启器可应用
> 见[applicable handler](#applicable handler), [applicable method](#applicable method), [applicable restart](#applicable restart)
## 0.24 applicable handler
> [!note] "可应用的处理器"
> n.
> 活跃处理器关联的类型包含给定条件.
> 见[condition](#condition), [handler](#handler)
## 0.25 applicable method
> [!note] "可应用的方法"
> n.
> 广义函数的方法, 其参数满足参数特化符, 见7.6.6.1.1
> 见[method](#method), [parameter specializers](#parameter specializers)
## 0.26 applicable restart
> [!note] "可应用的重启器"
> n.
> 1 活跃处理器关联的测试在给定条件作为参数时返回真值
> 2 活跃处理器关联的测试在`nil`作为参数时返回真值
> 见[handler](#handler)
## 0.27 apply
> [!note] "APPLY函数"
> v.t.
> 使用列表中元素作为参数调用函数
> 见[call](#call), [function](#function)
## 0.28 argument
> [!note] "参数"
> n.
> 1 作为函数被调用时的数据
> 2 格式控制中的格式化参数
> 见[function](#function), [format argument](#format argument)
## 0.29 argument evaluation order
> [!note] "参数求值顺序"
> n.
> 参数在函数调用中的被求值的顺序, 见3.1
## 0.30 argument precedence order
> [!note] "参数优先级顺序"
> n.
> 广义函数排序可应用的方法时考虑的参数顺序
> 见[applicable method](#applicable method)
## 0.31 around method
> [!note] ":around方法"
> n.
> 有限定符`:around`的方法.
> 见[method](#method), [qualifier](#qualifier)
## 0.32 array
> [!note] "数组"
> n.
> 有类型`ARRAY`的对象
## 0.33 array element type
> [!note] "数组元素类型"
> n.
> 1 数组关联的类型
> 2 数组的实际数据元素类型
> 3 数组的被表达的数组元素类型
> 见[actual array element type](#actual array element type), [expressed array element type](#expressed array element type)
## 0.34 array total size
> [!note] "数组总大小"
> n.
> 数组中元素总数量, 按数组维度之积计算.
> 见[dimension](#dimension)
## 0.35 assign
> [!note] "赋值"
> v.t.
> 改变已建立的绑定中变量的值.
> 见[binding](#binding), [variable](#variable), [setq](../Symbols#setq)
## 0.36 association list
> [!note] "关联列表"
> n.
> 表示关联的键值的cons列表, 每个cons的car是键, cdr是键对应的值.
> 见[cons](#cons)
## 0.37 asterisk
> [!note] "*"
> n.
> 标准字符`*`, 见图2-5.
## 0.38 at-sign
> [!note] "@"
> n.
> 标准字符`@`, 见图2-5.
## 0.39 atom
> [!note] "原子"
> n.
> 不是cons的对象
> 见[](#)
## 0.40 atomic
> [!note] "原子的"
> adj.
> 原子的.
> 见[atom](#atom)
## 0.41 atomic type specifier
> [!note] "原子类型描述符"
> n.
> 对每个原子类型描述符`x`, 存在一个等价的的复合类型描述符`(x)`
> 见[compound type specifier](#compound type specifier)
## 0.42 attribute
> [!note] "属性"
> n.
> 字符的程序可见的方面, 字符的标准属性是其编码, 见13.1.3
> 见[code](#code)
## 0.43 aux variable
> [!note] "辅助变量"
> n.
> 在lambda列表中由`&aux`引入的变量, 辅助变量不是参数.
> 见[lambda list](#lambda list)
## 0.44 auxiliary method
> [!note] "辅助方法"
> n.
> 构成方法对应的广义函数的完备方法集合中的一个方法.
> 见[primary methods](#primary methods), [method combination](#method combination)
## 0.45 backquote

## 0.46 backslash
> [!note] "\\"
> n.
> `\`, 称为逆斜线(reverse solidus)或反斜线(backslash). 见图2-5.
## 0.47 base character

## 0.48 base string

## 0.49 before method

## 0.50 bidirectional

## 0.51 binary

## 0.52 bind

## 0.53 binding

## 0.54 bit

## 0.55 bit array

## 0.56 bit vector

## 0.57 bit-wise logical operation specifier

## 0.58 block

## 0.59 block tag

## 0.60 boa lambda list

## 0.61 body parameter

## 0.62 boolean

## 0.63 boolean equivalent

## 0.64 bound

## 0.65 bound declaration

## 0.66 bounded

## 0.67 bounding index

## 0.68 bounding index designator

## 0.69 break loop

## 0.70 broadcast stream

## 0.71 built-in class

## 0.72 built-in type

## 0.73 byte

## 0.74 byte specifier

## 0.75 cadr

## 0.76 call

## 0.77 captured initialization form

## 0.78 car

## 0.79 case

## 0.80 case sensitivity mode

## 0.81 catch

## 0.82 catch tag

## 0.83 cddr

## 0.84 cdr

## 0.85 cell

## 0.86 character

## 0.87 character code

## 0.88 character designator

## 0.89 circular

## 0.90 circular list

## 0.91 class

## 0.92 class designator

## 0.93 class precedence list

## 0.94 close

## 0.95 closed

## 0.96 closure

## 0.97 coalesce

## 0.98 code

## 0.99 coerce

## 0.100 colon

## 0.101 comma

## 0.102 compilation

## 0.103 compilation environment

## 0.104 compilation unit

## 0.105 compile

## 0.106 compile time

## 0.107 compile-time definition

## 0.108 compiled code

## 0.109 compiled file

## 0.110 compiled function

## 0.111 compiler

## 0.112 compiler macro

## 0.113 compiler macro expansion

## 0.114 compiler macro form

## 0.115 compiler macro function

## 0.116 complex

## 0.117 complex float

## 0.118 complex part type

## 0.119 complex rational

## 0.120 complex single float

## 0.121 composite stream

## 0.122 compound form

## 0.123 compound type specifier

## 0.124 concatenated stream

## 0.125 condition

## 0.126 condition designator

## 0.127 condition handler

## 0.128 condition reporter

## 0.129 conditional newline

## 0.130 conformance

## 0.131 conforming code

## 0.132 conforming implementation

## 0.133 conforming processor

## 0.134 conforming program

## 0.135 congruent

## 0.136 cons

## 0.137 constant

## 0.138 constant form

## 0.139 constant object

## 0.140 constant variable

## 0.141 constituent

## 0.142 constituent trait

## 0.143 constructed stream

## 0.144 contagion

## 0.145 continuable

## 0.146 control form

## 0.147 copy

## 0.148 correctable

## 0.149 current input base

## 0.150 current logical block

## 0.151 current output base

## 0.152 current package

## 0.153 current pprint dispatch table

## 0.154 current random state

## 0.155 current readtable

## 0.156 data type

## 0.157 debug I/O

## 0.158 debugger

## 0.159 declaration

## 0.160 declaration identifier

## 0.161 declaration specifier

## 0.162 declare

## 0.163 decline

## 0.164 decoded time

## 0.165 default method

## 0.166 defaulted initialization argument list

## 0.167 define-method-combination arguments lambda list

## 0.168 define-modify-macro lambda list

## 0.169 defined name

## 0.170 defining form

## 0.171 defsetf lambda list

## 0.172 deftype lambda list

## 0.173 denormalized

## 0.174 derived type

## 0.175 derived type specifier

## 0.176 designator

## 0.177 destructive

## 0.178 destructuring lambda list

## 0.179 different

## 0.180 digit

## 0.181 dimension

## 0.182 direct instance

## 0.183 direct subclass

## 0.184 direct superclass

## 0.185 disestablish

## 0.186 disjoint

## 0.187 dispatching macro character

## 0.188 displaced array

## 0.189 distinct

## 0.190 documentation string

## 0.191 dot

## 0.192 dotted list

## 0.193 dotted pair

## 0.194 double float

## 0.195 double-quote

## 0.196 dynamic binding

## 0.197 dynamic environment

## 0.198 dynamic extent

## 0.199 dynamic scope

## 0.200 dynamic variable

## 0.201 echo stream

## 0.202 effective method

## 0.203 element

## 0.204 element type

## 0.205 em

## 0.206 empty list

## 0.207 empty type

## 0.208 end of file

## 0.209 environment

## 0.210 environment object

## 0.211 environment parameter

## 0.212 error

## 0.213 error output

## 0.214 escape

## 0.215 establish

## 0.216 evaluate

## 0.217 evaluation

## 0.218 evaluation environment

## 0.219 execute

## 0.220 execution time

## 0.221 exhaustive partition

## 0.222 exhaustive union

## 0.223 exit point

## 0.224 explicit return

## 0.225 explicit use

## 0.226 exponent marker

## 0.227 Marker  Meaning

## 0.228 D or d  double-float

## 0.229 E or e  float (see *read-default-float-format*)

## 0.230 F or f  single-float

## 0.231 L or l  long-float

## 0.232 S or s  short-float

## 0.233 Figure 26-1. Exponent Markers

## 0.234 export

## 0.235 exported

## 0.236 expressed adjustability

## 0.237 expressed array element type

## 0.238 expressed complex part type

## 0.239 expression

## 0.240 expressly adjustable

## 0.241 extended character

## 0.242 extended function designator

## 0.243 extended lambda list

## 0.244 extension

## 0.245 extent

## 0.246 external file format

## 0.247 external file format designator

## 0.248 external symbol

## 0.249 externalizable object

## 0.250 false

## 0.251 fbound

## 0.252 feature

## 0.253 feature expression

## 0.254 features list

## 0.255 file

## 0.256 file compiler

## 0.257 file position

## 0.258 file position designator

## 0.259 file stream

## 0.260 file system

## 0.261 filename

## 0.262 fill pointer

## 0.263 finite

## 0.264 fixnum

## 0.265 float

## 0.266 for-value

## 0.267 form
> [!note]
> n.
> 1 要被求值的对象.
> 2 一个符号, 一个复合形式或一个自求值对象.
> 3 一个复合形式, 首元素是操作符, 例如`quote`形式是个常量形式.
> 见[symbol](#symbol), [compound form](#compound form), [self-evaluating object](#self-evaluating object), [operator](#operator).
## 0.268 formal argument

## 0.269 formal parameter

## 0.270 format

## 0.271 format argument

## 0.272 format control

## 0.273 format directive

## 0.274 format string

## 0.275 free declaration

## 0.276 fresh

## 0.277 freshline

## 0.278 funbound

## 0.279 function

## 0.280 function block name

## 0.281 function cell

## 0.282 function designator

## 0.283 function form

## 0.284 function name

## 0.285 functional evaluation

## 0.286 functional value

## 0.287 further compilation

## 0.288 general

## 0.289 generalized boolean

## 0.290 generalized instance

## 0.291 generalized reference

## 0.292 generalized synonym stream

## 0.293 generic function

## 0.294 generic function lambda list

## 0.295 gensym

## 0.296 global declaration

## 0.297 global environment

## 0.298 global variable

## 0.299 glyph

## 0.300 go

## 0.301 go point one of possibly several exit points that are established by tagbody (or other abstractions, such as prog, which are built from tagbody).

## 0.302 go tag

## 0.303 graphic

## 0.304 handle

## 0.305 handler

## 0.306 hash table

## 0.307 home package

## 0.308 I/O customization variable

## 0.309 *debug-io*        *error-io*         query-io*

## 0.310 *standard-input*  *standard-output*  *trace-output*

## 0.311 Figure 26-2. Standardized I/O Customization Variables

## 0.312 identical

## 0.313 identifier

## 0.314 immutable

## 0.315 implementation

## 0.316 implementation limit

## 0.317 implementation-defined

## 0.318 implementation-dependent

## 0.319 implementation-independent

## 0.320 implicit block

## 0.321 implicit compilation

## 0.322 implicit progn

## 0.323 implicit tagbody

## 0.324 import

## 0.325 improper list

## 0.326 inaccessible

## 0.327 indefinite extent

## 0.328 indefinite scope

## 0.329 indicator

## 0.330 indirect instance

## 0.331 inherit

## 0.332 initial pprint dispatch table

## 0.333 initial readtable

## 0.334 initialization argument list

## 0.335 initialization form

## 0.336 input

## 0.337 instance

## 0.338 integer

## 0.339 interactive stream

## 0.340 intern

## 0.341 internal symbol

## 0.342 internal time

## 0.343 internal time unit

## 0.344 interned

## 0.345 interpreted function

## 0.346 interpreted implementation

## 0.347 interval designator

## 0.348 invalid

## 0.349 iteration form

## 0.350 iteration variable

## 0.351 key

## 0.352 keyword

## 0.353 keyword parameter

## 0.354 keyword/value pair

## 0.355 lambda combination

## 0.356 lambda expression

## 0.357 lambda form

## 0.358 lambda list

## 0.359 lambda list keyword

## 0.360 lambda variable

## 0.361 leaf

## 0.362 leap seconds

## 0.363 left-parenthesis

## 0.364 length

## 0.365 lexical binding

## 0.366 lexical closure

## 0.367 lexical environment

## 0.368 lexical scope

## 0.369 lexical variable

## 0.370 Lisp image

## 0.371 Lisp printer

## 0.372 Lisp read-eval-print loop

## 0.373 Lisp reader

## 0.374 list

## 0.375 list designator

## 0.376 list structure

## 0.377 literal

## 0.378 load

## 0.379 load time

## 0.380 load time value

## 0.381 loader

## 0.382 local declaration

## 0.383 local precedence order

## 0.384 local slot

## 0.385 logical block

## 0.386 logical host

## 0.387 logical host designator

## 0.388 logical pathname

## 0.389 long float

## 0.390 loop keyword

## 0.391 lowercase

## 0.392 macro
> [!note]
> n.
> 1 一个宏形式.
> 2 一个宏函数.
> 3 一个宏的名称.
> 见[macro form](#macro form), [macro function](#macro function), [macro name](#macro name).
## 0.393 macro character
> [!note]
> n.
> 一个字符, 当Lisp读取器在其主分发循环中遇到时, 引入读取器宏.
> 宏字符与宏没有关系.
> 见[](#)
## 0.394 macro expansion
> [!note]
> n.
> 1 将宏形式转换为另一个形式的过程.
> 2 作为该过程结果产生的宏.
> 见[reader macro](#reader macro).
## 0.395 macro form
> [!note]
> n.
> 代表另一个形式的形式(为了抽象、信息隐藏、语法遍历), 即或者是首元素为宏名称的复合形式, 或者是一个命名了符号宏的符号的形式.
> 见[compound form](#compound form), [macro name](#macro name), [symbol macro](#symbol macro).
## 0.396 macro function
> [!note]
> n.
> 一个有两个参数的函数: 形式和环境, 这个函数实现了宏扩展, 生成作为原始参数的形式求值后的形式.
> 见[form](#form), [environment](#environment), [macro expansion](#macro expansion).
## 0.397 macro lambda list
> [!note]
> n.
> 用在形式中以建立宏定义的扩展的lambda列表, 例如`defmacro`、`macrolet`.
> 见[3.4.4 宏lambda列表](../03-Evaluation-and-Compilation#3.4.4)
## 0.398 macro name
> [!note]
> n.
> 一个名称, 作为`macro-function`参数时返回true,
> 用在复合形式的首元素处, 标识该形式为宏形式.
> 见[macro-function](../Symbols#macro-function), [macro form](#macro form).
## 0.399 macroexpand hook
> [!note]
> n.
> `*macroexpand-hook*`的值对应的函数.
> 见[`*macroexpand-hook*`](../Symbols#*macroexpand-hook*)
## 0.400 mapping

## 0.401 metaclass

## 0.402 Metaobject Protocol

## 0.403 method

## 0.404 method combination

## 0.405 method-defining form

## 0.406 method-defining operator

## 0.407 minimal compilation

## 0.408 modified lambda list

## 0.409 most recent

## 0.410 multiple escape

## 0.411 multiple values

## 0.412 name

## 0.413 named constant

## 0.414 namespace

## 0.415 namestring

## 0.416 newline

## 0.417 next method

## 0.418 nickname

## 0.419 nil

## 0.420 non-atomic

## 0.421 non-constant variable

## 0.422 non-correctable

## 0.423 non-empty

## 0.424 non-generic function

## 0.425 non-graphic

## 0.426 non-list

## 0.427 non-local exit

## 0.428 non-nil

## 0.429 non-null lexical environment

## 0.430 non-simple

## 0.431 non-terminating

## 0.432 non-top-level form

## 0.433 normal return

## 0.434 normalized

## 0.435 null

## 0.436 null lexical environment

## 0.437 number

## 0.438 numeric

## 0.439 object

## 0.440 object-traversing

## 0.441 open

## 0.442 operator

## 0.443 optimize quality

## 0.444 optional parameter

## 0.445 ordinary function

## 0.446 ordinary lambda list

## 0.447 otherwise inaccessible part

## 0.448 output

## 0.449 package

## 0.450 package cell

## 0.451 package designator

## 0.452 package marker

## 0.453 package prefix

## 0.454 package registry

## 0.455 pairwise

## 0.456 parallel

## 0.457 parameter

## 0.458 parameter specializer

## 0.459 parameter specializer name

## 0.460 pathname

## 0.461 pathname designator

## 0.462 physical pathname

## 0.463 place

## 0.464 plist

## 0.465 portable

## 0.466 potential copy

## 0.467 potential number
> [!note] "可能的数值"
> n.
> 在一些符合标准的实现中被Lisp读取器解析为数值的文本内容, 但不要求被解析为数值.
> 没有对象是可能的数值: 一个对象或者是数值, 或者不是, 见[2.3.1.1 可能的数值的记号](../02-Syntax#2.3.1.1).
> 见[number](#number)
## 0.468 pprint dispatch table

## 0.469 predicate

## 0.470 present

## 0.471 pretty print

## 0.472 pretty printer

## 0.473 pretty printing stream

## 0.474 primary method

## 0.475 primary value

## 0.476 principal

## 0.477 print name

## 0.478 printer control variable

## 0.479 printer escaping

## 0.480 printing

## 0.481 process

## 0.482 processor

## 0.483 proclaim

## 0.484 proclamation

## 0.485 prog tag

## 0.486 program

## 0.487 programmer

## 0.488 programmer code

## 0.489 proper list

## 0.490 proper name

## 0.491 proper sequence

## 0.492 proper subtype

## 0.493 property

## 0.494 property indicator

## 0.495 property list

## 0.496 property value

## 0.497 purports to conform

## 0.498 qualified method

## 0.499 qualifier

## 0.500 query I/O

## 0.501 quoted object

## 0.502 radix

## 0.503 random state

## 0.504 rank

## 0.505 ratio

## 0.506 ratio marker

## 0.507 rational

## 0.508 read

## 0.509 readably

## 0.510 reader

## 0.511 reader macro

## 0.512 reader macro function

## 0.513 readtable

## 0.514 readtable case

## 0.515 readtable designator

## 0.516 recognizable subtype

## 0.517 reference

## 0.518 registered package

## 0.519 relative

## 0.520 repertoire

## 0.521 report

## 0.522 report message

## 0.523 required parameter

## 0.524 rest list

## 0.525 rest parameter

## 0.526 restart

## 0.527 restart designator

## 0.528 restart function

## 0.529 abort     muffle-warning  use-value

## 0.530 continue  store-value

## 0.531 Figure 26-4. Standardized Restart Functions

## 0.532 return

## 0.533 return value

## 0.534 right-parenthesis

## 0.535 Rubout
> [!note]
> n.
> 删除字符.
> 见[13.1.7 字符名称](../13-Characters#13.1.7)
## 0.536 run time

## 0.537 run-time compiler

## 0.538 run-time definition

## 0.539 run-time environment

## 0.540 safe

## 0.541 safe call

## 0.542 same

## 0.543 satisfy the test

## 0.544 scope

## 0.545 script

## 0.546 secondary value

## 0.547 section

## 0.548 self-evaluating object

## 0.549 semi-standard

## 0.550 semicolon

## 0.551 sequence

## 0.552 sequence function

## 0.553 sequential

## 0.554 sequentially

## 0.555 serious condition

## 0.556 session

## 0.557 set

## 0.558 setf expander

## 0.559 setf expansion

## 0.560 setf function

## 0.561 setf function name

## 0.562 shadow

## 0.563 shadowing symbol

## 0.564 shadowing symbols list

## 0.565 shared slot

## 0.566 sharpsign
> [!note] "#"
> n.
> 井号符号. 见图2-5.
> 见[standard character](#standard character)
## 0.567 short float

## 0.568 sign

## 0.569 signal

## 0.570 signature

## 0.571 similar

## 0.572 similarity

## 0.573 simple

## 0.574 simple array

## 0.575 simple bit array

## 0.576 simple bit vector

## 0.577 simple condition

## 0.578 simple general vector

## 0.579 simple string

## 0.580 simple vector

## 0.581 single escape

## 0.582 single float

## 0.583 single-quote

## 0.584 singleton

## 0.585 situation

## 0.586 slash

## 0.587 slot

## 0.588 slot specifier

## 0.589 source code

## 0.590 source file

## 0.591 space

## 0.592 special form
> [!note]
> n
> 不是宏形式的一个列表, 是一个有特殊语法或特殊求值规则形式, 可能操作求值环境或控制流.
> 特殊形式的首个元素是特殊操作符.
> 见[form](#form), [macro form](#macro form), [evaluation](#evaluation), [special operator](#special operator).
## 0.593 special operator
> [!note]
> 图3-2中列举的一组固定符号, 出现在形式的car中将该形式标识为特殊形式..
> 见[symbol](#symbol), [special form](#special form).
## 0.594 special variable

## 0.595 specialize

## 0.596 specialized

## 0.597 specialized lambda list

## 0.598 spreadable argument list designator

## 0.599 stack allocate

## 0.600 stack-allocated

## 0.601 standard character

## 0.602 standard class

## 0.603 standard generic function a function of type standard-generic-function.

## 0.604 standard input

## 0.605 standard method combination

## 0.606 standard object

## 0.607 standard output

## 0.608 standard pprint dispatch table

## 0.609 standard readtable

## 0.610 standard syntax

## 0.611 standardized

## 0.612 startup environment

## 0.613 step

## 0.614 stream

## 0.615 stream associated with a file

## 0.616 stream designator

## 0.617 stream element type

## 0.618 stream variable

## 0.619 stream variable designator

## 0.620 string

## 0.621 string designator

## 0.622 string equal

## 0.623 string stream

## 0.624 structure

## 0.625 structure class

## 0.626 structure name

## 0.627 style warning

## 0.628 subclass

## 0.629 subexpression

## 0.630 subform

## 0.631 subrepertoire

## 0.632 subtype

## 0.633 superclass

## 0.634 supertype

## 0.635 supplied-p parameter

## 0.636 symbol

## 0.637 symbol macro

## 0.638 synonym stream

## 0.639 synonym stream symbol

## 0.640 syntax type

## 0.641 system class

## 0.642 system code

## 0.643 t

## 0.644 tag

## 0.645 tail

## 0.646 target

## 0.647 terminal I/O

## 0.648 terminating

## 0.649 tertiary value

## 0.650 throw

## 0.651 tilde

## 0.652 time

## 0.653 time zone

## 0.654 token
> [!note] "记号"
> 数值或符号的文本表示. 见[2.3 解释记号](../02-Syntax#2.3)
> 见[number](#number), [symbol](#symbol)
## 0.655 top level form

## 0.656 trace output

## 0.657 tree

## 0.658 tree structure

## 0.659 true

## 0.660 truename

## 0.661 two-way stream

## 0.662 type

## 0.663 type declaration

## 0.664 type equivalent

## 0.665 type expand

## 0.666 type specifier

## 0.667 unbound

## 0.668 unbound variable

## 0.669 undefined function

## 0.670 unintern

## 0.671 uninterned

## 0.672 universal time

## 0.673 unqualified method

## 0.674 unregistered package

## 0.675 unsafe

## 0.676 unsafe call

## 0.677 upgrade

## 0.678 upgraded array element type

## 0.679 upgraded complex part type

## 0.680 uppercase

## 0.681 use

## 0.682 use list

## 0.683 user

## 0.684 valid array dimension

## 0.685 valid array index

## 0.686 valid array row-major index

## 0.687 valid fill pointer

## 0.688 valid logical pathname host

## 0.689 valid pathname device

## 0.690 valid pathname directory

## 0.691 valid pathname host

## 0.692 valid pathname name

## 0.693 valid pathname type

## 0.694 valid pathname version

## 0.695 valid physical pathname host

## 0.696 valid sequence index

## 0.697 value

## 0.698 value cell

## 0.699 variable

## 0.700 vector

## 0.701 vertical-bar
> [!note] "|"
> n.
> `|`, 称为竖线的标准字符.
> 见[](#)
## 0.702 whitespace

## 0.703 wild

## 0.704 write

## 0.705 writer

## 0.706 yield
