# LTNavigationBar
NavigationBar分类,可以更改NavigationBar的颜色呵呵透明度等.


## Usage

First, import this lib:
```objective-c
#import "UINavigationBar+Awesome.h"
```

The category includes lots of method that helps to change UINavigationBar's appearance dynamically:
```objective-c
@interface UINavigationBar (Awesome)
- (void)lt_setBackgroundColor:(UIColor *)backgroundColor;
- (void)lt_setElementsAlpha:(CGFloat)alpha;
- (void)lt_setTranslationY:(CGFloat)translationY;
- (void)lt_reset;
@end
```

You can call the various setter wherever you want, like:
```objective-c
[self.navigationController.navigationBar lt_setBackgroundColor:[UIColor blueColor]];
```

And usually in `viewWillDisappear`, you should call this method to avoid any side effects:
```objective-c
- (void)viewWillDisappear:(BOOL)animated
{
[super viewWillDisappear:animated];
[self.navigationController.navigationBar lt_reset];
}
```

See the example for details~ 
