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
