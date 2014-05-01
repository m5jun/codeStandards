##声明顺序
相关的属性声明应当归为一组，并按照下面的顺序排列：Positioning -> Box model -> Typographic ->Visual
由于定位（positioning）可以从正常的文档流中移除元素，并且还能覆盖盒模型（box model）相关的样式，因此排在首位。
盒模型排在第二位，因为它决定了组件的尺寸和位置。
其他属性只是影响组件的内部（inside）或者是不影响前两组属性，因此排在后面。
