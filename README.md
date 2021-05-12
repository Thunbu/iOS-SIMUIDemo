#### SDK 集成


```
platform :ios, '9.0'

use_frameworks!

target '工程名' do
inhibit_all_warnings!
source 'https://github.com/Thunbu/TBIMSpec.git'
pod 'TBIMUILibrary'

end
```

#### 简单使用

```
#import <GLSessionViewController.h>
#import <GLIMDBCommand.h>
#import <TBIMManager.h>
[[TBIMManager sharedInstance] initKit:@""]; // 用户申请的appid

[[TBIMManager sharedInstance] loginKit:self.accountTxt.text succ:^(id  _Nonnull data) {
        [[GLIMDBCommand sharedInstanced] openDB:self.accountTxt.text];
        GLSessionViewController *sessionVC = [[GLSessionViewController alloc]initWithSesstionStyle:0];
        [self.navigationController pushViewController:sessionVC animated:YES];
    } fail:^(int code, NSString * _Nonnull msg) {
        
    }];
```

### 常用测试账号

A_8589934620 掏钱猛 
A_8589934619 梅菜饼 
A_8589934618 张大葱 
A_8589934617 炫小银 
A_8589934616 汪大称 
A_8589934615 兔小虾
