# design-patterns

**工厂模式**

- 工厂模式符合 SO 原则
    - 构造函数和创建者分离，符合单一原则
    - 符合开放封闭原则

<img width="409" alt="Screenshot 2020-07-19 at 9 25 45 AM" src="https://user-images.githubusercontent.com/13563834/87864994-dfcea180-c9a1-11ea-9f31-1fdfeb68e11e.png">

```js
class Product {
  constructor(name) {
    this.name = name;
  }
  init = () => {
    console.log("init");
  };
  fn1 = () => {
    console.log("this is fn1 function");
  };
}

class Creator {
  create = (name) => {
    return new Product(name);
  };
}

// test
let creator = new Creator();
let p = creator.create("p1");
p.init();
p.fn1();

```


_这时候会问什么例子用这种模式呢？_

- React.createElement
- 看下面 React.createElement 的例子会知道 React.createElement 相当于一个工厂，我们传入什么值
 会返回Vnode 给我们

```js

var profile = React.createElement('div', null, 
        React.createElement('img', {src: 'avatar.png', className="profile"})
    )

class Vnode {
 // skip
}

React.createElement = function(tag, attrs, children) {
    return new Vnode(tag, attrs, children)
}
```













## 单例模式

## 策略模式

## 代理模式

## 迭代器模式

## 发布-订阅模式

## 命令模式

## 组合模式

## 模版方法模式

## 享元模式

## 职责链模式

## 中介者模式

## 装饰者模式

## 状态模式

## 适配器模式
