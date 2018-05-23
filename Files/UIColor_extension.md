Extension 

```swift
extension UIColor {
    static let fx_littleGray = UIColor(red: 158/255.0, green: 158/255.0, blue: 158/255.0, alpha: 1)
    static let fx_darkGray = UIColor(red: 67/255.0, green: 70/255.0, blue: 78/255.0, alpha: 1)
    static let fx_background = UIColor(red: 247/255.0, green: 247/255.0, blue: 247/255.0, alpha: 1)
    static let fx_navigationBar = UIColor(red: 50/255.0, green: 131/255.0, blue: 174/255.0, alpha: 1)
    static let fx_underline = UIColor(red: 229/255.0, green: 229/255.0, blue: 229/255.0, alpha: 1)
    
    static func rgbToColor(r: Int, g: Int, b: Int, a: CGFloat = 1) -> UIColor{
        return UIColor(red: CGFloat(r)/255.0,
                       green: CGFloat(g)/255.0,
                       blue: CGFloat(b)/255.0, alpha: a)
    }
}
```

