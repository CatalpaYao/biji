text-decoration: none;失效的解决方法
经过查阅，如果想要去掉a标签的默认效果，就要用`text-decoration: none;`，但是经过试验发现并不好用，可能是因为你用a标签里的class或id定义的CSS样式，就像这样：

```
<div class="test>
    <a class="navbarLink">链接</a>
</div>

.navbarLink{
    text-decoration: none;
}

如果这样定义a的下划线是不会消失的。

如果想要去掉默认样式，必须要这样定义CSS：
.test a{
    text-decoration: none;
}
