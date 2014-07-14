##1. 代码格式化
  >当定义连续几个变量时，采用如下这种排版方式，我是从underscore.js中学习到的，感觉排版清楚，会减少很多不必要的var关键字。
    
  ```
  //bad code
  
  var a=1;
  var b=2;
  var c=3;
  
  //good code
  var a=1,
      b=2,
      c=3;
  ```

##2. 命名
  >当查找jQuery对象，最好在变量前加$前缀以表示是jQuery对象。

  ```
  // bad code
  var first = $('#first')，
      second = $('#second')，
      value = $first.val();
  
  //good code
  var $first = $('#first')，
      $second = $('#second'),
      value = $first.val();
  
  ```
##3. 字符串过长截断
  >按一定长度截断字符串，并使用+运算符进行连接。分隔字符串尽量按语义进行，如不要在一个完整的名词中间断开。特别的，对于HTML片段的拼接，通过缩进，保持和HTML相同的结构，也可使用数组来进行拼接，相对+运算更容易调整缩进。

  ```
   var html = '' // 此处用一个空字符串，以便整个HTML片段都在新行严格对齐
      + '<article>'
      +     '<h1>Title here</h1>'
      +     '<p>This is a paragraph</p>'
      +     '<footer>Complete</footer>'
      + '</article>';
      
      
      var html = [
        '<article>',
            '<h1>Title here</h1>',
            '<p>This is a paragraph</p>',
            '<footer>Complete</footer>',
        '</article>'
      ];
    html = html.join(''); // 注意需要join
  
  ```
  
##4. 过长的逻辑条件组合
  >当较复杂的逻辑条件组合比较长时，应当将每个条件独立一行，逻辑运算符放置在行首进行分隔，或将部分逻辑按逻辑组合进行分隔。最终将右括号)与左大括号{放在独立一行，保证与if内语句块能容易视觉辨识。

  ```
    // 注意逻辑运算符前的缩进
  if (user.isAuthenticated()
      && user.isInRole('admin')
      && user.hasAuthority('add-admin')
      || user.hasAuthority('delete-admin')
  ) {
      // Code
  }
    
  ```
  
##5. 文件注释
  >以/**开始，以*/结束，文件注释中以@file文件说明，@author开发者信息，@date时间

  ```
  /**
   * @file 弹出对话框组件
   * @author tuanfe@baidu.com
   * @date 2014/5/11
   */
    
  ```
##6. 空格
  >在特定的位置加上空格有助于代码的可读性，以下位置 必须(MUST) 加上空格：

除括号外，所有运算符的前后，如
用作代码块起始的左大括号{前，包括if、else、try、finally这些关键字之后，以及函数定义的参数列表之后
以下关键字之后：for、switch、while、function
对象初始化（{ ... }）的每个属性名的冒号:后
所有逗号,后
单行的对象初始化（{ ... }）左大括号{后和右大括号}前
注意：函数声明与具名函数表达式，函数名与括号之间 不允许(MUST NOT) 包含空格，以期和函数调用保持一致。以下是一个函数的正确声明方式：

  ```
function foo(x, y, z) {
    // FunctionBody
}

var foo = function (x, y, z) {
    // FunctionBody
};

var foo = function foo(x, y, z) {
    // FunctionBody
};
    
  ```
