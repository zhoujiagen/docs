---
tags:
  - Lisp
  - Common-Lisp
  - CLHS
---

> There are 978 symbols in the `COMMON-LISP` package.
# 1 `&allow-other-keys`
# 2 `&aux`
# 3 `&body`
# 4 `&environment`
# 5 `&key`
# 6 `&optional`
# 7 `&rest`
# 8 `&whole`
# 9 ``*``
# 10 ``**``
# 11 ``***``
# 12 ``*break-on-signals*``
# 13 ``*compile-file-pathname*``
# 14 ``*compile-file-truename*``
# 15 ``*compile-print*``
# 16 ``*compile-verbose*``
# 17 ``*debug-io*``
# 18 ``*debugger-hook*``
# 19 ``*default-pathname-defaults*``
# 20 ``*error-output*``
# 21 ``*features*``
# 22 ``*gensym-counter*``
# 23 ``*load-pathname*``
# 24 ``*load-print*``
# 25 ``*load-truename*``
# 26 ``*load-verbose*``
# 27 ``*macroexpand-hook*``
# 28 ``*modules*``
# 29 ``*package*``
# 30 ``*print-array*``
# 31 ``*print-base*``
# 32 ``*print-case*``
# 33 ``*print-circle*``
# 34 ``*print-escape*``
# 35 ``*print-gensym*``
# 36 ``*print-length*``
# 37 ``*print-level*``
# 38 ``*print-lines*``
# 39 ``*print-miser-width*``
# 40 ``*print-pprint-dispatch*``
# 41 ``*print-pretty*``
# 42 ``*print-radix*``
# 43 ``*print-readably*``
# 44 ``*print-right-margin*``
# 45 ``*query-io*``
# 46 ``*random-state*``
# 47 ``*read-base*``
# 48 ``*read-default-float-format*``
# 49 ``*read-eval*``
# 50 ``*read-suppress*``
# 51 ``*readtable*``
# 52 ``*standard-input*``
# 53 ``*standard-output*``
# 54 ``*terminal-io*``
# 55 ``*trace-output*``
# 56 ``+``
# 57 ``++``
# 58 ``+++``
# 59 ``-``
# 60 ``/``
# 61 ``//``
# 62 ``///``
# 63 ``/=``
# 64 ``1+``
# 65 ``1-``
# 66 ``<``
# 67 ``<=``
# 68 ``=``
# 69 ``>``
# 70 ``>=``
# 71 `abort`
# 72 `abs`
# 73 `acons`
# 74 `acos`
# 75 `acosh`
# 76 `add-method`
# 77 `adjoin`

> [!note] "Function"
**Syntax**:

``` lisp
adjoin item list &key key test test-not => new-list
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 78 `adjust-array`
# 79 `adjustable-array-p`
# 80 `allocate-instance`
# 81 `alpha-char-p`
# 82 `alphanumericp`
# 83 `and`

> [!tip] "Macro"
**Syntax**:

``` lisp
and form* => result*
```

**Arguments and Values**:

- `form`: 一个形式
- `results`: 最后一个`form`的求值结果, 或符号`nil`, 或`t`

**Description**:

宏`and`按 **从左至右** 的顺序一次求值一个`form`.
一旦任意形式求值为`nil`, `and`不再对剩下的`form`求值直接返回`nil`.
如果除最后一个外所有的`form`求值为true, `and`返回求值最后一个`form`的结果.

如果没有提供`form`, `(and)`返回`t`.

`and`可以返回最后一个子形式的多值.

**Examples**:

``` lisp
(if (and (>= n 0)
			 (< n (length a-simple-vector))
			 (eq (elt a-simple-vector n) 'foo))
	(princ "Foo!"))
```

如果`a-simple-vector`的`n`位置元素是符号`foo`, `n`对`a-simple-vector`是有效的索引, 则上述表达式输出`Foo!`. 如果`n`越界, 因为`and`保证从左至右的顺序测试其内容部分, `elt`不被调用.

``` lisp
(setq temp1 1 temp2 1 temp3 1) =>  1
(and (incf temp1) (incf temp2) (incf temp3)) =>  2
(and (eql 2 temp1) (eql 2 temp2) (eql 2 temp3)) =>  true
(decf temp3) =>  1

; (eq temp3 'nil)求值为false, (decf temp3)不被执行
(and (decf temp1) (decf temp2) (eq temp3 'nil) (decf temp3)) =>  NIL

(and (eql temp1 temp2) (eql temp2 temp3)) =>  true
(and) =>  T
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[cond](#cond), [every](#every), [if](#if), [or](#or), [when](#when)

**Notes**:

``` lisp
(and form) ==  (let () form)
(and form1 form2 ...) ==  (when form1 (and form2 ...))
```


# 84 `append`
# 85 `apply`
# 86 `apropos`
# 87 `apropos-list`
# 88 `aref`
# 89 `arithmetic-error`
# 90 `arithmetic-error-operands`
# 91 `arithmetic-error-operation`
# 92 `array`
# 93 `array-dimension`
# 94 `array-dimension-limit`
# 95 `array-dimensions`
# 96 `array-displacement`
# 97 `array-element-type`
# 98 `array-has-fill-pointer-p`
# 99 `array-in-bounds-p`
# 100 `array-rank`
# 101 `array-rank-limit`
# 102 `array-row-major-index`
# 103 `array-total-size`
# 104 `array-total-size-limit`
# 105 `arrayp`
# 106 `ash`
# 107 `asin`
# 108 `asinh`
# 109 `assert`
# 110 `assoc`
# 111 `assoc-if`
# 112 `assoc-if-not`
# 113 `atan`
# 114 `atanh`
# 115 `atom`

> [!note] "Function"
**Syntax**:

``` lisp
atom object => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 116 `base-char`
# 117 `base-string`
# 118 `bignum`
# 119 `bit`
# 120 `bit-and`
# 121 `bit-andc1`
# 122 `bit-andc2`
# 123 `bit-eqv`
# 124 `bit-ior`
# 125 `bit-nand`
# 126 `bit-nor`
# 127 `bit-not`
# 128 `bit-orc1`
# 129 `bit-orc2`
# 130 `bit-vector`
# 131 `bit-vector-p`
# 132 `bit-xor`
# 133 `block`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
block name form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 134 `boole`
# 135 `boole-1`
# 136 `boole-2`
# 137 `boole-and`
# 138 `boole-andc1`
# 139 `boole-andc2`
# 140 `boole-c1`
# 141 `boole-c2`
# 142 `boole-clr`
# 143 `boole-eqv`
# 144 `boole-ior`
# 145 `boole-nand`
# 146 `boole-nor`
# 147 `boole-orc1`
# 148 `boole-orc2`
# 149 `boole-set`
# 150 `boole-xor`
# 151 `boolean`
# 152 `both-case-p`
# 153 `boundp`
# 154 `break`
# 155 `broadcast-stream`
# 156 `broadcast-stream-streams`
# 157 `built-in-class`
# 158 `butlast`
# 159 `byte`
# 160 `byte-position`
# 161 `byte-size`

# 162 `call-arguments-limit`
# 163 `call-method`
# 164 `call-next-method`
# 165 `cdr`

> [!tip] "Accessor"
**Syntax**:

``` lisp
car x => object
cdr x => object
caar x => object
cadr x => object
cdar x => object
cddr x => object
caaar x => object
caadr x => object
cadar x => object
caddr x => object
cdaar x => object
cdadr x => object
cddar x => object
cdddr x => object
caaaar x => object
caaadr x => object
caadar x => object
caaddr x => object
cadaar x => object
cadadr x => object
caddar x => object
cadddr x => object
cdaaar x => object
cdaadr x => object
cdadar x => object
cdaddr x => object
cddaar x => object
cddadr x => object
cdddar x => object
cddddr x => object
(setf (car x) new-object)
(setf (cdr x) new-object)
(setf (caar x) new-object)
(setf (cadr x) new-object)
(setf (cdar x) new-object)
(setf (cddr x) new-object)
(setf (caaar x) new-object)
(setf (caadr x) new-object)
(setf (cadar x) new-object)
(setf (caddr x) new-object)
(setf (cdaar x) new-object)
(setf (cdadr x) new-object)
(setf (cddar x) new-object)
(setf (cdddr x) new-object)
(setf (caaaar x) new-object)
(setf (caaadr x) new-object)
(setf (caadar x) new-object)
(setf (caaddr x) new-object)
(setf (cadaar x) new-object)
(setf (cadadr x) new-object)
(setf (caddar x) new-object)
(setf (cadddr x) new-object)
(setf (cdaaar x) new-object)
(setf (cdaadr x) new-object)
(setf (cdadar x) new-object)
(setf (cdaddr x) new-object)
(setf (cddaar x) new-object)
(setf (cddadr x) new-object)
(setf (cdddar x) new-object)
(setf (cddddr x) new-object)
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 166 `case`
# 167 `catch`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
catch tag form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 168 `ccase`
# 169 `ftruncate`

> [!note] "Function"
**Syntax**:

``` lisp
floor number &optional divisor => quotient, remainder
ffloor number &optional divisor => quotient, remainder
ceiling number &optional divisor => quotient, remainder
fceiling number &optional divisor => quotient, remainder
truncate number &optional divisor => quotient, remainder
ftruncate number &optional divisor => quotient, remainder
round number &optional divisor => quotient, remainder
fround number &optional divisor => quotient, remainder
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 170 `cell-error`
# 171 `cell-error-name`
# 172 `cerror`
# 173 `change-class`
# 174 `char`
# 175 `char-code`
# 176 `char-code-limit`
# 177 `char-downcase`
# 178 `char-equal`
# 179 `char-greaterp`
# 180 `char-int`
# 181 `char-lessp`
# 182 `char-name`
# 183 `char-not-equal`
# 184 `char-not-greaterp`
# 185 `char-not-lessp`
# 186 `char-upcase`
# 187 `char/=`
# 188 `char<`
# 189 `char<=`
# 190 `char=`
# 191 `char>`
# 192 `char>=`
# 193 `character`
# 194 `characterp`
# 195 `check-type`
# 196 `cis`
# 197 `class`
# 198 `class-name`
# 199 `class-of`
# 200 `clear-input`
# 201 `clear-output`
# 202 `close`
# 203 `clrhash`
# 204 `code-char`
# 205 `coerce`
# 206 `compilation-speed`
# 207 `compile`
# 208 `compile-file`
# 209 `compile-file-pathname`
# 210 `compiled-function`
# 211 `compiled-function-p`
# 212 `compiler-macro`
# 213 `compiler-macro-function`
# 214 `complement`
# 215 `complex`
# 216 `complexp`
# 217 `compute-applicable-methods`
# 218 `compute-restarts`
# 219 `concatenate`
# 220 `concatenated-stream`
# 221 `concatenated-stream-streams`
# 222 `cond`

> [!tip] "Macro"
**Syntax**:

``` lisp
cond {clause}* => result*

clause::= (test-form form*)
```

**Arguments and Values**:

- `test-form`: 一个形式
- `forms`: 隐式的`progn`
- `results`: (1) 首个`test-form`为true的`clause`的`forms`的值, 或者(2) 该`clause`中没有`forms`时`test-form`的主值, 或者(3) 没有`test-form`为true时为`nil`

**Description**:

`cond`允许依赖于`test-form`执行`forms`.

`test-form`按参数列表中顺序依次求值, 直到有一个求值为true. 如果在这个子句中没有`forms`, 则`test-form`的 **主值** 作为`cond`形式的结果返回; 否则与该`test-form`相应的`forms`从左至右依次求值, 像在一个隐式的`progn`中一样, 最后一个形式的值作为`cond`形式的返回值.

一旦有一个`test-form`求值为true, 后续的`test-from`不再求值. 如果没有`test-form`求值为true, 则返回`nil`.

**Examples**:

``` lisp
(defun select-options ()
(cond ((= a 1) (setq a 2))
			((= a 2) (setq a 3))
			((and (= a 3) (floor a 2)))
			(t (floor a 3)))) =>  SELECT-OPTIONS

(setq a 1) =>  1

(select-options) =>  2 ; ((= a 1) (setq a 2))
a =>  2

(select-options) =>  3 ; ((= a 2) (setq a 3))
a =>  3

(select-options) =>  1 ; ((and (= a 3) (floor a 2)))

(setq a 5) =>  5
(select-options) =>  1, 2 ; (t (floor a 3))
```

**Side Effects**: 无.


**Affected By**: 无.


**Exceptional Situations**: 无.


**See Also**:

[if](#if), [case](#case)

**Notes**: 无.




# 223 `condition`
# 224 `conjugate`
# 225 `cons`

> [!note] "Function"
**Syntax**:

``` lisp
cons object-1 object-2 => cons
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 226 `consp`

> [!note] "Function"
**Syntax**:

``` lisp
consp object => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:

# 227 `constantly`
# 228 `constantp`
# 229 `continue`
# 230 `control-error`
# 231 `copy-alist`
# 232 `copy-list`

> [!note] "Function"
**Syntax**:

``` lisp
copy-list list => copy
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 233 `copy-pprint-dispatch`
# 234 `copy-readtable`
# 235 `copy-seq`
# 236 `copy-structure`
# 237 `copy-symbol`
# 238 `copy-tree`
# 239 `cos`
# 240 `cosh`
# 241 `count`
# 242 `count-if`
# 243 `count-if-not`
# 244 `ctypecase`
# 245 `debug`
# 246 `decf`
# 247 `declaim`
# 248 `declaration`
# 249 `declare`
# 250 `decode-float`
# 251 `decode-universal-time`
# 252 `defclass`
# 253 `defconstant`
# 254 `defgeneric`
# 255 `define-compiler-macro`
# 256 `define-condition`
# 257 `define-method-combination`
# 258 `define-modify-macro`
# 259 `define-setf-expander`
# 260 `define-symbol-macro`
# 261 `defmacro`
# 262 `defmethod`
# 263 `defpackage`
# 264 `defparameter`
# 265 `defsetf`
# 266 `defstruct`
# 267 `deftype`
# 268 `defun`


> [!tip] "Macro"
**Syntax**:

``` lisp
defun function-name lambda-list [[declaration* | documentation]] form*

=> function-name
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 269 `defvar`
# 270 `delete`
# 271 `delete-duplicates`
# 272 `delete-file`
# 273 `delete-if`
# 274 `delete-if-not`
# 275 `delete-package`
# 276 `denominator`
# 277 `deposit-field`
# 278 `describe`
# 279 `describe-object`
# 280 `destructuring-bind`
# 281 `digit-char`
# 282 `digit-char-p`
# 283 `directory`
# 284 `directory-namestring`
# 285 `disassemble`
# 286 `division-by-zero`
# 287 `do, do*`

> [!tip] "Macro"
**Syntax**:

``` lisp
do ({var | (var [init-form [step-form]])}*)
  (end-test-form result-form*)
  declaration*
  {tag | statement}*
=> result*

do* ({var | (var [init-form [step-form]])}*)
  (end-test-form result-form*)
  declaration*
  {tag | statement}*
=> result*
```


**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:


# 288 `do-all-symbols`
# 289 `do-external-symbols`
# 290 `do-symbols`
# 291 `documentation`
# 292 `dolist`
# 293 `dotimes`

> [!tip] "Macro"
**Syntax**:

``` lisp
dotimes (var count-form [result-form]) declaration* {tag | statement}*

=> result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 294 `double-float`
# 295 `double-float-epsilon`
# 296 `double-float-negative-epsilon`
# 297 `dpb`
# 298 `dribble`
# 299 `dynamic-extent`
# 300 `ecase`
# 301 `echo-stream`
# 302 `echo-stream-input-stream`
# 303 `echo-stream-output-stream`
# 304 `ed`
# 305 `elt`
# 306 `encode-universal-time`
# 307 `end-of-file`
# 308 `endp`
# 309 `enough-namestring`
# 310 `ensure-directories-exist`
# 311 `ensure-generic-function`
# 312 `eq`

> [!note] "Function"
**Syntax**:

``` lisp
eq x y => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 313 `eql`

> [!note] "Function"
**Syntax**:

``` lisp
eql x y => generalized-boolean
```


**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 314 `equal`

> [!note] "Function"
**Syntax**:

``` lisp
equal x y => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:






# 315 `equalp`
# 316 `error`
# 317 `etypecase`
# 318 `eval`
# 319 `eval-when`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
eval-when (situation*) form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 320 `oddp`

> [!note] "Function"
**Syntax**:

``` lisp
evenp integer => generalized-boolean
oddp integer => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 321 `every`
# 322 `exp`
# 323 `export`
# 324 `expt`
# 325 `extended-char`
# 326 `fboundp`
# 327 `fdefinition`
# 328 `file-author`
# 329 `file-error`
# 330 `file-error-pathname`
# 331 `file-length`
# 332 `file-namestring`
# 333 `file-position`
# 334 `file-stream`
# 335 `file-string-length`
# 336 `file-write-date`
# 337 `fill`
# 338 `fill-pointer`
# 339 `find`
# 340 `find-all-symbols`
# 341 `find-class`
# 342 `find-if`
# 343 `find-if-not`
# 344 `find-method`
# 345 `find-package`
# 346 `find-restart`
# 347 `find-symbol`
# 348 `finish-output`
# 349 `tenth`

> [!tip] "Accessor"
**Syntax**:

``` lisp
first list => object
second list => object
third list => object
fourth list => object
fifth list => object
sixth list => object
seventh list => object
eighth list => object
ninth list => object
tenth list => object
(setf (first list) new-object)
(setf (second list) new-object)
(setf (third list) new-object)
(setf (fourth list) new-object)
(setf (fifth list) new-object)
(setf (sixth list) new-object)
(setf (seventh list) new-object)
(setf (eighth list) new-object)
(setf (ninth list) new-object)
(setf (tenth list) new-object)
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:


# 350 `fixnum`
# 351 `macrolet`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
flet ((function-name lambda-list [[local-declaration* | local-documentation]] local-form*)*) declaration* form*
=> result*

labels ((function-name lambda-list [[local-declaration* | local-documentation]] local-form*)*) declaration* form*
=> result*

macrolet ((name lambda-list [[local-declaration* | local-documentation]] local-form*)*) declaration* form*
=> result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 352 `float`
# 353 `float-digits`
# 354 `float-precision`
# 355 `float-radix`
# 356 `float-sign`
# 357 `floating-point-inexact`
# 358 `floating-point-invalid-operation`
# 359 `floating-point-overflow`
# 360 `floating-point-underflow`
# 361 `floatp`

# 362 `fmakunbound`
# 363 `force-output`
# 364 `format`
# 365 `formatter`
# 366 `fresh-line`
# 367 `ftype`
# 368 `funcall`

> [!note] "Function"
**Syntax**:

``` lisp
funcall function &rest args => result*
```

**Arguments and Values**:

- function: 函数指示器
- args: 函数的参数
- results: 函数的返回值

**Description**:

`funcall`在使用参数`args`调用函数`function`.
如果`function`是个符号, 通过在全局环境中找到其函数值将其转换为一个函数.

**Examples**:

``` lisp
(funcall #'+ 1 2 3) =>  6
(funcall 'car '(1 2 3)) =>  1
(funcall 'position 1 '(1 2 3 2 1) :start 1) =>  4
(cons 1 2) =>  (1 . 2)
(flet ((cons (x y) `(kons ,x ,y)))
  (let ((cons (symbol-function '+)))
(funcall #'cons
         (funcall 'cons 1 2)
         (funcall cons 1 2))))
=>  (KONS (1 . 2) 3)
```

**Affected By**: 无.

**Exceptional Situations**:

如果`function`是个符号, 且没有全局定义的同名函数或者是全局定义的同名宏或特殊操作符时, 发出类型为`undefined-function`的错误信号.

**See Also**:

[apply](#apply), [function](#function), [3.1 求值](../03-Evaluation-and-Compilation#3.1).

**Notes**:

``` lisp
(funcall function arg1 arg2 ...)
==  (apply function arg1 arg2 ... nil)
==  (apply function (list arg1 arg2 ...))
```

`funcall`和普通函数调用之前的区别是, 前者是通过求值一个形式获得的函数, 而后者是在函数通常出现的位置做特殊解释获得的.


# 369 `function`


> [!attention] "Special Operator"
**Syntax**:

``` lisp
function name => function
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 370 `function-keywords`
# 371 `function-lambda-expression`
# 372 `functionp`
# 373 `gcd`
# 374 `generic-function`
# 375 `gensym`
# 376 `gentemp`
# 377 `get`
# 378 `get-decoded-time`
# 379 `get-dispatch-macro-character`
# 380 `get-internal-real-time`
# 381 `get-internal-run-time`
# 382 `get-macro-character`
# 383 `get-output-stream-string`
# 384 `get-properties`
# 385 `get-setf-expansion`
# 386 `get-universal-time`
# 387 `getf`
# 388 `gethash`
# 389 `go`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
go tag =>|
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 390 `graphic-char-p`
# 391 `handler-bind`
# 392 `handler-case`
# 393 `hash-table`
# 394 `hash-table-count`
# 395 `hash-table-p`
# 396 `hash-table-rehash-size`
# 397 `hash-table-rehash-threshold`
# 398 `hash-table-size`
# 399 `hash-table-test`
# 400 `host-namestring`
# 401 `identity`
# 402 `if`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
if test-form then-form [else-form] => result*
```

**Arguments and Values**:

- `test-form`: 一个形式
- `then-form`: 一个形式
- `else-form`:一个形式, 默认为`nil`
- `results`: 如果`test-form`为true, `then-form`返回的结果; 否则是`else-form`返回的结果

**Description**:

`if`允许依赖于单个`test-form`执行形式.

首先求值`test-form`, 如果其结果为true, 则选择`then-form`, 否则选择`else-form`. 对选择的形式求值.

**Examples**:

``` lisp
(if t 1) =>  1
(if nil 1 2) =>  2

(defun test ()
(dolist (truth-value '(t nil 1 (a b c)))
	(if truth-value (print 'true) (print 'false))
	(prin1 truth-value))) =>  TEST
(test)
>>  TRUE T
>>  FALSE NIL
>>  TRUE 1
>>  TRUE (A B C)
=>  NIL
```

**Affected By**: 无.


**Exceptional Situations**: 无.


**See Also**:

[cond](#cond), [unless](#unless), [when](#when)

**Notes**:

``` lisp
 (if test-form then-form else-form)
 ==
 (cond (test-form then-form)
   (t else-form))
```




# 403 `ignorable`
# 404 `ignore`
# 405 `ignore-errors`
# 406 `imagpart`
# 407 `import`
# 408 `in-package`
# 409 `incf`
# 410 `initialize-instance`
# 411 `inline`
# 412 `input-stream-p`
# 413 `inspect`
# 414 `integer`
# 415 `integer-decode-float`
# 416 `integer-length`
# 417 `integerp`


> [!note] "Function"
**Syntax**:

``` lisp
integerp object => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 418 `interactive-stream-p`
# 419 `intern`
# 420 `internal-time-units-per-second`
# 421 `nintersection`

> [!note] "Function"
**Syntax**:

``` lisp
intersection list-1 list-2 &key key test test-not => result-list
nintersection list-1 list-2 &key key test test-not => result-list
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 422 `invalid-method-error`
# 423 `invoke-debugger`
# 424 `invoke-restart`
# 425 `invoke-restart-interactively`
# 426 `isqrt`
# 427 `keyword`
# 428 `keywordp`
# 429 `lambda`
# 430 `lambda-list-keywords`
# 431 `lambda-parameters-limit`
# 432 `last`

> [!note] "Function"
**Syntax**:

``` lisp
last list &optional n => tail
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 433 `lcm`
# 434 `ldb`
# 435 `ldb-test`
# 436 `ldiff`
# 437 `least-negative-double-float`
# 438 `least-negative-long-float`
# 439 `least-negative-normalized-double-float`
# 440 `least-negative-normalized-long-float`
# 441 `least-negative-normalized-short-float`
# 442 `least-negative-normalized-single-float`
# 443 `least-negative-short-float`
# 444 `least-negative-single-float`
# 445 `least-positive-double-float`
# 446 `least-positive-long-float`
# 447 `least-positive-normalized-double-float`
# 448 `least-positive-normalized-long-float`
# 449 `least-positive-normalized-short-float`
# 450 `least-positive-normalized-single-float`
# 451 `least-positive-short-float`
# 452 `least-positive-single-float`
# 453 `length`

> [!note] "Function"
**Syntax**:

``` lisp
length sequence => n
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 454 `let*`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
let ( { var | (var [init-form]) }* ) declaration* form* => result*
let* ( { var | (var [init-form]) }* ) declaration* form* => result*
```

**Arguments and Values**:

- `var`: 一个符号
- `init-form`: 一个形式(称为初始值形式)
- `declaration`: 一个`declare`表达式, 不被求值
- `form`: 一个形式
- `results`: `forms`返回的值

**Description**:

`let`和`let*` **创建新的变量绑定**, 并使用这些绑定执行一组形式.
`let`按并行方式执行绑定, `let*`按串行方式执行绑定.

形式

``` lisp
(let ((var1 init-form-1)
		(var2 init-form-2)
		...
		(varm init-form-m))
declaration1
declaration2
...
declarationp
form1
form2
...
formn)
```

首先按顺序求值表达式`init-form-1`、`init-form-2`等, 保存结果值.
然后所有变量`varj`绑定到对应的值; 每个绑定是 **词法的**, 除非存在相反的`special`声明.
接着按顺序求值`formk`; 除最后一个值外丢弃所有值(即, `let`的体是一个隐式的`progn`).

`let*`与`let`相似, 但按串行方式执行变量绑定. 一个`var`的`init-form`表达式可以引用前面绑定的`var`.

形式

``` lisp
(let* ((var1 init-form-1)
		 (var2 init-form-2)
		 ...
		 (varm init-form-m))
declaration1
declaration2
...
declarationp
form1
form2
...
formn)
```

首先求值表达式`init-form-1`, 将结果绑定到`var1`; 然后求值表达式`init-form-2`, 将结果绑定到`var2`, 等等. 接着, 表达式`formj`按序求值; 除最后一个值外丢弃所有值(即, `let*`的体是一个隐式的`progn`).

在`let`和`let*`中, 如果一个`var`没有对应的`init-form`, 则`var`初始化为`nil`.

特殊形式`let`有属性: 名称绑定的作用域不包含任意初始值形式.
对于`let*`, 变量的作用域也包含之后的变量绑定中剩余的初始值形式.

**Examples**:

``` lisp
(setq a 'top) =>  TOP
(defun dummy-function () a) =>  DUMMY-FUNCTION

(let ((a 'inside) (b a)) ;(b a)中a是指toplevel的a
 (format nil "~S ~S ~S" a b (dummy-function))) =>  "INSIDE TOP TOP"

(let* ((a 'inside) (b a));(b a)中a是指前一个绑定的变量
 (format nil "~S ~S ~S" a b (dummy-function))) =>  "INSIDE INSIDE TOP"

(let ((a 'inside) (b a))
 (declare (special a)) ;将a改为非词法的
 (format nil "~S ~S ~S" a b (dummy-function))) =>  "INSIDE TOP INSIDE"
```

下面的代码是不正确的.

``` lisp
(let (x)
(declare (integer x))
(setq x (gcd y z))
...)
```

`x`的初始值为`nil`, 违背了类型声明`(declare (integer x))`.


**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[progv](#progv)

**Notes**: 无.




# 455 `lisp-implementation-type`
# 456 `lisp-implementation-version`
# 457 `list*`

> [!note] "Function"
**Syntax**:

``` lisp
list &rest objects => list
list* &rest objects+ => result
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 458 `list-all-packages`
# 459 `list-length`
# 460 `listen`
# 461 `listp`

> [!note] "Function"
**Syntax**:

``` lisp
listp object => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 462 `load`
# 463 `load-logical-pathname-translations`
# 464 `load-time-value`


> [!attention] "Special Operator"
**Syntax**:

``` lisp
load-time-value form &optional read-only-p => object
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 465 `locally`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
locally declaration* form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 466 `log`
# 467 `logand`
# 468 `logandc1`
# 469 `logandc2`
# 470 `logbitp`
# 471 `logcount`
# 472 `logeqv`
# 473 `logical-pathname`
# 474 `logical-pathname-translations`
# 475 `logior`
# 476 `lognand`
# 477 `lognor`
# 478 `lognot`
# 479 `logorc1`
# 480 `logorc2`
# 481 `logtest`
# 482 `logxor`
# 483 `long-float`
# 484 `long-float-epsilon`
# 485 `long-float-negative-epsilon`
# 486 `long-site-name`

# 487 `loop`

> [!tip] "Macro"
**Syntax**:

``` lisp
; 简单的循环形式
loop compound-form* => result*
; 扩展的循环形式
loop [name-clause] { variable-clause }* { main-clause }* => result*
```
``` EBNF
(* 1 名称从句 *)
name-clause::= named name

(* 2 变量从句 *)
variable-clause::= with-clause | initial-final | for-as-clause
(* 2.1 WITH从句 *)
with-clause::= with var1 [type-spec] [= form1] { and var2 [type-spec] [= form2] }*

(* 3 主从句 *)
main-clause::= unconditional | accumulation | conditional | termination-test | initial-final

(* 2.2/3.5 序言和后继从句 *)
initial-final::= initially compound-form+ | finally compound-form+

(* 3.1 无条件执行从句 *)
unconditional::= { do | doing } compound-form+ | return { form | it }
(* 3.2 累积从句 *)
accumulation::= list-accumulation | numeric-accumulation
list-accumulation::= { collect | collecting | append | appending | nconc | nconcing } { form | it }
                     [into simple-var]
numeric-accumulation::= { count | counting | sum | summing | }
                         maximize | maximizing | minimize | minimizing { form | it }
                        [into simple-var] [type-spec]
(* 3.3 条件执行从句 *)
conditional::= { if | when | unless } form selectable-clause { and selectable-clause }*
               [else selectable-clause { and selectable-clause }*]
               [end]
selectable-clause::= unconditional | accumulation | conditional
(* 3.4 终止测试从句 *)
termination-test::= while form | until form | repeat form | always form | never form | thereis form

(* 2.3 for-as从句 *)
for-as-clause::= { for | as } for-as-subclause { and for-as-subclause }*
for-as-subclause::= for-as-arithmetic | for-as-in-list | for-as-on-list | for-as-equals-then |
                    for-as-across | for-as-hash | for-as-package
for-as-arithmetic::= var [type-spec] for-as-arithmetic-subclause
for-as-arithmetic-subclause::= arithmetic-up | arithmetic-downto | arithmetic-downfrom
arithmetic-up::= [ [ { from | upfrom } form1
                    | { to | upto | below } form2
                    | by form3 ] ]+
arithmetic-downto::= [ [ {{ from form1 }}1
                        | {{ { downto | above } form2 }}1
                        | by form3 ] ]
arithmetic-downfrom::= [ [ {{ downfrom form1 }}1
                          | { to | downto | above } form2
                          | by form3 ] ]
for-as-in-list::= var [type-spec] in form1 [by step-fun]
for-as-on-list::= var [type-spec] on form1 [by step-fun]
for-as-equals-then::= var [type-spec] = form1 [then form2]
for-as-across::= var [type-spec] across vector
for-as-hash::= var [type-spec] being { each | the }
               { { hash-key | hash-keys } { in | of } hash-table
                 [using (hash-value other-var)]
               | { hash-value | hash-values } { in | of } hash-table
                 [using (hash-key other-var)]}
for-as-package::= var [type-spec] being { each | the }
                  { symbol | symbols
                  | present-symbol | present-symbols
                  | external-symbol | external-symbols }
                  [{ in | of } package]
(* 2.1.1 类型描述和变量 *)
type-spec::= simple-type-spec | destructured-type-spec
simple-type-spec::= fixnum | float | t | nil
destructured-type-spec::= of-type d-type-spec
d-type-spec::= type-specifier | (d-type-spec . d-type-spec)
var::= d-var-spec
var1::= d-var-spec
var2::= d-var-spec
other-var::= d-var-spec
d-var-spec::= simple-var | nil | (d-var-spec . d-var-spec)
```

**Arguments and Values**:

- `compound-form`: 一个复合形式
- `name`: 一个符号
- `simple-var`: 一个符号(变量名称)
- `form, form1, form2, form3`: 一个形式
- `step-fun`: 求值为单个传递参数的函数肚饿形式
- `vector`: 求值为向量的形式
- `hash-table`: 求值为哈希表的形式
- `package`: 求值为包指示器的形式
- `type-specifier`: 一个类型描述符. 可以是原子类型描述符或复合类型描述符, 在解构中恰当解析方面引入了额外的复杂性; 更多信息见[6.1.1.7 解构](../06-Iteration#6.1.1.7).
- `result`: 一个对象

**Description**:

见[6.1 循环功能](../06-Iteration#6.1).

**Examples**:

``` lisp
;; An example of the simple form of LOOP.
 (defun sqrt-advisor ()
   (loop (format t "~&Number: ")
     (let ((n (parse-integer (read-line) :junk-allowed t)))
       (when (not n) (return))
       (format t "~&The square root of ~D is ~D.~%" n (sqrt n)))))
=>  SQRT-ADVISOR
 (sqrt-advisor)
>>  Number: 5<NEWLINE>
>>  The square root of 5 is 2.236068.
>>  Number: 4<NEWLINE>
>>  The square root of 4 is 2.
>>  Number: done<NEWLINE>
=>  NIL

;; An example of the extended form of LOOP.
 (defun square-advisor ()
   (loop as n = (progn (format t "~&Number: ")
                   (parse-integer (read-line) :junk-allowed t))
     while n
     do (format t "~&The square of ~D is ~D.~%" n (* n n))))
=>  SQUARE-ADVISOR
 (square-advisor)
>>  Number: 4<NEWLINE>
>>  The square of 4 is 16.
>>  Number: 23<NEWLINE>
>>  The square of 23 is 529.
>>  Number: done<NEWLINE>
=>  NIL

;; Another example of the extended form of LOOP.
 (loop for n from 1 to 10
   when (oddp n)
     collect n)
=>  (1 3 5 7 9)
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[do](#do), [dolist](#dolist), [dotimes](#dotimes), [return](#return), [go](#go), [throw](#throw), [6.1.1.7 解构](../06-Iteration#6.1.1.7).

**Notes**:

除了简单的循环形式中不能用本地宏`loop-finish`, 简单的循环形式与扩展的循环形式按如下方式关联:

``` lisp
(loop compound-form*) ==  (loop do compound-form*)
```



# 488 `loop-finish`
# 489 `lower-case-p`
# 490 `machine-instance`
# 491 `machine-type`
# 492 `machine-version`
# 493 `macro-function`
# 494 `macroexpand`
# 495 `macroexpand-1`

# 496 `make-array`
# 497 `make-broadcast-stream`
# 498 `make-concatenated-stream`
# 499 `make-condition`
# 500 `make-dispatch-macro-character`
# 501 `make-echo-stream`
# 502 `make-hash-table`
# 503 `make-instance`
# 504 `make-instances-obsolete`
# 505 `make-list`
# 506 `make-load-form`
# 507 `make-load-form-saving-slots`
# 508 `make-method`
# 509 `make-package`
# 510 `make-pathname`
# 511 `make-random-state`
# 512 `make-sequence`
# 513 `make-string`
# 514 `make-string-input-stream`
# 515 `make-string-output-stream`
# 516 `make-symbol`
# 517 `make-synonym-stream`
# 518 `make-two-way-stream`
# 519 `makunbound`
# 520 `map`
# 521 `map-into`
# 522 `mapcon`

> [!note] "Function"
**Syntax**:

``` lisp
mapc function &rest lists+ => list-1
mapcar function &rest lists+ => result-list
mapcan function &rest lists+ => concatenated-results
mapl function &rest lists+ => list-1
maplist function &rest lists+ => result-list
mapcon function &rest lists+ => concatenated-results
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 523 `maphash`
# 524 `mask-field`
# 525 `max`
# 526 `member-if-not`

> [!note] "Function"
**Syntax**:

``` lisp
member item list &key key test test-not => tail
member-if predicate list &key key => tail
member-if-not predicate list &key key => tail
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 527 `merge`
# 528 `merge-pathnames`
# 529 `method`
# 530 `method-combination`
# 531 `method-combination-error`
# 532 `method-qualifiers`
# 533 `min`
# 534 `minusp`
# 535 `mismatch`
# 536 `rem`

> [!note] "Function"
**Syntax**:

``` lisp
mod number divisor => modulus
rem number divisor => remainder
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 537 `most-negative-double-float`
# 538 `most-negative-fixnum`
# 539 `most-negative-long-float`
# 540 `most-negative-short-float`
# 541 `most-negative-single-float`
# 542 `most-positive-double-float`
# 543 `most-positive-fixnum`
# 544 `most-positive-long-float`
# 545 `most-positive-short-float`
# 546 `most-positive-single-float`
# 547 `muffle-warning`
# 548 `multiple-value-bind`
# 549 `multiple-value-call`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
multiple-value-call function-form form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 550 `multiple-value-list`
# 551 `multiple-value-prog1`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
multiple-value-prog1 first-form form* => first-form-results
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 552 `multiple-value-setq`
# 553 `multiple-values-limit`
# 554 `name-char`
# 555 `namestring`
# 556 `nbutlast`
# 557 `nconc`
# 558 `next-method-p`
# 559 `nil`

> [!tip] "Constant Variable"
**Constant Value**:

``` lisp
nil
```


**Description**:


**Examples**:


**See Also**:


**Notes**:




# 560 `no-applicable-method`
# 561 `no-next-method`
# 562 `not`

> [!note] "Function"
**Syntax**:

``` lisp
not x => boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 563 `notany`
# 564 `notevery`
# 565 `notinline`
# 566 `nreconc`
# 567 `nreverse`
# 568 `nset-exclusive-or`
# 569 `nstring-capitalize`
# 570 `nstring-downcase`
# 571 `nstring-upcase`
# 572 `nsublis`
# 573 `nth`

> [!tip] "Accessor"
**Syntax**:

``` lisp
nth n list => object
(setf (nth n list) new-object)
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 574 `nth-value`
# 575 `nthcdr`

> [!note] "Function"
**Syntax**:

``` lisp
nthcdr n list => tail
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 576 `null`

> [!note] "Function"
**Syntax**:

``` lisp
null object => boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 577 `number`
# 578 `numberp`
# 579 `numerator`
# 580 `open`
# 581 `open-stream-p`
# 582 `optimize`
# 583 `or`

> [!tip] "Macro"
**Syntax**:

``` lisp
or form* => results*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 584 `otherwise`
# 585 `output-stream-p`
# 586 `package`
# 587 `package-error`
# 588 `package-error-package`
# 589 `package-name`
# 590 `package-nicknames`
# 591 `package-shadowing-symbols`
# 592 `package-use-list`
# 593 `package-used-by-list`
# 594 `packagep`
# 595 `pairlis`
# 596 `parse-error`
# 597 `parse-integer`
# 598 `parse-namestring`
# 599 `pathname`
# 600 `pathname-device`
# 601 `pathname-directory`
# 602 `pathname-host`
# 603 `pathname-match-p`
# 604 `pathname-name`
# 605 `pathname-type`
# 606 `pathname-version`
# 607 `pathnamep`
# 608 `peek-char`
# 609 `phase`
# 610 `pi`
# 611 `plusp`
# 612 `pop`

> [!tip] "Macro"
**Syntax**:

``` lisp
pop place => element
```

**Arguments and Values**:

- `place`: 一个位置, 它的值是一个列表(可以是点列表、循环列表)
- `element`: 一个对象(`place`的内容的car)

**Description**:

`pop`读取`place`的值, 记住检索的列表的car, 将列表的cdr写入`place`, 最终返回原始检索的列表car.

有关`place`的子形式的求值, 见[5.1.1.1 子形式到位置的求值](../05-Data-and-Control-Flow#5.1.1.1).

**Examples**:

``` lisp
(setq stack '(a b c)) =>  (A B C)
(pop stack) =>  A
stack =>  (B C)

(setq llst '((1 2 3 4))) =>  ((1 2 3 4))
(pop (car llst)) =>  1
llst =>  ((2 3 4))
```

**Side Effects**: `place`的内容被修改.

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[push](#push), [pushnew](#pushnew), [5.1 通用的引用](../05-Data-and-Control-Flow#5.1)

**Notes**:

`(pop place)`的作用基本上等价于:

``` lisp
(prog1 (car place) (setf place (cdr place)))
```

除了后者会求值`place`的子形式三次, 而`pop`只求值一次.

# 613 `position`
# 614 `position-if`
# 615 `position-if-not`
# 616 `pprint`
# 617 `pprint-dispatch`
# 618 `pprint-exit-if-list-exhausted`
# 619 `pprint-fill`
# 620 `pprint-indent`
# 621 `pprint-linear`
# 622 `pprint-logical-block`
# 623 `pprint-newline`
# 624 `pprint-pop`
# 625 `pprint-tab`
# 626 `pprint-tabular`
# 627 `prin1`
# 628 `prin1-to-string`
# 629 `princ`
# 630 `princ-to-string`
# 631 `print`
# 632 `print-not-readable`
# 633 `print-not-readable-object`
# 634 `print-object`
# 635 `print-unreadable-object`
# 636 `probe-file`
# 637 `proclaim`
# 638 `prog`
# 639 `prog*`
# 640 `prog1`
# 641 `prog2`
# 642 `progn`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
progn form* => result*
```

**Arguments and Values**:

- `forms`: 一个隐式的`progn`
- `results`: `forms`的值

**Description**:

`progn`按给定的顺序求值`forms`. 丢弃除最后一个形式外的值.

如果`progn`作为顶级形式出现, 则`progn`中的`forms`被编译器视为顶级形式.

**Examples**:

``` lisp
(progn) =>  NIL
(progn 1 2 3) =>  3
(progn (values 1 2 3)) =>  1, 2, 3

(setq a 1) =>  1
(if a
	 (progn (setq a nil) 'here)
	 (progn (setq a t) 'there)) =>  HERE
a =>  NIL
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[prog1](#prog1), [prog2](#prog2), [3.1 求值](../03-Evaluation-and-Compilation#3.1)

**Notes**:

Common Lisp中很多地方包含使用隐式`progn`的语法. 即, 作为其语法的一部分,
允许写多个被串行求值的形式, 忽略除最后一个形式的结果, 返回最后一个形式的结果.
这些地方包括但不限于: lambda表达式的体, 多个控制和条件形式的体(`case`、`catch`、`progn`、`when`等).

# 643 `program-error`
# 644 `progv`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
progv symbols values form* => result*
```

**Arguments and Values**:

- `symbols`: 符号列表; 被求值
- `values`: 对象列表, 被求值
- `forms`: 隐式`progn`
- `results`: `forms`返回的值

**Description**:

`progv`创建新的 **动态变量** 绑定, 并使用这些绑定执行每个`form`. 按顺序求值每个`form`.

`progv`允许绑定一个或多个 **运行时确定名称的** 动态变量. 每个`form`按顺序求值, 使用名称在`symbols`中的绑定到相应的`values`的动态变量.
如果提供了过少的`values`, 则剩下的符号被绑定为没有值.
如果提供了过多的`values`, 则多余的被忽略.
在从`progv`中退出时, 动态变量的绑定被撤销.

**Examples**:

``` lisp
(setq *x* 1) =>  1

(progv '(*x*) '(2) *x*) =>  2
*x* =>  1 ;动态变量绑定被撤销
```

假设`*x*`不是全局特殊的,

``` lisp
(let ((*x* 3))				; 变量*x*
 (progv '(*x*) '(4)	; 符号*x*
	 (list *x* (symbol-value '*x*)))) =>  (3 4)
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[let](#let), [3.1 求值(Evaluation)](../03-Evaluation-and-Compilation#3.1)

**Notes**:

`progv`在编写内嵌在Lisp中的语言时很有用, 提供了绑定动态变量的机制.

# 645 `provide`
# 646 `psetq`
# 647 `push`
# 648 `pushnew`
# 649 `quote`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
quote object => object
```

**Arguments and Values**:

- `object`: 一个对象, 不被求值

**Description**:

特殊操作符`quote`直接返回`object`.

如果字面量对象(包括被引述的对象)被破坏性修改时, 后果未定义.

**Examples**:

``` lisp
(setq a 1) =>  1

(quote (setq a 3)) =>  (SETQ A 3)
a =>  1 ;object未被求值

'a =>  A
''a =>  (QUOTE A)
'''a =>  (QUOTE (QUOTE A))

(setq a 43) =>  43
(list a (cons a 3)) =>  (43 (43 . 3))
(list (quote a) (quote (cons a 3))) =>  (A (CONS A 3))

1 =>  1
'1 =>  1

"foo" =>  "foo"
'"foo" =>  "foo"

(car '(a b)) =>  A
'(car '(a b)) =>  (CAR (QUOTE (A B)))

#(car '(a b)) =>  #(CAR (QUOTE (A B)))
'#(car '(a b)) =>  #(CAR (QUOTE (A B)))
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[3.1 求值(Evaluation)](../03-Evaluation-and-Compilation#3.1), [2.4.3 `'`(single-quote)](../02-Syntax#2.4.3), [3.2.1 编译器术语](../03-Evaluation-and-Compilation#3.2.1)

**Notes**:

文本记法`'object`等价于`(quote object)`, 见[3.2.1 编译器术语](../03-Evaluation-and-Compilation#3.2.1).

自求值对象不需要被`quote`引述. 符号和列表用于标识程序的部分, 不使用`quote`不能作为常值数据使用.
因为`quote`抑制了这些对象的求值, 它们称为数据而不是程序.

# 650 `random`
# 651 `random-state`
# 652 `random-state-p`
# 653 `rassoc`
# 654 `rassoc-if`
# 655 `rassoc-if-not`
# 656 `ratio`
# 657 `rational`
# 658 `rationalize`
# 659 `rationalp`
# 660 `read`
# 661 `read-byte`
# 662 `read-char`
# 663 `read-char-no-hang`
# 664 `read-delimited-list`
# 665 `read-from-string`
# 666 `read-line`
# 667 `read-preserving-whitespace`
# 668 `read-sequence`
# 669 `reader-error`
# 670 `readtable`
# 671 `readtable-case`
# 672 `readtablep`
# 673 `real`
# 674 `realp`
# 675 `realpart`
# 676 `reduce`
# 677 `reinitialize-instance`
# 678 `remf`
# 679 `remhash`
# 680 `remove`
# 681 `remove-duplicates`
# 682 `remove-if`
# 683 `remove-if-not`
# 684 `remove-method`
# 685 `remprop`
# 686 `rename-file`
# 687 `rename-package`
# 688 `replace`
# 689 `require`
# 690 `rest`
# 691 `restart`
# 692 `restart-bind`
# 693 `restart-case`
# 694 `restart-name`
# 695 `return`
# 696 `return-from`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
return-from name [result] =>|
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 697 `revappend`
# 698 `reverse`
# 699 `room`
# 700 `rotatef`
# 701 `row-major-aref`
# 702 `rplaca`
# 703 `rplacd`
# 704 `safety`
# 705 `satisfies`
# 706 `sbit`
# 707 `scale-float`
# 708 `schar`
# 709 `search`
# 710 `sequence`
# 711 `serious-condition`
# 712 `set`
# 713 `nset-difference`

> [!note] "Function"
**Syntax**:

``` lisp
set-difference list-1 list-2 &key key test test-not => result-list
nset-difference list-1 list-2 &key key test test-not => result-list
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 714 `set-dispatch-macro-character`
# 715 `set-exclusive-or`
# 716 `set-macro-character`
# 717 `set-pprint-dispatch`
# 718 `set-syntax-from-char`
# 719 `psetf`

> [!tip] "Macro"
**Syntax**:

``` lisp
setf {pair}* => result*
psetf {pair}* => nil

pair::= place newvalue
```

**Arguments and Values**:

- `place`: 一个位置
- `newvalue`: 一个形式
- `results`: 为最后一个位置存储形式放回的多值, 或在没有`pairs`时返回`nil`

**Description**:

`setf`将`place`的值修改为`newvalue`.

`(setf place newvalue)`展开为一个更新形式, 出处求值`newvalue`的结果到被`place`引用的位置.
一些`place`形式使用带可选传递参数的访问器. 这些可选传递参数是否被`setf`允许, 或它们使用的效果是什么, 是由`setf`展开器函数决定的, 不受`setf`的控制. 任何接受`&optional`、`&rest`或`&key`传递参数且这些传递参数声明为可用于`setf`的函数的文档必须描述如何处理这些传递参数.

如果提供了多个`pair`, `pairs`按顺序处理, 即:

``` lisp
(setf place-1 newvalue-1
		place-2 newvalue-2
		...
		place-N newvalue-N)
```

等价于:

``` lisp
(progn (setf place-1 newvalue-1)
		 (setf place-2 newvalue-2)
		 ...
		 (setf place-N newvalue-N))
```

对于`psetf`, 如果提供了多个`pair`, 则将新值指派给位置是并行执行的.
待求值的所有子形式(`place`和`newvalue`的形式), 按从左到右的顺序求值; 在所有求值完成后, 所有指派动作按不可预计的顺序执行.

`setf`和`psetf`展开的详情, 见[5.1.2 位置的种类](../05-Data-and-Control-Flow#5.1.2).

**Examples**:

``` lisp
(setq x (cons 'a 'b) y (list 1 2 3)) =>  (1 2 3)
(setf (car x) 'x (cadr y) (car x) (cdr x) y) =>  (1 X 3)
x =>  (X 1 X 3)
y =>  (1 X 3)

(setq x (cons 'a 'b) y (list 1 2 3)) =>  (1 2 3)
(psetf (car x) 'x (cadr y) (car x) (cdr x) y) =>  NIL
x =>  (X 1 A 3)
y =>  (1 A 3)
```

**Affected By**:

[define-setf-expander](#define-setf-expander), [defsetf](#defsetf), [`*macroexpand-hook*`](#*macroexpand-hook*)

**Exceptional Situations**: 无.

**See Also**:

[define-setf-expander](#define-setf-expander), [defsetf](#defsetf), [macroexpand-1](#macroexpand-1), [rotatef](#rotatef), [shiftf](#shiftf), [5.1 通用的引用](../05-Data-and-Control-Flow#5.1)

**Notes**: 无.


# 720 `setq`

> [!attention] "Special Form"
**Syntax**:

``` lisp
setq { pair }* => result

pair ::= var form
```

**Pronunciation**: ['set,kyoo]


**Arguments and Values**:

- `var`: 一个符号, 命名了一个不是常值变量的变量
- `form`: 一个形式
- `result`: 最后一个`form`的主值, 或者在没有提供`pair`时为`nil`

**Description**:

赋值给变量. `setq var1 form1 var2 form2 ...`是Lisp中简单的变量赋值语句.
首先`form1`被求值, 其求值结果存放在变量`var1`中, 接着`form2`被求值, 其求值结果存放在变量`var2`中, 等等.
`setq`可被用于 **词法** 或 **动态** 变量的赋值.

如果任意一个变量`var`引用了`symbol-macrolet`生成的绑定, 则该变量被视为使用了`setf`(而不是`setq`).

**Examples**:

``` lisp
;; A simple use of SETQ to establish values for variables.
(setq a 1 b 2 c 3) =>  3
a =>  1
b =>  2
c =>  3

;; Use of SETQ to update values by sequential assignment.
;; 串行赋值
(setq a (1+ b) b (1+ a) c (+ a b)) =>  7
a =>  3
b =>  4
c =>  7

;; This illustrates the use of SETQ on a symbol macro.
(let ((x (list 10 20 30))) ;x=(10 20 30)
(symbol-macrolet ((y (car x)) (z (cadr x))) ; y=10, z=20
	(setq y (1+ z) z (1+ y)) ;y=21, z=22 -- setf x=(21 22 30)
	(list x y z)))
=>  ((21 22 30) 21 22)
```

**Side Effects**:

每个`form`的主值被赋值给相应的`var`.

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[psetq](#psetq), [set](#set). [setf](#setf), [symbol-macrolet](#symbol-macrolet)

**Notes**: 无.



# 721 `shadow`
# 722 `shadowing-import`
# 723 `shared-initialize`
# 724 `shiftf`
# 725 `short-float`
# 726 `short-float-epsilon`
# 727 `short-float-negative-epsilon`
# 728 `short-site-name`
# 729 `signal`
# 730 `signed-byte`
# 731 `signum`
# 732 `simple-array`
# 733 `simple-base-string`
# 734 `simple-bit-vector`
# 735 `simple-bit-vector-p`
# 736 `simple-condition`
# 737 `simple-condition-format-arguments`
# 738 `simple-condition-format-control`
# 739 `simple-error`
# 740 `simple-string`
# 741 `simple-string-p`
# 742 `simple-type-error`
# 743 `simple-vector`
# 744 `simple-vector-p`
# 745 `simple-warning`
# 746 `sin`
# 747 `single-float`
# 748 `single-float-epsilon`
# 749 `single-float-negative-epsilon`
# 750 `sinh`
# 751 `sleep`
# 752 `slot-boundp`
# 753 `slot-exists-p`
# 754 `slot-makunbound`
# 755 `slot-missing`
# 756 `slot-unbound`
# 757 `slot-value`
# 758 `software-type`
# 759 `software-version`
# 760 `some`
# 761 `sort`
# 762 `space`
# 763 `special`
# 764 `special-operator-p`
# 765 `speed`
# 766 `sqrt`
# 767 `stable-sort`
# 768 `standard`
# 769 `standard-char`
# 770 `standard-char-p`
# 771 `standard-class`
# 772 `standard-generic-function`
# 773 `standard-method`
# 774 `standard-object`
# 775 `step`
# 776 `storage-condition`
# 777 `store-value`
# 778 `stream`
# 779 `stream-element-type`
# 780 `stream-error`
# 781 `stream-error-stream`
# 782 `stream-external-format`
# 783 `streamp`
# 784 `string`
# 785 `string-capitalize`
# 786 `string-downcase`
# 787 `string-equal`
# 788 `string-greaterp`
# 789 `string-left-trim`
# 790 `string-lessp`
# 791 `string-not-equal`
# 792 `string-not-greaterp`
# 793 `string-not-lessp`
# 794 `string-right-trim`
# 795 `string-stream`
# 796 `string-trim`
# 797 `string-upcase`
# 798 `string/=`
# 799 `string<`
# 800 `string<=`
# 801 `string=`
# 802 `string>`
# 803 `string>=`
# 804 `stringp`
# 805 `structure`
# 806 `structure-class`
# 807 `structure-object`
# 808 `style-warning`
# 809 `sublis`
# 810 `subseq`
# 811 `subsetp`
# 812 `nsubst-if-not`

> [!note] "Function"
**Syntax**:

``` lisp
subst new old tree &key key test test-not => new-tree
subst-if new predicate tree &key key => new-tree
subst-if-not new predicate tree &key key => new-tree
nsubst new old tree &key key test test-not => new-tree
nsubst-if new predicate tree &key key => new-tree
nsubst-if-not new predicate tree &key key => new-tree
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 813 `nsubstitute-if-not`

> [!note] "Function"
**Syntax**:

``` lisp
substitute newitem olditem sequence &key from-end test test-not start end count key
=> result-sequence

substitute-if newitem predicate sequence &key from-end start end count key
=> result-sequence

substitute-if-not newitem predicate sequence &key from-end start end count key
=> result-sequence

nsubstitute newitem olditem sequence &key from-end test test-not start end count key
=> sequence

nsubstitute-if newitem predicate sequence &key from-end start end count key
=> sequence

nsubstitute-if-not newitem predicate sequence &key from-end start end count key
=> sequence
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 814 `subtypep`
# 815 `svref`
# 816 `sxhash`
# 817 `symbol`
# 818 `symbol-function`
# 819 `symbol-macrolet`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
symbol-macrolet ( (symbol expansion)* ) declaration* form*
=> result*
```

**Arguments and Values**:

- `symbol`: 一个符号
- `expansion`: 一个形式
- `declaration`: 一个`decalre`表达式, 不被求值
- `forms`: 一个隐式的`progn`
- `results`: `forms`返回的值

**Description**:

`symbol-macrolet`提供了影响 **符号的宏扩展环境** 的机制.

`symbol-macrolet`在词法上, 为每个由`symbol`命名的符号宏建立展开函数.
符号宏的展开函数唯一可以保证的属性是, 当被应用在形式和环境时, 返回正确的展开(展开在概念上存储在展开函数中还是环境中是依赖于实现的).

`symbol-macrolet`的词法作用域中对`symbol`作为变量的引用, 被使用正常的宏展开过程处理, 见[3.1.2.1.1 符号作为形式](../03-Evaluation-and-Compilation#3.1.2.1.1).
符号宏的展开受与调用符号宏相同的词法环境中进一步的宏展开影响, 跟常规宏一样.

`let`中的`declaration`在这里也可使用, 有一个例外: 如果用`special`声明一个已用`symbol-macrolet`定义的符号时, `symbol-macrolet`发出错误信号.

当`symbol-macrolet`形式中的`forms`被展开时, 使用`setq`设置指定变量的值时被视为是`setf`.
`psetq`一个定义为符号宏的符号时, 被视为是`psetf`, `multiple-value-setq`被视为是`values`上调用`setf`.

`symbol-macrolet`的使用可以被`let`遮盖. 换种方式说, `symbol-macrolet`只在`forms`周围的`symbol`词法绑定作用域中替换`symbol`的出现.

**Examples**:

``` lisp
;;; The following is equivalent to
;;;   (list 'foo (let ((x 'bar)) x)),
;;; not
;;;   (list 'foo (let (('foo 'bar)) 'foo))
 (symbol-macrolet ((x 'foo))
   (list x (let ((x 'bar)) x))) ;被let遮盖
=>  (foo bar)
NOT=>  (foo foo)

 (symbol-macrolet ((x '(foo x)))
   (list x))
=>  ((FOO X))
```

**Affected By**: 无.

**Exceptional Situations**:

如果尝试绑定定义为 **全局变量** 的符号, 发出类型为`program-error`的错误信号.

如果`declaration`中包含`special`声明, 使用了被`symbol-macrolet`绑定的符号, 发出类型为`program-error`的错误信号.

**See Also**:

[with-slots](#with-slots), [macroexpand](#macroexpand)

**Notes**:

特殊形式`symbol-macrolet`是实现`macroexpand`的基本机制.

如果一个`symbol-macrolet`形式是顶级形式, `forms`也按顶级形式处理. 见[3.2.3 文件编译](../03-Evaluation-and-Compilation#3.2.3).

# 820 `symbol-name`
# 821 `symbol-package`
# 822 `symbol-plist`
# 823 `symbol-value`
# 824 `symbolp`
# 825 `synonym-stream`
# 826 `synonym-stream-symbol`
# 827 `t`
# 828 `tagbody`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
tagbody {tag | statement}* => nil
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 829 `tailp`
# 830 `tan`
# 831 `tanh`
# 832 `terpri`
# 833 `the`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
the value-type form => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 834 `throw`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
throw tag result-form =>|
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:




# 835 `time`
# 836 `trace`
# 837 `translate-logical-pathname`
# 838 `translate-pathname`
# 839 `tree-equal`
# 840 `truename`
# 841 `two-way-stream`
# 842 `two-way-stream-input-stream`
# 843 `two-way-stream-output-stream`
# 844 `type`
# 845 `type-error`
# 846 `type-error-datum`
# 847 `type-error-expected-type`
# 848 `type-of`
# 849 `typecase`
# 850 `typep`
# 851 `unbound-slot`
# 852 `unbound-slot-instance`
# 853 `unbound-variable`
# 854 `undefined-function`
# 855 `unexport`
# 856 `unintern`
# 857 `nunion`

> [!note] "Function"
**Syntax**:

``` lisp
union list-1 list-2 &key key test test-not => result-list
nunion list-1 list-2 &key key test test-not => result-list
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:



# 858 `when`

> [!tip] "Macro"
**Syntax**:

``` lisp
when test-form form* => result*
unless test-form form* => result*
```

**Arguments and Values**:

- `test-form`: 一个形式
- `forms`: 一个隐式的`progn`
- `result`: 在`when`形式中, 如果`test-form`求值为true, 或在`unless`形式中`test-form`求值为false, 返回`forms`的求值结果; 其他情况返回`nil`

**Description**:

`when`和`unless`允许依赖于单个`test-form`执行`forms`.

在`when`形式中, 如果`test-form`求值为true, `forms`按 **从左至右** 的顺序求值, `forms`返回的结果作为`when`形式的返回结果. 否则, 如果`test-form`求值为false, `forms`不被求值, `when`形式返回`nil`.

在`unless`形式中, 如果`test-form`求值为false, `forms`按 **从左至右** 的顺序求值, `forms`返回的结果作为`unless`形式的返回结果. 否则, 如果`test-form`求值为true, `forms`不被求值, `unless`形式返回`nil`.

**Examples**:

``` lisp
(when t 'hello) =>  HELLO
(unless t 'hello) =>  NIL

(when nil 'hello) =>  NIL
(unless nil 'hello) =>  HELLO

(when t) =>  NIL
(unless nil) =>  NIL

(when t (prin1 1) (prin1 2) (prin1 3))
>>  123
=>  3

(unless t (prin1 1) (prin1 2) (prin1 3)) =>  NIL
(when nil (prin1 1) (prin1 2) (prin1 3)) =>  NIL
(unless nil (prin1 1) (prin1 2) (prin1 3))
>>  123
=>  3

(let ((x 3))
(list
			;;1: (4)
			(when (oddp x) (incf x) (list x))
			;;2: NIL - 不执行(incf x) (list x)
			(when (oddp x) (incf x) (list x))
			;;3: (5)
			(unless (oddp x) (incf x) (list x))
			;;4: NIL - 不执行(incf x) (list x)
			(unless (oddp x) (incf x) (list x))

			;;5: 6
			(if (oddp x) (incf x) (list x))
			;;6: (6)
			(if (oddp x) (incf x) (list x))
			;;7: 7
			(if (not (oddp x)) (incf x) (list x))
			;;8: (7)
			(if (not (oddp x)) (incf x) (list x))))
=>  ((4) NIL (5) NIL 6 (6) 7 (7))
```

**Affected By**: 无.

**Exceptional Situations**: 无.

**See Also**:

[and](#and), [cond](#cond), [if](#if), [or](#or)

**Notes**:

``` lisp
(when test {form}+) ==  (and test (progn {form}+))
(when test {form}+) ==  (cond (test {form}+))
(when test {form}+) ==  (if test (progn {form}+) nil)
(when test {form}+) ==  (unless (not test) {form}+)

(unless test {form}+) ==  (cond ((not test) {form}+))
(unless test {form}+) ==  (if test nil (progn {form}+))
(unless test {form}+) ==  (when (not test) {form}+)
```



# 859 `unread-char`
# 860 `unsigned-byte`
# 861 `untrace`
# 862 `unuse-package`
# 863 `unwind-protect`

> [!attention] "Special Operator"
**Syntax**:

``` lisp
unwind-protect protected-form cleanup-form* => result*
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:





# 864 `update-instance-for-different-class`
# 865 `update-instance-for-redefined-class`
# 866 `upgraded-array-element-type`
# 867 `upgraded-complex-part-type`
# 868 `upper-case-p`
# 869 `use-package`
# 870 `use-value`
# 871 `user-homedir-pathname`
# 872 `values`
# 873 `values-list`
# 874 `variable`
# 875 `vector`
# 876 `vector-pop`
# 877 `vector-push`
# 878 `vector-push-extend`
# 879 `vectorp`
# 880 `warn`
# 881 `warning`
# 882 `wild-pathname-p`
# 883 `with-accessors`
# 884 `with-compilation-unit`
# 885 `with-condition-restarts`
# 886 `with-hash-table-iterator`
# 887 `with-input-from-string`
# 888 `with-open-file`
# 889 `with-open-stream`
# 890 `with-output-to-string`
# 891 `with-package-iterator`
# 892 `with-simple-restart`
# 893 `with-slots`
# 894 `with-standard-io-syntax`
# 895 `write`
# 896 `write-byte`
# 897 `write-char`
# 898 `write-line`
# 899 `write-sequence`
# 900 `write-string`
# 901 `write-to-string`
# 902 `y-or-n-p`
# 903 `yes-or-no-p`
# 904 `zerop`

> [!note] "Function"
**Syntax**:

``` lisp
zerop number => generalized-boolean
```

**Arguments and Values**:


**Description**:


**Examples**:


**Affected By**:


**Exceptional Situations**:


**See Also**:


**Notes**:
