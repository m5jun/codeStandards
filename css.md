##1. 声明顺序
  >相关的属性声明应当归为一组，并按照下面的顺序排列：
  
  >Positioning -> Box model -> Typographic ->Visual
  
  >由于定位（positioning）可以从正常的文档流中移除元素，并且还能覆盖盒模型（box model）相关的样式，因此排在首位。
  盒模型排在第二位，因为它决定了组件的尺寸和位置。
  其他属性只是影响组件的内部（inside）或者是不影响前两组属性，因此排在后面。
  
  ```css
  .tuanfe-container {
    /* Positioning */
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 100;
  
    /* Box-model */
    display: block;
    float: right;
    width: 100px;
    height: 100px;
  
    /* Typography */
    font: normal 13px "Helvetica Neue", sans-serif;
    line-height: 1.5;
    color: #333;
    text-align: center;
  
    /* Visual */
    background-color: #f5f5f5;
    border: 1px solid #e5e5e5;
    border-radius: 3px;
  
    /* Misc */
    opacity: 1;
  }
  ```
  
##2. 媒体查询
  >切记将媒体查询放在尽可能相关规则的附近。不要将他们打包放在一个单一样式文件中或者放在文档底部。如果你把他们分开了，将来只会被大家遗忘。
  
  ```
  .element {
      ... 
  }
  .element-avatar {
      ... 
  }
  .element-selected {
      ... 
  }
  
  @media (min-width: 480px) {
      .element {
          ...
      }
      .element-avatar {
          ...
      }
      .element-selected {
          ... 
      }
  }
  
  ```
  
##3. 单行和多行规则声明
>单行规则：对于只包含一条声明的样式，为了易读性和便于快速编辑，建议将语句放在同一行。这样做的关键因素是为了错误检测。例如，CSS 校验器指出在 183 行有语法错误。如果是单行声明，你就不会忽略这个错误；如果是多行声明的话，你就要仔细分析了；
  
>多行规则：对于带有多条声明的样式，应当将声明分为多行，这样结构更加清晰，易读，有的人会觉得占用更多空间，但最终线上都 是会经过压缩的，所以没什么影响。
  
  ```
  /* Single declarations on one line */
  .span1 { width: 60px; }
  .span2 { width: 140px; }
  .span3 { width: 220px; }
  
  /* Multiple declarations, one per line */
  .sprite {
    display: inline-block;
    width: 16px;
    height: 15px;
    background-image: url(../img/sprite.png);
  }
  .icon           { background-position: 0 0; }
  .icon-home      { background-position: 0 -20px; }
  .icon-account   { background-position: 0 -40px; }
  ```
