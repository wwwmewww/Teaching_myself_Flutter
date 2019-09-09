## Keys

1. 什么时候用key？<br>需要添加、删除、重新排序、处于某种状态的相同类型的小部件集合。要修改集合中的装订小部件的顺序或数量,用key很有用。跨部件StatelessWidget 不需要key
2. 什么地方用key？ 放在小部件的顶部。
3. 用哪个key？localKey globalKey? 根据类型使用不用的key
    - ValueKey
    - ObjectKey 
    - UniqueKey，具有多个相同值的小部件 或者 想确保 每个小部件与其它小部件不同。
    - PageKey 用户滚动位置的专用key
    - globalKey 1. 更改父级不会丢失状态 或 访问另一个小部件的信息。2. 验证密码，但不希望与树中其它小部件分享改状态信息