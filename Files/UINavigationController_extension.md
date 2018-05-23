extension

```swift
extension UINavigationController {
    
    func setAppearance(foregroundColor: UIColor = UIColor.rgbToColor(r: 67, g: 70, b: 78), barTintColor: UIColor = UIColor.white) {
        self.navigationBar.barTintColor = barTintColor
        self.navigationBar.shadowImage = UIImage()
        // 设置title的样式属性
        let titleAttributes = [NSAttributedStringKey.foregroundColor: foregroundColor,
                               NSAttributedStringKey.font: UIFont.PingFangSCMedium(size: 18)!]
        self.navigationBar.titleTextAttributes = titleAttributes
    }
    
    // 判断当前导航控制器的viewControllers中是否包含某一个子控制器,并返回其下标
    func containSubController(_ controllerClass: AnyClass) -> (Bool, Int, UIViewController?) {
        var isContained = false
        var index = 0
        var namedController: UIViewController?
        
        let controllers = self.viewControllers
        for controller in controllers {
            if controller.isMember(of: controllerClass) {
                isContained = true
                index = controllers.index(of: controller)!
                namedController = controller
                break
            }
        }
        
        return (isContained, index, namedController)
    } 
}
```

