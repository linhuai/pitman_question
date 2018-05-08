# 坑人的面试题

**写出下面代码的运行结果**

	console.log([] = []); // false

	console.log(![] == false); // true

	console.log([] == false); // true

	console.log(!!"hello"); // true

	console.log("hello" == true); // false

	console.log(typeof(typeof('hello'))); // string

**以下代码的运行的结果是什么**

	function Foo() {
		getName = function () {
			alert(1);
		}
		return this;
	}

	Foo.getName = function () {
		alert(2);
	}

	Foo.prototype.getName = function () {
		alert(3);
	}

	var getName = function () {
		alert(4)
	}

	function getName() {
		alert(5);
	}

	Foo.getName(); // 2

	getName(); // 4

	Foo().getName(); // 1

	getName(); // 1

	new Foo.getName(); // 2



