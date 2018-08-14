title: Array 的五种迭代方法 -----every() /filter() /forEach() /map() /some()
date: 2018-08-14 15:00:49
tags: 

---

- 1.every() 和 some()

  - every()是对数组中的每一项运行给定函数，如果该函数对每一项都返回true，则返回true。
  - some()是对数组中的每一项运行给定函数，如果该函数对任一项返回true，则返回true。
  - every()和some()很相似，他们都用于查询数组中的项是否满足某个条件，对every()来说，传入的函数必须对每一项都返回true，这个方法才返回true；否则，则返回false。而some()方法则只要传入的函数对数组中的某一项返回true，就会返回true。例如：

```javascript
var numbers = [1, 2, 3, 4, 5, 4, 3, 2, 1];
var everyResult = numbers.every(function (item, index, array) {
  return (item > 2);
});
alert(everyResult); //false
var someResult = numbers.some(function (item, index, array) {
  return (item > 2);
});
alert(someResult); //true
```

- filter()
  filter() 是对数组中的每一项运行给定函数， 返回该函数会返回true的项所组成的数组。 它利用指定的函数确定是否在返回的数组中包含某一项。 例如：

  ```JavaScript
  var numbers = [1, 2, 3, 4, 5, 4, 3, 2, 1];
  var filterResult = numbers.filter(function (item, index, array) {
    return (item > 2);
  });
  alter(filterResult); //[3,4,5,4,3];
  ```

- forEach() 

  是多数组中的每一项运行给定函数，这个方法没有返回值。它只是对数组中的每一项运行传入的函数，没有返回值。本质上与使用for循环迭代数组一样。
