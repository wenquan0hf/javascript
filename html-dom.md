## 文档对象模型

在浏览器窗口中的每个网页都可以看作一个对象。

文档对象就代表了在浏览器窗口中显示的那个 HTML 文档。文档对象有很多属性表示其他的一些对象，通过对这些属性的操作，我们就可以访问或者修改文档的内容。

对文档对象的访问和修改的方式被称为**文档对象模型**，或者称为**DOM**。这些对象是按照继承关系组织在一起的。这个继承关系结构用来将网页文档对象联系在一起。

- **窗口对象:** 继承关系中的最顶层。它是继承结构中对顶层的元素。
- **文档对象:** 每一个被加载到窗口中的 HTML 对象变成了文档对象。文档对象中包含了网页的内容。
- **表单对象：** 任何以 `<form>...</form>` 标签圈起来的内容是表单对象。
- **表单控制元素：** 这个表单对象包含表单中定义的所有元素，例如文本框，按钮，单选按钮和多选按钮。

如下是一些重要对象的继承结构图：

![](./images/html-dom.jpg)

有几个文档对象是已经实现了的。下面的部分详细的介绍这些文档对象，并且介绍你如何利用这些对象访问和修改文档内容。

- 传统的文档对象模型： 这个模型是在 JavaScript 语言早期版本中引入的。它能够很好的被所有的浏览器支持，但是仅仅只被允许访问文档某些确定的关键区域，比如，表单，表单元素和图像。
- W3C 文档对象模型： 这种文档对象模型允许访问和修改所有的文档内容，而且它是被万维网组织标准化的。这种模型基本上被所有的现代浏览器支持。
- IE4 文档对象模型： 这种文档对象模型是由微软的 IE 浏览器的第四版本而引入的。IE 5和之后的浏览器版本能够支持 W3C 文档对象模型的大多数特性。


### 文档对象的兼容性

如果你想写个脚本，当 W3C 文档对象模型可用的时候，利用这种模型，而当 IE 4文档对象模型有效的时候，利用 IE 4文档对象模型，因此，你可以利用兼容性测试的方法，这种方法首先检测已经存在的方法或者属性，从而去决定浏览器是否能够兼容你想要的文档对象模型。例如：

```
	if (document.getElementById) {

		 // If the W3C method exists, use it

	}

	else if (document.all) {

		// If the all[] array exists, use it

	}

	else {

		// Otherwise use the legacy DOM

	}
```
