# typeAndObject

## type

### undefined & null

#### undefined
javascript的代码undefined表示未定义，其是一个变量，并非是一个关键字，为了避免无意中被篡改，一般建议使用void 0来获取undefined值.

#### null
null表示的是：“定义了但是为空”，null是JavaScript的关键字。

---
### number

#### 浮点数的计算
```
  console.log( Math.abs(0.1 + 0.2 - 0.3) <= Number.EPSILON);

```

---
---

## Object
对象的定义：属性的集合。属性分为数据属性和访问器属性，二者都是key-value解构。key可以是字符串或者Symbol类型。

### 基本类型
基本类型的number,string,boolean的运算符提供装箱操作，会根据基础类型构造一个临时对象，是的能在基础类型上调用对应对象的方法

### 类型转换
转换表| null| undefined | boolean(true) | boolean(false)|number|string|symbol|object
:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
boolean | FALSE|FALSE|-|-|O/NaN-false|''-false|TRUE|TRUE
Numer|0|NaN|1|0|-|#stringToNumber|TypeError|#拆箱转换
String|"null"|"undefined"|TRUE|FALSE|#NumberToString|-|TypeError|#拆箱转换
Object|TypeError|#装箱转换|#装箱转换|#装箱转换|#装箱转换|#装箱转换|-

#### 装箱转化
将基本类型转换成对应的对象。
#### 拆箱转化
对象类型到基本类型的转换

对象到Sring和Number的转换都遵循“先拆箱再转换”的规则。通过拆箱转换，把对象变成基本类型，再从基本类型转换为对应的String或者Number。

拆箱转换回尝试调用valueOf和toString来获得拆箱后的基本类型。如果valueOf和toString都不存在，或者没有返回基本类型，则会产生错误类型TypeError。
