##1. 声明顺序
相关的属性声明应当归为一组，并按照下面的顺序排列：
  Positioning -> Box model -> Typographic ->Visual
由于定位（positioning）可以从正常的文档流中移除元素，并且还能覆盖盒模型（box model）相关的样式，因此排在首位。
盒模型排在第二位，因为它决定了组件的尺寸和位置。
其他属性只是影响组件的内部（inside）或者是不影响前两组属性，因此排在后面。

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
