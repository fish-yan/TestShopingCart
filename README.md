# TestShopingCart
**本文也是利用第三方实现了淘宝购物车的动画,使用起来非常简单.**
###第一步:
使用cocoaPods导入
如果不会使用cocoaPods请看这:http://blog.csdn.net/fish_yan_/article/details/50483282
```Objective-C
pod 'KNSemiModalViewController_hons82', '~> 0.4.4'
```

###第二步
关键代码
在你需要的viewController中引入头文件,仿照以下方式写
```Objective-C
//button的方法
- (IBAction)addShopingButtonAction:(UIButton *)sender {
    //自己创建一个view
    UIView *aView = [[UIView alloc]initWithFrame:CGRectMake(0, [UIScreen mainScreen].bounds.size.height - 200, [UIScreen mainScreen].bounds.size.width, 200)];
    aView.backgroundColor = [UIColor redColor];
    //不需要背景图得时候直接调用下面这个方法就可以了
//    [self presentSemiView:aView];
    //添加背景图
    UIImageView * bgimgv = [[UIImageView alloc] initWithImage:[UIImage imageNamed:@"background_01"]];
    [self presentSemiView:aView withOptions:@{ KNSemiModalOptionKeys.backgroundView:bgimgv }];
}
```
效果图(这是加了背景图的效果图)
![这里写图片描述](http://img.blog.csdn.net/20160111175244209)

