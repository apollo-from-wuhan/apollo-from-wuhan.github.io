# apollo-from-wuhan.github.io

今天学习`vue-cli`时发现, 部署在`github`或`github.io`上方式有所不同, 感到很费解, 所以就开始试着学习如何使用`github.io`

但是怎么都不成功, 一开始本地可以看到, `github`上面看不到, 后来又相反, `github`可以看到, 本地看不到.

总结一下, 碰到的坑:
+ 最大的坑在于`_config.yml`里面的`baseurl`不需要设置, 即删除这一行, 不然本地或远程的显示就会不正常;
+ 阮一峰老师的写法有问题, 直接在`master`分支上`github`才能够显示;
+ `gem`也很慢, 要换用国内的源, 找了好久, 才发现这个https://gems.ruby-china.com/网站值得收藏一下:

> ```bash
>$ gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
>$ gem sources -l
>https://gems.ruby-china.com
># 确保只有 gems.ruby-china.com
> ```

+ `ruby`安装后有几乎3个g, 太大了,好像是安装过程中开发工具(C的)有几乎一个g;
+ 调试过程中的一个技巧, 本地页面跳转异常之后应该直接查看`a`标签的链接, 这样可以很快看出是路径问题`//`,从而导致跳转后IP都变了;
+ 可能直接`fork`别人的主题或blog进行修改会更快更好;
+ 好像任何`github`的库都可以变为`pages`, 但是地址不同, 比如`https://apollo-from-wuhan.github.io/Head-First-HTML5/`和` https://apollo-from-wuhan.github.io/`, 一个在根目录另外一个不在, 这可能也是网上很多教程混乱冲突的地方;
+ 再就是`master`分支和`gh-pages`分支的问题, 难道`github`网站改动过吗? 让人莫名其妙!
+ 自己的博客, 总的说来搭建的失败了, 没有样式, 而且只能自己写源码!! 坑!!

