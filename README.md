# 思考：原型中Function和Object之间的关系
原型的一些拓展
### 算是查了一些资料然后自己总结了一下，反正没消化完以后估计也会忘，先存着
![](http://a4.qpic.cn/psb?/V118JuTr0BKcy7/1XpjZtPCYcExisnyXyJM0WKFQ.DLmFJMs.uMysd61tU!/m/dPMAAAAAAAAA&bo=9wSAAgAAAAADB1M!&rf=photolist)
```js
function Hero(){
    this.name = 'zhangwuji';
}
var hero = new Hero();

console.log(hero instanceof Object);// true
console.log(Hero instanceof Function);// true
console.log(Hero instanceof Object);// true
console.log(Hero.prototype instanceof Object);// true

console.log(Hero.prototype);// 显式原型
console.log(hero.__proto__);// 隐式原型
console.log(hero.constructor);// 构造器

var obj = new Object();

// Object也是一个对象
console.log(Object instanceof Object);// true
// Object的构造器是Function
console.log(Object.constructor);// Function
// Function也是一个对象
console.log(Function instanceof Object);// true
// Function的构造器是自身
console.log(Function.constructor);// Function

console.log(Object instanceof Function);// true

// 思考题：Object和Function的原型属性是谁? - Object为什么是Function类型?
```
