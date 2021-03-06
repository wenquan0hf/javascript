# 布尔对象

**Boolean** 对象表示两个值，不是“真”就是“假”。

## 语法

创建一个 **Boolean** 对象：

  ```
     var val = new Boolean(value);
  ``` 
 
如果省略 **value** 参数或参数是 0，-0 ，空，假， NaN ，未定义，或者是空字符串（“ ”），这个对象初始值为假。   

## 布尔属性

这里列出了每个属性和它们的描述。

<table  >
<tr>
<th align="left">属性</th>
<th align="left">描述</th>
</tr>
<tr>
<td>constructor</a></td>
<td>返回创建这个对象的布尔函数的一个引用。</td>
</tr>
<tr>
<td>prototype</a></td>
<td>原型属性允许您添加对象的属性和方法。</td>
</tr>
</table>

## 布尔方法

这里列出了每个方法和它们的描述。

<table>
<tr>
<th align="left">方法</th>
<th align="left">描述</th>
</tr>
<tr>
<td>toSource()</a></td>
<td>返回一个包含布尔对象来源的一个字符串；你可以使用这个字符串来创建一个等效的对象。</td>
</tr>
<tr>
<td>toString()</a></td>
<td>
根据对象的值来返回“真”或者“假”。</td>
</tr>
<tr>
<td>valueOf()</a></td>
<td>返回布尔对象的原始值。</td>
</tr>
</table>
    


