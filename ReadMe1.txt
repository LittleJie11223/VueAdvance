选择题 
1.D
2.D

简答题：
对比新旧节点差异，首先调用2个钩子函数，对比之前触发，一个是prepatch,一个是update钩子函数。然后触发postpatch，之后是判断新旧节点的text属性，之后是判断新旧节点的text属性，判断节点中是否有text属性，并且不等于旧节点的属性，然后更新dom中的文本内容；然后判断老节点中是否有children,如果有则移除，病设置新dom中的text内容，如果新旧都有children，如果不想等，则updateChildren,然后更新差异；如果只有新节点有，则看老节点是否有text，如果有，则清空，再去添加子节点；如果老节点有children，新节点没有，则移除所有老节点；如果老节点有text，新的没有，则清空dom中的textContent。
