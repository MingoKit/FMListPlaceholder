# FMListPlaceholder
![](https://ws1.sinaimg.cn/large/006tNc79gy1fz8ipkdw88j30va0b4q48.jpg)

[![platform](https://img.shields.io/badge/platform-iOS-blue.svg?style=plastic)](#)
[![languages](https://img.shields.io/badge/language-objective--c-blue.svg)](#) 
[![cocoapods](https://img.shields.io/badge/cocoapods-supported-4BC51D.svg?style=plastic)](https://cocoapods.org/pods/FMListPlaceholder)
[![support](https://img.shields.io/badge/support-iOS9%2B-orange.svg)](#) 

#### [**中文说明**](https://github.com/yfming93/FMListPlaceholder/blob/master/README_Chinese.md)


A delightful Placeholder for List View (UITableView, UICollectionView).

**One line code handle empty list placeholder logic.**

### 0x001 Different From Other Similar：

- Placeholders are not displayed at first time while you enter the list. The logic is processed when the list is refreshed again after network request is completed.
- Simple, efficient and practical, one line code can be integrated;
- Provide a more comprehensive and highly customized effect.
- The default effect can be replaced with one line code. Set your own global default effects. You can also customize the effect again in a special list.
- Support custom views as the placeholder.

### 0x002 Renderings
![](https://ws1.sinaimg.cn/large/006tNc79gy1fz8jghf5d0g30hj0dsx6p.gif)


### 0x003 How to use
- Use CocoaPods:
    - write `pod "FMListPlaceholder"` in the `Podfile` file.
    - Open terminal, cd the directory of project. run `pod install`.
    - Import the main file：`#import <FMListPlaceholder.h>`
- Manual import：
    - Drag All files in the `FMListPlaceholder` folder to project.
    - Import the main file：`#import "FMListPlaceholder.h"`


##### One Line Use 
    _tableView.needPlaceholderView = YES;   //the same as UICollectionView
    

Or Use Below
##### Custom Global Default

``` objc
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    [FMListPlaceholder fm_defaultBackgroundColor:UIColor.whiteColor coverName:@"xxx" tips:@"Sorroy,nil here!" tipsTextColor:UIColor.grayColor tipsFont:[UIFont systemFontOfSize:16] coverSize:CGSizeZero coverCenterYOffset:-30 coverSpaceToTips:10];

    return YES;
}
```
#### 0x004 Custom
##### Custom One List 

``` objc
[_tableView fm_emptyCoverName:@"fm_placeholder_nil" emptyTips:@" "];
[_tableView fm_backgroundColor:[UIColor colorWithRed:0.91 green:0.90 blue:0.90 alpha:1.00] tipsTextColor:UIColor.redColor tipsFont:nil];
[_tableView fm_coverCenterYOffset:-80 coverSize:CGSizeMake(90, 120) coverSpaceToTips:20];
// the same as UICollectionView
```
<br/>

##### Click Reload Handle

``` objc
_tableView.reloadBlock = ^(UIScrollView *listView) {
  // Reload Handle is Here!
  // [listView.mj_header beginRefreshing]; // reloadData
};
```
##### Details (See the example program FMListPlaceholderExample for details)


### 0x005 Hope
- If you have any questions during the process or want more interfaces to customize，you can issues me!
Instead of giving me star, it is better to throw a bug to me!
- If you want to participate in the maintenance of this project or have a good design style, welcome to pull request!
- If you feel slightly discomfort in use, please contact me. 
    - BLOG SITE: [www.yfmingo.cn](www.yfmingo.cn)  
    - Email: yfmingo@163.com.
- Hope to improve this project together, let it become more powerful, able to meet the needs of most users!

### 0x006 Change Log
#### 2019.01.23 V1.1.0

- `[+]` Support custom views as the placeholder;
- `[+]` Added some usage examples

### 0x007 QQ Chat Room
![](https://ws3.sinaimg.cn/small/006tNc79gy1fz8aavckscj30f10kl0us.jpg)

### 0x008 Requirements
- iOS 9.0 or later
- Xcode 9.0 or later

### 0x009 [Licenses](https://github.com/yfming93/FMListPlaceholder/blob/master/LICENSE)
**All source code is licensed under the MIT [License](https://github.com/yfming93/FMListPlaceholder/blob/master/LICENSE).**


> MIT License
> 
> Copyright (c) 2019 Fleeming
> 
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
> 
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
> 
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

