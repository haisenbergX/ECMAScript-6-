# ES6学习笔记 #

----------
## 1. 块级作用域 ##
（1）**let**取代**var**

ES6提出了两个新的声明变量的命令：let和const。其中，let完全可以取代var，因为两者语义相同，而且let没有副作用。
    'use strict';
    
    if (true) {
      let x = 'hello';
    }
    
    for (let i = 0; i < 10; i++) {
      console.log(i);
    } 
上面代码如果用var替代let，实际上就声明了两个全局变量，这显然不是本意。变量应该只在其声明的代码块内有效，var命令做不到这一点。

var命令存在变量提升效用，let命令没有这个问题。
    'use strict';
    
    if(true) {
      console.log(x); // ReferenceError
      let x = 'hello';
    }
